---
title: Integrando aplicativos de capacidade de gerenciamento com o instalador Clique para Executar do Microsoft 365 Apps
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Saiba como integrar o instalador Clique para Executar do Microsoft 365 Apps com uma solução de gerenciamento de software.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297311"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Integrando aplicativos de capacidade de gerenciamento com o instalador Clique para Executar do Microsoft 365 Apps

Saiba como integrar o instalador Clique para Executar do Microsoft 365 Apps com uma solução de gerenciamento de software.
  
O instalador Clique para Executar do Microsoft 365 Apps fornece uma interface COM que permite aos profissionais de TI e às soluções de gerenciamento de software controlarem o gerenciamento de atualizações. Essa interface tem recursos adicionais de gerenciamento além do que é fornecido pela Ferramenta de Implantação do Office.
  
> [!NOTE]
> Este artigo se aplica aos aplicativos do Office que usam o instalador Clique para Executar. 
  
## <a name="integrating-with-the-click-to-run"></a>Integração ao Clique para Executar

Para usar essa interface, um aplicativo de capacidade de gerenciamento invoca a interface COM e chama APIs expostas que se comunicam diretamente com o serviço de instalação Clique para Executar. 
  
> [!NOTE]
> O instalador Clique para Executar do Office pode ser executado na linha de comando com parâmetros que podem controlar o comportamento, conforme documentado em [Ferramenta de Implantação do Office para Clique para Executar](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool). 
  
**Veja a seguir um diagrama conceitual da interface COM**

![Um diagrama usando a interface COM no instalador Clique para Executar do Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de uso da interface COM no instalador Clique para Executar do Office")
  
O instalador Clique para Executar do Microsoft 365 Apps implementa uma interface baseada em COM, **IUpdateNotify** registrada no CLSID **CLSID_UpdateNotifyObject**.
  
Essa interface pode ser invocada da seguinte maneira:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

A chamada será bem-sucedida se o autor da chamada estiver em execução sob privilégios elevados, pois o programa de instalação Clique para Executar deve ser executado com privilégios elevados.
  
A interface COM **IUpdateNotify** expõe três funções assíncronas responsáveis por validar os comandos e parâmetros, bem como agendar a execução com o serviço de instalação Clique para Executar. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Um quarto método, **Status**, pode ser usado para obter informações sobre o status do último comando executado ou o status do comando em execução no momento (isto é, êxito, falha, códigos de erro detalhados).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Há quatro estados em que o serviço de instalação Clique para Executar pode estar durante o seu ciclo de vida, durante o qual os métodos **IUpdateNotify** podem ser chamados; Reinicializando, Ocioso, Baixando e Aplicando. 
  
**Veja a seguir o diagrama de Máquina de Estado da interface COM**

![Um diagrama de estado da interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Um diagrama de estado para a interface COM")
  
> [!NOTE]
> **Reinicializando**: quando o computador está sendo inicializado, há um período em que o serviço instalador Clique para Executar fica indisponível. Uma chamada bem-sucedida ao método Status após uma reinicialização retornará eUPDATE_UNKNOWN. 
  
**Ocioso:** quando o instalador Clique para Executar estiver no estado ocioso, você poderá chamar: 
  
- **Aplicar**: instala o conteúdo anteriormente baixado.
    
- **Cancelar**: retorna `0x800000e`, "Um método foi chamado em um momento inesperado".
    
- **Baixar**: baixa novo conteúdo no cliente para instalação posterior.
    
- **Status**: retorna o resultado da última ação concluída ou uma mensagem de erro se a ação terminou em falha. Se não houver ação anterior, **Status** retornará `eUPDATE_UNKNOWN`.
    
**Baixando:** quando o instalador Clique para Executar estiver no estado baixando, você poderá chamar: 
  
- **Aplicar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".
    
- **Cancelar**: interrompe o download e remove o conteúdo parcialmente baixado.
    
- **Baixar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado". 
    
- **Status**: retorna **DOWNLOAD_WIP** para indicar que o trabalho de download está em andamento. 
    
**Aplicando:** quando o instalador Clique para Executar estiver no processo de instalação do conteúdo anteriormente baixado: 
  
- **Aplicar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado".
    
- **Cancelar**: retorna `0x800000e`, a ação Aplicar não pode ser cancelada.
    
- **Baixar**: retorna **HRESULT** com o valor `0x800000e`, "Um método foi chamado em um momento inesperado". 
    
- **Status**: retorna **APPLY_WIP** para indicar que o trabalho de aplicação está em andamento. 
    
> [!NOTE]
> Uma vez que OfficeC2RCOM é um serviço COM+ e foi dinamicamente carregado, é preciso chamar **CoCreateInstance** toda vez que você chama um método nessa classe, a fim de garantir a obtenção do resultado esperado. O serviço COM+ tratará de criar uma nova instância, se necessário. Quando um dos métodos é chamado pela primeira vez, COM+ carregará o objeto **IUpdateNotify** e o executará em uma das instâncias de dllhost.exe. O novo objeto permanecerá ativo por aproximadamente 3 minutos em estado ocioso. Se uma chamada subsequente for feita dentro de três minutos, a contar da última chamada, o objeto **IUpdateNotify** permanecerá carregado e não será criada uma nova instância. Se nenhuma chamada for feita em três minutos, o objeto IUpdateNotify será descarregado e um novo objeto **IUpdateNotify** será criado quando a próxima chamada for feita. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guia de referência da API COM do instalador Clique para Executar

Na seguinte documentação de referência de API:
  
- Os parâmetros estão em um formato de par chave/valor separados por um espaço.
    
- Os parâmetros não diferenciam maiúsculas de minúsculas.
    
- Há uma [lista de parâmetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) com documentação disponível. 
    
- Agora, o resumo da interface IUpdateNotify2 está incluído.
    
### <a name="apply"></a>Aplicar

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parâmetros

-  _displaylevel_: **true** para mostrar o status da instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status da instalação, incluindo erros, durante o processo de atualização. O padrão é **false**.
    
-  _forceappshutdown_: **true** para forçar os aplicativos do Office a desligarem imediatamente quando a ação **Aplicar** for disparada; **false** para falha, se algum aplicativo do Office estiver em execução. O padrão é **false**. Veja [Comentários](#bk_ApplyRemark) para saber mais. 
    
  Se algum aplicativo do Office estiver em execução quando a ação **Aplicar** for disparada, a ação **Aplicar** normalmente falha. Passar `forceappshutdown=true` ao método **Aplicar** fará com que o serviço **OfficeClickToRun** desligue imediatamente os aplicativos e aplique a atualização. O usuário poderá enfrentar perda de dados nesse caso. 
    
#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|**S_OK** <br/> |A ação foi enviada com êxito ao serviço Clique para Executar para execução.  <br/> |
|**E_ACCESSDENIED** <br/> |O autor da chamada não está em execução com privilégios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Parâmetros inválidos foram passados.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |A ação não é permitida neste momento. Veja [Comentários](#bk_ApplyRemark) para saber mais.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Comentários

- Se algum aplicativo do Office estiver em execução quando a ação **Aplicar** for disparada, a ação **Aplicar** falhará. Passar `forceappshutdown=true` ao método **Aplicar** fará com que o serviço **OfficeClickToRun** desligue imediatamente qualquer aplicativo do Office que esteja em execução e aplique a atualização. O usuário pode sofrer perda de dados, uma vez que não é solicitado que salve as alterações em documentos abertos. 
    
- Essa ação poderá ser disparada somente quando o status COM for um dos seguintes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Se você chamar o método **Apply** sem baixar o conteúdo antes, o método **Apply** indicará **Êxito**, pois ele não detectou nada a ser aplicado e concluiu o processo **Apply** com êxito. 
    
### <a name="cancel"></a>Cancelar

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|S_OK  <br/> |A ação foi enviada com êxito ao serviço Clique para Executar para execução.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |A ação não é permitida neste momento. Consulte a seção [Comentários](#bk_CancelRemarks) para obter mais informações  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Comentários

- Esse método poderá ser disparado somente quando o status COM for **eDOWNLOAD_WIP**. Ele tentará cancelar a ação de download atual. O status COM será alterado para **eDOWNLOAD_CANCELLING** e, por fim, para **eDOWNLOAD_CANCELED**. O status COM retornará **E_ILLEGAL_METHOD_CALL** se disparado em qualquer outro momento. 
    
### <a name="download"></a>Baixar

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parâmetros

-  _displaylevel_: **true** para mostrar o status da instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status da instalação, incluindo erros, durante o processo de atualização. O padrão é **false**.
    
-  _updatebaseurl_: URL para a fonte alternativa de download.
    
-  _updatetoversion_: a versão para a qual atualizar o Office. Defina esse parâmetro se desejar atualizar para um versão mais antiga do que a versão que está atualmente instalada.
    
-  _downloadsource_: CLSID da implementação **IBackgroundCopyManager** personalizada (gerenciador do BITS). 
    
-  _contentid_: identifica o conteúdo a ser baixado do servidor de conteúdo por meio do gerenciador do BITS personalizado. Esse valor é passado pela interface do BITS para interpretação.
    
#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|**S_OK** <br/> |A ação foi enviada com êxito ao serviço Clique para Executar para execução.  <br/> |
|**E_ACCESSDENIED** <br/> |O autor da chamada não está em execução com privilégios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Parâmetros inválidos foram passados.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |A ação não é permitida neste momento. Veja [Comentários](#bk_DownloadRemark) para saber mais.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Comentários

- Você deve especificar _downloadsource_ e _contentid_ como um par. Caso contrário, o método **Baixar** retornará um erro **E_INVALIDARG**. 
    
- Se _downloadsource_, _contentid_ e _updatebaseurl_ forem fornecidos, _updatebaseurl_ será ignorado. 
    
- Essa ação poderá ser disparada somente quando o status COM for um dos seguintes: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Se você chamar o método **Apply** sem o conteúdo baixado anteriormente, o método **Apply** indicará **Êxito**, pois ele não detectou nada a ser aplicado e concluiu o processo **Apply** com êxito. 
    
#### <a name="examples"></a>Exemplos

- Para baixar o conteúdo do gerenciador do BITS personalizado: chame a função **download()** passando os seguintes parâmetros: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Para baixar o conteúdo da REDE de Distribuição de Conteúdo do Office (CDN): chame a função **download()** sem especificar os _parâmetros downloadsource_, _contentid_ ou _updatebaseurl._ 
    
- Para baixar o conteúdo de um local personalizado: chame a função **download()** passando o seguinte parâmetro: 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>Status

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>Parâmetros

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Ponteiro para uma estrutura UPDATE_STATUS_REPORT.  <br/> |
   
#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|**S_OK** <br/> |O método **Status** sempre retorna esse resultado. Inspecione a estrutura `UPDATE_STATUS_RESULT` para ver o status atual ação.  <br/> |
   
#### <a name="remarks"></a>Comentários

- O campo de status de `UPDATE_STATUS_REPORT` contém o status de ação atual. Um dos seguintes valores de status é retornado: 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- Se o último comando resultou em um erro, o campo de erro de `UPDATE_STATUS_REPORT` conterá informações detalhadas sobre o erro. Dois tipos de código de erro são retornados do método **Status**. 
    
- Se o erro for inferior a `UPDATE_ERROR_CODE::eUNKNOWN`, o erro será um dos seguintes códigos de erro predefinidos:
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  Se um código de erro de retorno for superior a `UPDATE_ERROR_CODE::eUNKNOWN`, trata-se do **HRESULT** de uma chamada de função com falha. Para extrair o HRESULT, subtraia `UPDATE_ERROR_CODE::eUNKNOWN` do valor retornado no campo de erro de `UPDATE_STATUS_REPORT`.
    
  A lista completa de valores de status e erro pode ser exibida inspecionando a biblioteca de tipos **IUpdateNotify** inserida em OfficeC2RCom.dll. 
    
- O campo contentid é usado para chamadas a **Status** depois que **Baixar** tiver sido iniciado e retornar o contentid que foi passado à chamada **Baixar**. É uma prática recomendada inicializar esse campo como **nulo** antes chamar o método **Status** e, em seguida, verificar o valor depois que **Status** tiver sido retornado. Se o valor ainda for **null**, isso significa que não há contentid a ser retornado. Se o valor não for **null**, você precisará liberá-lo com um chamada a **SysFreeString()**. Veja um trecho de código de como chamar **Status** após **Baixar**.
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a>Resumo da interface IUpdateNotify2

Na versão [16.0.8208.6352] adicionamos uma nova interface **IUpdateNotify2.** 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Essa interface também hospedava a interface IUpdateNotify original para fornecer compatibilidade com versões anteriores. Isso significa que, ao usar essa interface, você terá acesso a todos os métodos fornecidos na interface **UpdateNotifyObject**. 
    
- Novos métodos adicionados a IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Obtenha a lista de aplicativos de bloqueio de atualizações. Essa chamada retornará os aplicativos do Office em execução que impedirão o processo de atualização de prosseguir. 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtenha os dados de implantação do Office. 
    
- Se desejar usar os novos métodos, você precisará garantir:
    
  - Que a sua versão C2R seja mais nova do que o build acima (\> = build fork de junho).
    
  - O uso de UpdateNotifyObject2, em vez de **UpdateNotifyObject** para chamar **CoCreateInstance**.
    
Se você não usar qualquer um dos métodos novos, não será necessário alterar nada. Todos os métodos existentes funcionarão exatamente da mesma maneira que antes.
  
## <a name="implementing-the-bits-interface"></a>Como implantar a interface do BITS

O BITS ([Serviço de Transferência Inteligente em Segundo Plano](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal)) é um serviço fornecido pela Microsoft para transferir arquivos entre um cliente e um servidor. O BITS é um dos canais que o instalador Clique para Executar do Office pode usar para baixar conteúdo. Por padrão, o instalador Clique para Executar do Microsoft 365 Apps usa a implementação do BITS criada pelo Windows para baixar o conteúdo da CDN. 
  
Ao fornecer uma implementação do BITS personalizado ao método **download()** da interface **IUpdateNotify**, seu software de capacidade de gerenciamento pode controlar onde e como o cliente baixa o conteúdo. Uma interface do BITS personalizada é útil ao fornecer um canal de distribuição de conteúdo personalizado diferente dos canais integrados Clique para Executar, como CDN, servidores IIS ou compartilhamentos de arquivos. 
  
O requisito mínimo para uma interface do BITS personalizado trabalhar com o serviço C2R do Office é:
  
- Para **IBackgroundCopyManager**:
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- Para **IBackgroundCopyJob**:
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- Para **IBackgroundCopyJob3**:
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Para as funções `Addfile` e `AddFileWithRanges`, a URL remota está no seguinte formato: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits é embutido em código e significa o BITS personalizado.
    
  -  _\<contentid\>_ é o _parâmetro contentid_ do **método Download().** 
    
  -  _\<relative path to target file\>_ fornece o local e o nome do arquivo a ser baixado. 
    
    Por exemplo, se você tiver fornecido um _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` ao método **Download()** e o C2R do Office quiser baixar o arquivo cab da versão, como o arquivo `v32.cab`, ele chamará **AddFile()** com o seguinte `RemoteUrl`:
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Para **IBackgroundCopyError**:
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Para **IBackgroundCopyFile**:
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a>Como automatizar o preparo do conteúdo

Os administradores de IT podem optar por ter clientes da área de trabalho habilitados para receber atualizações automaticamente quando estão disponíveis diretamente da CDN ou podem optar por controlar a implantação de atualizações disponíveis nos canais de atualização usando a Ferramenta de Implantação do Office ou o Microsoft Endpoint Configuration Manager.
  
O serviço dá suporte à capacidade das ferramentas de gerenciamento de reconhecer e automatizar o download do conteúdo quando as atualizações são disponibilizadas.
  
**A imagem a seguir é uma visão geral de como baixar uma imagem personalizada**

![Um diagrama usando a interface COM no instalador Clique para Executar do Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de uso da interface COM no instalador Clique para Executar do Office")
  
### <a name="overview-of-downloading-a-custom-image"></a>Visão geral de como baixar uma imagem personalizada
  
No diagrama anterior, você verá que uma nova imagem do Microsoft 365 Apps está disponível na CDN. Junto com a imagem do Microsoft 365 Apps, uma API está disponível com as informações necessárias para habilitar o software de capacidade de gerenciamento para criar imagens personalizadas diretamente, substituindo a necessidade de usar a Ferramenta de Implantação do Office.

Uma empresa configura o WSUS para sincronizar as atualizações do Microsoft 365 Apps. Essas atualizações não contêm a carga real da imagem, mas permitem que o software de capacidade de gerenciamento reconheça quando conteúdo novo está disponível. O software de capacidade de gerenciamento pode ler os metadados da Atualização do Microsoft 365 Apps para entender a qual versão do Office a atualização se aplica.

Se a atualização for aplicável, o software de capacidade de gerenciamento pode usar o conteúdo da CDN e a lista de arquivos para criar a imagem personalizada e armazená-la no local do compartilhamento de arquivos que ele está configurado para usar.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Usando a API da lista de arquivos do Microsoft 365 Apps

A API da lista de arquivos do Microsoft 365 Apps é usada para recuperar os nomes dos arquivos necessários para uma atualização específica do Microsoft 365 Apps.

Solicitação HTTP

GET https://config.office.com/api/filelist

Não forneça um corpo de solicitação para esse método.

Nenhuma permissão é necessária para chamar essa API.

Parâmetros de consulta opcionais

|**Nome**|**Descrição**|
|:-----|:-----|
| canal <br/>| Especifica o nome do canal  <br/> Opcional – padrão para 'SemiAnnual' <br/> Valores com suporte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| versão <br/>| Especifica a versão de atualização <br/> Opcional – assume como padrão a versão mais recente disponível para o canal especificado |
| arch <br/>| Especifica a arquitetura do cliente <br/> Opcional – o padrão é 'x64' <br/> Valores com suporte: x64, x86 |
| lid <br/>| Especifica os arquivos de idioma a incluir <br/> Opcional – assume como padrão nenhum <br/> Para especificar vários idiomas, inclua um parâmetro de consulta de lid para cada idioma <br/> Use o formato do identificador de idioma, por ex. 'en-us', 'fr-fr' |
| alllanguages <br/>| Especifica a inclusão de todos os arquivos de idioma <br/> Opcional – o padrão é false |

Resposta HTTP

Se bem-sucedido, este método retorna um código de resposta 200 OK e uma coleção de objetos de arquivo no corpo da resposta.

Para criar uma imagem, siga estas etapas:
1.  Chame a API, fornecendo os parâmetros de consulta apropriados para o canal, a versão e a arquitetura da atualização em que você está interessado.
Observação: objetos de arquivo com o atributo "lcid": "0" são arquivos neutros de idioma e devem ser incluídos na imagem.
2.  Construa uma imagem local da CDN iterando pelos objetos de arquivo e copiando os arquivos da CDN, enquanto cria a estrutura de pastas conforme especificado pelo atributo "relativePath" definido para cada um dos objetos de arquivo.

O exemplo a seguir recupera a lista de arquivos do Canal Atual e a versão 16.0.4229.1004 para 64bit e inclui os arquivos de idioma francês e inglês:

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Verificação de hash de arquivos .dat

As ferramentas de criação de imagem podem verificar a integridade dos arquivos .dat baixados comparando um valor de hash calculado com o valor de hash fornecido associado a cada um dos arquivos .dat. Veja a seguir um exemplo de um objeto de arquivo que especifica os valores hashLocation e hashAlgorithm:
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- O **atributo hashLocation** especifica o local do caminho relativo do arquivo .cab que contém o valor de hash. Crie o local do arquivo hash concatenando a URL + relativePath + hashLocation. No seguinte exemplo, o local stream.x64.bg-bg.hash seria: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- O **atributo hashAlgorithm** especifica qual algoritmo de hash foi usado. 
    
  Para validar a integridade do arquivo stream.x64.bg-bg.dat, abra o stream.x64.bg-bg.hash e leia o valor do HASH, que é a primeira linha do texto no arquivo de hash. Compare-o com o valor do hash calculado (usando o algoritmo de hash especificado) para verificar a integridade do arquivo .dat baixado.
    
  O exemplo a seguir mostra o código C# para leitura do hash.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Atualizações do Microsoft 365 Apps

Todas as Atualizações de Aplicativos do Microsoft 365 são publicadas no [Catálogo do Microsoft Update.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)
  
As Atualizações de Aplicativos do Microsoft 365 permitem que o software de capacidade de gerenciamento trate as Atualizações de Aplicativos do Microsoft 365 de maneira muito semelhante a qualquer outra atualização do WU com uma exceção; as atualizações do cliente não contêm uma carga real. As Atualizações de Aplicativos do Microsoft 365 não devem ser instaladas em nenhum cliente, mas usadas para disparar os fluxos de trabalho com o software de capacidade de gerenciamento substituindo o comando de instalação pelo mecanismo de instalação baseado em COM mostrado acima.

**A figura a seguir mostra um diagrama do fluxo de trabalho da Atualização de Cliente do Office 365.**

![Diagrama de fluxo de trabalho de atualizações do cliente O365PP .](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de fluxo de trabalho para atualizações do cliente O365PP")
  
Cada Atualização do Microsoft 365 Apps publicada inclui metadados sobre a atualização. Esses metadados incluem um parâmetro chamado MoreInfoUrl que pode ser usado para derivar a chamada de API para a API da lista de arquivos para essa atualização específica.

No exemplo a seguir, a API da lista de arquivos é incorporada ao MoreInfoURL e começa com "ServicePath="

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Metadados adicionais para automatização do preparo de conteúdo

**API do Histórico de Versões**
  
A API do histórico de versões do Microsoft 365 Apps é usada para recuperar detalhes de cada uma das atualizações publicadas na CDN juntamente com os nomes de canal e outros atributos de canal.

Solicitação HTTP

```http
GET https://config.office.com/api/filelist/channels 
```

Não forneça um corpo de solicitação para esse método.

Nenhuma permissão é necessária para chamar essa API.

Resposta HTTP

Se bem-sucedido, este método retorna um código de resposta 200 OK e uma coleção de objetos de arquivo no corpo da resposta.

**SKUs API**
  
A API de SKUs retorna informações úteis para determinar quais produtos estão disponíveis para implantação e manutenção da CDN do Office, juntamente com várias opções para cada um.

Solicitação HTTP

```http
GET https://config.office.com/api/filelist/skus 
```

Não forneça um corpo de solicitação para esse método.

Nenhuma permissão é necessária para chamar essa API.

Resposta HTTP

Se bem-sucedido, este método retorna um código de resposta 200 OK e uma coleção de objetos de arquivo no corpo da resposta.
