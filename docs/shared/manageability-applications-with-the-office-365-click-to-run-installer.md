---
title: Integrar aplicativos de capacidade de gerenciamento com o instalador de click-to-run do Office 365
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Saiba como integrar o instalador do Office 365 Click-to-Run com uma solução de gerenciamento de software.
ms.openlocfilehash: abe941e3e3818eed1f18108f1678e46e8156b08c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771189"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a>Integrar aplicativos de capacidade de gerenciamento com o instalador de click-to-run do Office 365

Saiba como integrar o instalador do Office 365 Click-to-Run com uma solução de gerenciamento de software.
  
O instalador do Click-to-Run do Office 365 fornece uma interface COM que permite que os profissionais de TI e soluções de gerenciamento de software controle programático sobre gerenciamento de atualizações. Esta interface oferece recursos de gerenciamento adicionais além do que é fornecido pela ferramenta de implantação do Office.
  
> [!NOTE]
> Este artigo se aplica ao Office 2016 e posterior, Office 365. 
  
## <a name="integrating-with-the-click-to-run"></a>Integrando com o Click-to-Run

Para usar essa interface, um aplicativo de gerenciabilidade invoca a interface COM e chamadas expostos APIs que se comunicam diretamente com o serviço de instalação Click-to-Run. 
  
> [!NOTE]
> O instalador do Office Click-to-Run pode ser executado na linha de comando com os parâmetros que podem controlar o comportamento, conforme documentado no [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/en-us/download/details.aspx?id=49117). 
  
**A seguir é um diagrama conceitual da interface COM**

![Um diagrama de usar a interface COM no installer Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no installer Click-To-Run do Office")
  
A interface do Office 365 Click-to-Run installer implementa um baseado em COM, **IUpdateNotify** registrado para CLSID **CLSID_UpdateNotifyObject**.
  
Essa interface pode ser invocado da seguinte maneira:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

A chamada só será bem-sucedida se o chamador está sendo executado em privilégios elevados, como o programa de instalação Click-to-Run deve ser executado com privilégios elevados.
  
A interface **IUpdateNotify** COM expõe três funções assíncronas responsáveis para validar os comandos e parâmetros e agendar a execução com o serviço de instalação Click-to-Run. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

A outro método, o **Status**, pode ser usado para obter mais informações sobre o status do último comando executado ou o status do comando atualmente em execução (ou seja, êxito, falha, códigos de erro detalhadas).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Existem quatro estados de que o serviço de instalação Click-to-Run pode estar em durante o ciclo de vida, durante o qual os métodos **IUpdateNotify** poderão ser convocados; Reinicializar, ociosa, baixando e aplicação. 
  
**A seguir é o diagrama de máquina de estado de Interface COM**

![Um diagrama de estado para a interface COM.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Um diagrama de estado para a interface COM")
  
> [!NOTE]
> **Rebooting**: quando o computador está inicializando há um período de tempo quando o serviço do installer Click-to-Run não está disponível. Uma chamada bem sucedida para o método de Status após uma reinicialização retornará eUPDATE_UNKNOWN. 
  
**Ocioso:** Quando o instalador Click-to-Run está no estado ocioso, você pode chamar: 
  
- **Aplicar**: Install conteúdo baixado anteriormente.
    
- **Cancelar**: retorna `0x800000e`, "um método foi chamado num momento inesperado".
    
- **Download**: baixa o novo conteúdo para o cliente para instalação posterior.
    
- **Status**: retorna o resultado de uma mensagem de erro ou a última ação concluída se a ação é encerrada em falha. Se não houver nenhuma ação anterior, o **Status** retorna `eUPDATE_UNKNOWN`.
    
**Baixando:** Quando o instalador Click-to-Run está no estado de download, você pode chamar: 
  
- **Aplicar**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado".
    
- **Cancelar**: interrompe o download e remove o conteúdo baixado parcialmente.
    
- **Download**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado". 
    
- **Status**: retorna **DOWNLOAD_WIP** para indicar que o trabalho de download está em andamento. 
    
**Aplicação:** Quando o instalador do Click-to-Run está no processo de instalação anteriormente Baixe conteúdo: 
  
- **Aplicar**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado".
    
- **Cancelar**: retorna `0x800000e`, a ação de aplicar não pode ser cancelada.
    
- **Download**: retorna um **HRESULT** com o valor `0x800000e`, "um método foi chamado num momento inesperado". 
    
- **Status**: retorna **APPLY_WIP** para indicar que se aplicam a trabalho estiver em andamento. 
    
> [!NOTE]
> Como OfficeC2RCOM é um serviço COM + e é carregado dinamicamente, você precisará chamar **CoCreateInstance** toda vez que você chama um método nessa classe para garantir que você obtenha o resultado esperado. O serviço COM + manipulará criando uma nova instância, se necessário. Quando um dos métodos é chamado pela primeira vez, COM + carregará o objeto **IUpdateNotify** e executá-lo dentro de uma das instâncias dllhost.exe. O novo objeto ficará ativo por cerca de 3 minutos em ocioso. Se for feita uma chamada de subsequente em três minutos da última chamada, o objeto **IUpdateNotify** permanecerá carregado e uma nova instância não é criada. Se nenhuma chamada for feita em três minutos, o objeto IUpdateNotify será descarregado e será criado um novo objeto **IUpdateNotify** quando a próxima chamada é feita. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guia de referência de API COM instalador Click-to-Run

Na seguinte documentação de referência de API:
  
- Parâmetros estão em um formato de par de chave/valor separado por um espaço.
    
- Os parâmetros não diferenciam maiusculas de minúsculas.
    
- Há uma [lista de parâmetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) com a documentação disponível. 
    
- Resumo das IUpdateNotify2 interface agora é incluído.
    
### <a name="apply"></a>Aplicar

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parâmetros

-  _displaylevel_: **true** para mostrar o status de instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status de instalação, incluindo erros, durante o processo de atualização. O padrão é **false**.
    
-  _forceappshutdown_: **true** para forçar os aplicativos do Office para serem desligados imediatamente quando a ação de **Aplicar** for disparada; **false** falhe se quaisquer aplicativos do Office estão sendo executados. O padrão é **false**. Consulte [comentários](#bk_ApplyRemark) para obter mais informações. 
    
  Se qualquer aplicativo do Office estiver em execução quando a ação de **Aplicar** é acionada, a ação de **Aplicar** geralmente falhará. Passando `forceappshutdown=true` para **Aplicar** o método causará o serviço **OfficeClickToRun** imediatamente desligar os aplicativos e aplicar a atualização. Nesse caso, o usuário pode enfrentar perda de dados. 
    
#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|**S_OK** <br/> |Ação foi enviada com êxito para o serviço de Click-To-Run para execução.  <br/> |
|**E_ACCESSDENIED** <br/> |O chamador não está sendo executado com privilégios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Parâmetros inválidos foram passados.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Ação não é permitida neste momento. Consulte [comentários](#bk_ApplyRemark) para obter mais informações.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Comentários

- Se qualquer aplicativo do Office estiver em execução quando a ação de **Aplicar** é acionada, a ação de **Aplicar** falhará. Passando `forceappshutdown=true` para **Aplicar** o método causará o serviço **OfficeClickToRun** para serem desligados imediatamente quaisquer aplicativos do Office que estão funcionando e aplicam a atualização. O usuário perceba dados conforme eles não serão solicitados a salvar as alterações para abrir documentos do.. 
    
- Essa ação só pode ser acionada quando o status de COM é um destes procedimentos: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Se você chamar o método **Apply** sem fazer o download de conteúdo anteriormente, o método **Apply** informará **Succeeded** como ela detectada nada a aplicar e o processo de **Aplicar** for concluído com êxito. 
    
### <a name="cancel"></a>Cancelar

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|S_OK  <br/> |Ação foi enviada com êxito para o serviço de Click-to-Run para execução.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Ação não é permitida neste momento. Consulte a seção [comentários](#bk_CancelRemarks) para obter mais informações  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Comentários

- Este método só pode ser acionado quando o de id de status COM **eDOWNLOAD_WIP**. Ele tentará cancelar a ação de download atual. O status de COM será altere para **eDOWNLOAD_CANCELLING** e eventualmente para **eDOWNLOAD_CANCELED**. O status COM retornará **E_ILLEGAL_METHOD_CALL** se disparado em qualquer outro momento. 
    
### <a name="download"></a>Baixar

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parâmetros

-  _displaylevel_: **true** para mostrar o status de instalação, incluindo erros, durante o processo de atualização; **false** para ocultar o status de instalação, incluindo erros, durante o processo de atualização. O padrão é **false**.
    
-  _updatebaseurl_: URL para a fonte de download alternativo.
    
-  _updatetoversion_: A versão para atualizar o Office. Defina esse parâmetro se você deseja atualizar para uma versão mais antiga do que a versão está instalada no momento.
    
-  _downloadsource_: CLSID da implementação **IBackgroundCopyManager** personalizada (Gerenciador de BITS). 
    
-  _contentid_: identifica o conteúdo para download do servidor de conteúdo por meio do Gerenciador de BITS personalizado. Esse valor é passado por meio da interface de BITS para interpretação.
    
#### <a name="return-results"></a>Retornar resultados

|||
|:-----|:-----|
|**S_OK** <br/> |Ação foi enviada com êxito para o serviço de Click-To-Run para execução.  <br/> |
|**E_ACCESSDENIED** <br/> |O chamador não está sendo executado com privilégios elevados.  <br/> |
|**E_INVALIDARG** <br/> |Parâmetros inválidos foram passados.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Ação não é permitida neste momento. Consulte [comentários](#bk_DownloadRemark) para obter mais informações.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Comentários

- Você deve especificar _downloadsource_ e _contentid_ como um par. Caso contrário, o método **Baixar** retornará um erro **E_INVALIDARG** . 
    
- Se forem fornecidos _downloadsource_, _contentid_e _updatebaseurl_ , _updatebaseurl_ será ignorado. 
    
- Essa ação só pode ser acionada quando o status de COM é um destes procedimentos: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Se você chamar o método **Apply** sem conteúdo baixado anteriormente, o método **Apply** informará **Succeeded** como ela detectada nada a aplicar e o processo de **Aplicar** for concluído com êxito. 
    
#### <a name="examples"></a>Exemplos

- Para baixar o conteúdo do Gerenciador de BITS personalizado: chamar a função de **download ()** , passando os seguintes parâmetros: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Para baixar o conteúdo da Microsoft CDN: chamar a função de **download ()** sem especificar os parâmetros _downloadsource_, _contentid_ou _updatebaseurl_ . 
    
- Para baixar o conteúdo de um local personalizado: chamar a função de **download ()** , passando o parâmetro a seguir: 
    
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
|**S_OK** <br/> |O método **Status** sempre retorna este resultado. Inspecione o `UPDATE_STATUS_RESULT` estrutura para o status da ação atual.  <br/> |
   
#### <a name="remarks"></a>Comentários

- O campo status do `UPDATE_STATUS_REPORT` contém o status da ação atual. Um dos seguintes valores de status é retornado: 
    
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

- Se o último comando resultou em um erro, o campo de erro do `UPDATE_STATUS_REPORT` contém informações detalhadas sobre o erro. Dois tipos de códigos de erro são retornados pelo método **Status** . 
    
- Se o erro menor que `UDPATE_ERROR_CODE::eUNKNOWN`, o erro é um dos seguintes códigos de erro predefinidas:
    
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

  Se o código de erro de retorno for maior que `UDPATE_ERROR_CODE::eUNKNOWN` é o **HRESULT** de uma chamada de função com falha. Para extrair o HRESULT subtrair `UDPATE_ERROR_CODE::eUNKNOWN` do valor retornado no campo de erro o `UPDATE_STATUS_REPORT`.
    
  A lista completa dos valores de status e de erro pode ser exibida por meio da biblioteca de tipos do **IUpdateNotify** incorporada OfficeC2RCom.dll inspeção. 
    
- O campo contentid é usado nas chamadas ao **Status** depois que **Baixar** iniciou e retorna contentid que foi passado para a chamada de **Download** . É uma prática recomendada para inicializar este campo como **Nulo** antes de chamar o método de **Status** e verifique se o valor depois que o **Status** foi retornado. Se o valor ainda for **nula**, isso significa que não há nenhuma contentid para retornar. Se o valor não for **nula**, você precisará liberá-la com uma chamada para **SysFreeString()**. Aqui está um trecho de código de como chamar **Status** após **Baixar**.
    
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

> [!NOTE]
> Esse resumo é fornecido como um info complemento aos [aplicativos de capacidade de gerenciamento de integração com o instalador de clique para executar do Office 365](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx). Depois que o doc pública for atualizada, este doc pode ser considerado como obsoleta. 
  
De C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (primeira compilação publicamente disponível deve ser a compilação de bifurcação junho – 8326.*) adicionamos uma nova interface **IUpdateNotify2** . Eis algumas informações básicas sobre essa interface: 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Essa interface também hospedado a interface IUpdateNotify original para fornecer compatibilidade com versões anteriores. O que significa que se você usar essa interface, você tem acesso a todos os métodos fornecidas na interface **UpdateNotifyObject** . 
    
- Novos métodos são adicionados ao IUpdateNotify2:
    
  - **HRESULT** GetBlockingApps (BSTR [out] \* AppsList). Obtenha atualizações bloqueando a lista de aplicativos. Essa chamada retornará executando aplicativos do Office que bloqueiam o processo de atualização de prosseguir. 
    
  - **HRESULT** GetOfficeDeploymentData (dataType int, pcwszName **LPCWSTR** , BSTR [out] [in] [in] * OfficeData). Obtenha os dados de implantação do Office. 
    
- Se desejar usar os métodos de novos, você precisa certificar-se:
    
  - Sua versão C2R é mais recente que a compilação acima (\>= compilação de bifurcação de junho).
    
  - Use UpdateNotifyObject2, em vez de **UpdateNotifyObject** para chamar **CoCreateInstance**.
    
Se você não usar qualquer um dos métodos novos, você não precisará alterar nada. Todos os métodos existentes funcionará como exato da mesma maneira que antes.
  
## <a name="implementing-the-bits-interface"></a>Implementando a interface de BITS

O [Serviço de transferência inteligente de plano de fundo](https://msdn.microsoft.com/en-us/library/bb968799(v=vs.85).aspx) (BITS) é um serviço oferecido pela Microsoft para transferir arquivos entre um cliente e servidor. BITS é um dos canais que instalador Click-To-Run do Office pode usar para baixar o conteúdo. Por padrão, o Office Click-To-Run instalador usa as janelas criada na implementação de BITS para baixar o conteúdo da CDN. 
  
Fornecendo uma implementação personalizada de BITS para o método **download ()** da interface **IUpdateNotify** , seu software gerenciabilidade pode controlar onde e como o cliente baixa o conteúdo. Uma interface de BITS personalizada é útil quando fornecendo um canal de distribuição de conteúdo personalizados que não seja os canais internos Click-to-Run, como a CDN do Office, servidores do IIS, ou compartilhamentos de arquivos. 
  
O requisito mínimo para uma interface de BITS personalizada funcionar com o serviço Office C2R é:
  
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

- Para o `Addfile` e `AddFileWithRanges` funções, a URL remota está no seguinte formato: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits é codificada e significa BITS personalizadas.
    
  -  _ \<contentid\> _ é o parâmetro _contentid_ o método **download ()** . 
    
  -  _ \<caminho relativo para o arquivo de destino\> _ fornece o local e o nome do arquivo para baixar. 
    
    Por exemplo, se você tiver fornecido um _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` para o **download ()** quiser baixar o arquivo cab de versão, tais como método e Office C2R `v32.cab` arquivo, ele chamará **AddFile()** com as seguintes `RemoteUrl`:
    
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

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/en-us/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/en-us/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="http://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a>Automatizando o preparo de conteúdo

Os administradores de TI podem optar por ter habilitados para receber automaticamente atualizações quando eles estão disponíveis diretamente da Microsoft conteúdo entrega rede (CDN) ou eles podem escolher para controlar a implantação das atualizações disponíveis da atualização de clientes de desktop canais usando a ferramenta de implantação do Office ou o System Center Configuration Manager.
  
O serviço suporta a capacidade de ferramentas de gerenciamento reconhecer e automatizar o download do conteúdo quando atualizações são disponibilizadas.
  
**A imagem a seguir está uma visão geral de download de uma imagem personalizada**

![Um diagrama de usar a interface COM no installer Office Click-To-Run.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Um diagrama de usar a interface COM no installer Click-To-Run do Office")
  
### <a name="overview-of-downloading-a-custom-image"></a>Visão geral de download de uma imagem personalizada
  
No diagrama anterior, você vê que uma nova imagem do Office 365 ProPlus está disponível na rede de distribuição conteúdo do Office (CDN). Junto com a imagem do Office 365 ProPlus, uma lista de arquivo no formato XML também está disponível que tem as informações necessárias para habilitar o software de capacidade de gerenciamento criar diretamente imagens personalizadas, substituindo a necessidade de usando a ferramenta de implantação do Office.
  
Uma empresa configura seu WSUS para sincronizar as atualizações do cliente do Office 365. Essas atualizações não contêm a carga de imagem real, mas permitir que o software de gerenciabilidade reconhecer quando o conteúdo novo está disponível. O software de capacidade de gerenciamento, em seguida, pode ler os metadados de atualização do cliente para entender qual versão do Office que a atualização se aplica ao.
  
Se a atualização for aplicável, o software de capacidade de gerenciamento pode usar o conteúdo CDN e a lista de arquivos para criar a imagem personalizada e armazená-lo para o local de compartilhamento de arquivo que ele está configurado para usar.
  
### <a name="format-of-the-xml-file-list"></a>Formato da lista de arquivo XML

Há duas listas de arquivos disponíveis em um arquivo cab na CDN. Uma lista os arquivos para a versão de 32 bits do Office e outro para a versão de 64 bits do Office. A URL do local da lista de arquivos Office (OFL. Arquivo CAB) é [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). As listas de dois arquivos são chamadas:
  
- O365Client_32bit.XML
    
- O365Client_64bit.XML
    
Dentro do XML para cada do arquivo listas é um <UpdateFiles> nó que contém um atributo version.  `<UpdateFiles version="1.4">`. Esta versão é incrementada se alterações forem feitas para as listas de arquivos.
  
Há dois parâmetros que precisam ser combinado com o XML para tornar uma imagem personalizada: 
  
- Substitua *% % de versão* a versão de compilação do Office. Isso pode ser derivado dos metadados de atualização do cliente (explicado na próxima seção). 
    
- Defina *baseURL* usando-se o valor da URL associado a ramificação que a imagem está sendo criada para. Isso é derivado dos metadados de atualização do cliente, explicado na seção a seguir. 
    
As etapas para a criação de uma imagem são:
  
1. Abra a lista de arquivo XML.
    
2. Substitua ocorrências de *% versão %* com a versão de compilação do Office aplicável. A versão de compilação pode ser adquirida no releasehistory.xml, conforme descrito neste artigo. 
    
3. Leia o atributo de URL para a ramificação de destino.
    
4. Remova nós de idioma para qualquer idiomas não obrigatório a imagem personalizada.
    
   > [!NOTE]
   > Nós com idioma = '0' são de idioma neutro e deve ser incluído na imagem. 
  
5. Construa uma imagem de local da CDN iteração entre a lista de arquivos XML e copiando os arquivos CDN, ao criar a estrutura de pasta, conforme necessário. 
    
   - Se o atributo *Renomear* for fornecido, em seguida, o arquivo copiado para o valor *Renomear* fornecidos no atributo renomear. Isso é usado para criar o padrão de nível superior arquivos v64.cab e v32.cab. Estas são as versões renomeadas do arquivo cab de compilação de nível superior e são usadas como a versão de instalação padrão, se a versão não for especificada. 
    
   - Use URL + relativePath + filename para construir o local CDN.
    
A seguir estão exemplos que usam o canal mensal (conforme definido pelo `<baseURL>` nó) e versão 16.0.4229.1004 do releasehistory.xml de compilação. 
  
```xml
<baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- A seguir está um arquivo de idioma neutro necessário para todos os idiomas. O nome do arquivo é v64_16.0.4229.1004.cab e ele deve ser copiado de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` e renomeado para `…/office/data/v64.cab`. 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- A seguir é um arquivo a ser incluído na imagem en-US designado pelo LCID do idioma = 1033. O nome do arquivo é s641033.cab e ele deve ser copiado de `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` e não foi renomeado.
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a>Verificação de hash dos arquivos. dat

Ferramentas de criação de imagem podem verificar a integridade dos arquivos. dat baixado comparando um valor HASH calculado com o valor HASH fornecido associado a cada um dos arquivos. dat. A seguir está um exemplo de um arquivo. dat do canal mensal com a versão de compilação 16.0.4229.1004 e idioma definido como búlgaro:
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- O atributo **hashLocation** Especifica o local de caminho relativo da stream.x64.bg-bg.hash para o arquivo stream.x64.bg-bg.dat. Construa o local do arquivo de hash concatenando a URL + relativePath + hashLocation. No exemplo a seguir, o local de stream.x64.bg-bg.hash seria: 
    
  ```http
  http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- O atributo **hashAlgo** Especifica qual algoritmo de hash foi usado. Nesse caso, Sha256 foi usada. 
    
  Para validar a integridade do arquivo stream.x64.bg-bg.dat, abra o stream.x64.bg-bg.hash e ler o valor HASH que é a primeira linha do texto no arquivo de hash. Compare com o valor de hash computados (usando o algoritmo de hash especificado) para verificar a integridade do arquivo. dat baixado.
    
  O exemplo a seguir mostra o código c# para ler o hash.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a>Atualizações de cliente do Office 365

Todas as atualizações de cliente do Office 365 são publicadas para o [Catálogo do Microsoft Update](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Atualizações de cliente do Office 365 habilitar software gerenciabilidade tratar as atualizações do cliente do Office 365, de maneira muito semelhante a qualquer outra atualização WU com uma exceção; as atualizações do cliente não contêm uma carga real. As atualizações do cliente do Office 365 não deve ser instaladas em todos os clientes mas preferência seja usadas para acionar os fluxos de trabalho com o software de capacidade de gerenciamento, substituindo o comando de instalação com o COM base em mecanismo de instalação mostrado acima. 
  
**A figura a seguir mostra um diagrama do fluxo de trabalho de atualização de cliente do Office 365.**

![Diagrama de fluxo de trabalho para atualizações do cliente O365PP.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de fluxo de trabalho para atualizações do cliente O365PP")
  
Cada Office 365 cliente atualização publicado inclui metadados sobre a atualização. Esses metadados incluem um parâmetro chamado *MoreInfoUrl* que pode ser usado para derivar as seguintes informações: 
  
-  *Ver*: identifica a versão do Office associada com essa atualização. 
    
-  *Filial*: identifica o canal de atualização para essa atualização. Os valores incluem InsiderFast, internas, mensalmente, multidifusão, amplos. Valores adicionais podem ser adicionados no futuro. 
    
-  *Forma arco*: identifica a arquitetura de processador associada a essa atualização. 
    
-  *xmlVer*: A versão das listas de arquivo XML que deve ser usado para construir a imagem base para esta atualização. 
    
-  *xmlPath*: caminho para o OFL. Lista de arquivo CAB que contém o arquivo XML. 
    
-  *mlFile*: O nome da lista de arquivos que deve ser usado para esta atualização. O valor será O365Client_32bit ou O365Client_64bit e isso coincidirá com a forma de arco. 
    
A URL a seguir está um exemplo do parâmetro *MoreInfoURL* que refere-se para as versões de atualização de cliente do Office 365 para a versão de 32 bits do Office com a versão de compilação do 16.0.2342.2343 no canal atual. 
  
http://officecdn.microsoft.com/pr/wsus/ofl.cabé o local das listas de arquivo XML para essa atualização, especificamente o O365Client_32bit.xml de dentro do OFL. CAB.
  
[Liberações de canal de atualização de cliente Office 365](http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a>Metadados adicionais para automatizar a preparação de conteúdo

Além de metadados que é publicado que define lá também são arquivos adicionais do XML publicados para o CDN que pode ajudar a fornecer informações adicionais sobre os clientes do Office 365 estão disponíveis a partir do CDN do Office.
  
**SKUS. XML**
  
Este arquivo XML contido em um CAB assinado e publicado para o CDN Office na seguinte URL: [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).
  
Os metadados publicado nesse arquivo XML são útil para determinar quais produtos estão disponíveis para implantação e manutenção da CDN Office junto com várias opções para cada um. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

** \<ReleaseInfo\> ** nó raiz contém o atributo de PublishedDate que identifica a data em que este arquivo foi publicado. 
  
** \<SKU\> ** nó identifica um SKU individual. 
  
- O atributo *ProductID* identifica a ID que é passada como atributo ID no Configuration se estiver usando a ODT. Por exemplo, `<Product ID="O365ProPlusRetail">`. 
    
- O *padrão* de atributo, se definido como verdadeiro, identifica a SKU recomendada. 
    
** \<App\> ** nós são usados para definir os aplicativos individuais do Office que ofereça suporte a cada SKU. 
  
- O atributo *Name* é o nome do aplicativo exibido. 
    
- O *AppID* é o atributo ID passado do Configuration. XML para o ** \<ExcludeApp\> ** nó se estiver usando a ODT. Por exemplo, `<ExcludeApp ID="Publisher" />`. 
    
**RELEASEHISTORY. XML**
  
Este arquivo XML contido em um CAB assinado e publicado para o CDN do Office no seguinte local: [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab). 
  
Os metadados publicado nesse arquivo XML são útil para determinar quais canais são suportados para a manutenção de atualizações de CDN do Office, juntamente com informações sobre o histórico de compilação para cada um dos canais com suporte.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

O ** \<ReleaseHistory\> ** nó raiz contém o atributo de PublishedDate que identifica a data em que este arquivo foi publicado. 
  
O ** \<UpdateChannel\> ** nó define um canal com suporte. 
  
- *Nome* do atributo define a ID do canal que é utilizada para passar para a ODT no Configuration como o atributo de canal. 
    
  Exemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">` 
    
  > [!NOTE] 
  > Este atributo foi preterido e é usado apenas para compatibilidade com versões anteriores. Use o atributo ID no lugar do atributo Name. 
    
- O atributo *ID* define a ID do canal que é utilizada para passar para a ODT no Configuration como o atributo de canal. 
    
  Exemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">` 
    
- O atributo **DisplayName** é usado como o nome para exibição. 
    
O ** \<atualizar\> ** nó é usado para definir cada atualização que tenha sido publicada para o canal em particular. 
  
- Atributo o **mais recente** , se definido como verdadeiro, define a versão que é a versão mais recente para esse canal. 
    
- O atributo **Version** define o número de versão para essa atualização específica. 
    
- O atributo **LegacyVersion** define o número de versão completa para essa atualização específica. 
    
- O atributo **Construir** define o número de compilação para essa atualização específica. 
    
- O atributo **PubTime** define a data e hora em que essa atualização foi publicada para o CDN do Office. 
    

