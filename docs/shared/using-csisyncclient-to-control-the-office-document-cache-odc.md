---
title: Usando CSISyncClient para controlar o Cache de Documentos do Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Saiba como usar CSISyncClient para controlar o Cache de Documentos do Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346253"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Usando CSISyncClient para controlar o Cache de Documentos do Office (ODC)

Saiba como usar o CSISyncClient para controlar o Cache de Documentos do Office (ODC).
  
CSISyncClient é um servidor COM fora do processo (CsiSyncClient.exe) que permite ao Microsoft OneDrive controlar o comportamento do Cache de Documentos do Office (ODC). Por exemplo, o OneDrive pode chamar o ODC via CSISyncClient para carregar e baixar arquivos de e para pontos de extremidade habilitados do MS-FSSHTTP. Isso permite recursos avançados com suporte no serviço do Office, como coautoria e transições perfeitas de offline para online.
  
CsiSyncClient está disponível na área de trabalho do Office (x86 e x64). Observação: embora as versões mais recentes do Office possam ser fornecidas com CsiSyncClient, o processo será usado apenas para compatibilidade com versões anteriores. A interface CsiSyncClient e a metodologia de controle do ODC mudarão em versões futuras do Office.
  
No momento, a ID de classe está definida para responder somente ao OneDrive.
  
O objeto COM pode ser usado como um servidor COM fora do processo e é executado CsiSyncClient.exe. Devido a limitações com o Access (que o ODC usa), ele acompanha o tipo de bit que o Office entra, portanto, o Office x64 significa um objeto COM x64 ou x86 Office significa um objeto COM x86. Para se deparar com essa limitação, especificar o CLSCTX_LOCAL_SERVER como parte do CoCreateInstance fará com que o objeto COM seja hospedado como um servidor COM fora do processo, permitindo a compatibilidade de bits cruzados.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient usa as interfaces a seguir.
  
### <a name="interface-ilsclocalsyncclient"></a>Interface ILSCLocalSyncClient

Esta é a interface principal usada para sincronizar arquivos no Office.
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
O objeto COM exposto é usado como um servidor fora do processo. Especificar CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite a compatibilidade entre processos de 64 e 32bits.
  
Depois de criar o objeto COM em coautor, você DEVE chamar [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) primeiro. Depois [que ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) for concluído com êxito, você poderá chamar qualquer API com a frequência que desejar e em qualquer ordem. Você também pode chamar [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) em um objeto já inicializado, mas isso não faz nada. 
  
As exceções ao parágrafo anterior são [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) e [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Depois de chamar [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) no objeto COM, você DEVE destruir esse objeto e criar um novo. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) excluirá seu subcache, excluirá todas as informações de arquivo associadas no cache, mas deixará os documentos no disco. Ele também deixa o estado intacto para comunicação com o cache. Isso permite que você chame [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) novamente para criar um novo cache sem ter que destruir e recriar o objeto COM. 
  
**Funções de membro público**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile é usado para remover as informações do arquivo do cache. No entanto, esse método deixará o arquivo associado no disco e no servidor.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
A cadeia de caracteres que identifica a ResourceID do arquivo. Esse valor deve não estar vazio com um máximo de 128 caracteres. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |A ResourceID determinada não está no cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |A inicialização não foi chamada com êxito no passado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo está sincronizando ou aberto no momento e não pode ser excluído.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges retorna um enumerador de objetos ILSCEvent e também retorna um token que é dado à próxima chamada para GetChanges, supondo que o consumidor tenha processado o conjunto anterior de eventos. Eventos antes do  _nPreviousChangesToken_ especificado serão excluídos e indisponíveis. Se não houver eventos a serem processados,  _pnCurrentChangesToken_ deverá ter o mesmo valor que  _nPreviousChangesToken_, mas  _ppiEvents_ ainda será definido. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parâmetros

 _nPreviousChangesToken_
  
Identifica qual evento foi processado pela última vez pelo consumidor. 
  
 _pnCurrentChangesToken_
  
Identifica o evento mais recente que está sendo entregue ao consumidor. Não deve ser nulo.
  
 _ppiEvents_
  
Um enumerador para os eventos entregues ao consumidor. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission é usado para consultar se a heurística de sincronização do Office para custo de rede e uso de energia foi substituído. Quando estiver em uma rede 3G ou outra rede de alto custo, ou quando estiver funcionando com bateria ou conectado, o Office poderá optar por bloquear o tráfego de rede até um horário mais adequado.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parâmetros

 _nspType_
  
Um sinalizador que define qual heurística de custo será consultada. Consulte [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Especifica se a heurística de custo solicitado está atualmente substituído ou não. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus é usado para coletar informações para um arquivo específico: se ele existe no cache, se tem comunicação pendente com a cópia do servidor e se o Office 2013 tem os dados mais atualizados da cópia local. Ele exige um sinalizador bit a bit dos valores [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar quais informações o objeto COM CsiSyncClient deve consultar. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
A cadeia de caracteres que identifica o arquivo no cliente. Esse valor deve não estar vazio, com um máximo de 128 caracteres. 
  
 _sfRequestedStatus_
  
Um sinalizador que define quais informações retornar. Consulte [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
A cadeia de caracteres que identifica o local do arquivo identificado por  _bstrResourceID_ no cliente. Não deve ser nulo. 
  
 _pbstrETag_
  
Uma cadeia de caracteres que conterá a eTag para o arquivo identificado por  _bstrResourceID_. Não deve ser nulo. 
  
 _psfFileStatus_
  
Um sinalizador que conterá o status solicitado via  _sfRequestedStatus_ para o arquivo identificado por  _bstrResourceID_. Não deve ser nulo. Consulte [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |As informações de arquivo especificadas  _por bstrResourceID_ não existem no cache.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged foi solicitado ou o arquivo especificado por  _bstrResourceID_ está bloqueado ou ausente.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions retorna uma lista de extensões de arquivo delimitadas por pipe que atualmente são suportadas pelo objeto COM CsiSyncClient. Observe que essa lista pode mudar e o consumidor será notificado sobre uma alteração por meio do objeto IPartnerActivityCallback fornecido no [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (consulte EventOccured). 
  
Um exemplo da cadeia de caracteres retornada é o seguinte: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parâmetros

 _pbstrSupportedFileExtensions_
  
Uma cadeia de caracteres a ser definida com um conjunto delimitado por pipe de extensões de arquivo com suporte pelo objeto COM CsiSyncClient. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

A inicialização deve ser o primeiro método chamado. Caso contrário, todas as outras APIs retornarão E_LSC_NOTINITIALIZED. Chamar Initialize em um objeto já inicializado retorna S_OK e não faz nada. Se E_LSC_CACHEMISMATCH for retornado, o chamador poderá chamar [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para excluir o cache associado ao SuppliedID fornecido. No entanto, nesse caso, outras APIs ainda retornarão E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parâmetros

 _bstrSuppliedID_
  
Identifica o consumidor e qual cache usar. Deve ser não vazio com um máximo de 32 caracteres. 
  
 _bstrProgID_
  
Identifica o objeto COM do consumidor para comunicação de duas vias. Deve ser não vazio com um máximo de 39 caracteres. Consulte [ \< ProgID \> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obter mais informações sobre ProgIDs. 
  
 _bstrFileSystemDirectoryHint_
  
Identifica a raiz do diretório na qual os arquivos locais serão armazenados. Deve ser não vazio com um máximo de 256 caracteres. O diretório já deve existir. 
  
 _pEventCallback_
  
A interface de retorno de chamada que o CsiSyncClient notificará sobre alterações. Consulte IPartnerActivityCallback::EventOccurred. Esse valor não deve ser nulo. 
  
 _pfCreatedNewCache_
  
Retorna se um novo cache foi criado. Se nenhum cache estiver associado ao SuppliedID, um será criado. Esse valor não deve ser nulo.
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Uma SuppliedID já tem um cache associado a ele, mas tem um ProgId ou FileSystemDirectoryHint diferente dos fornecidos.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |O FileSystemDirectoryHint (ou uma subpasta) já existe em um cache diferente.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |O ProgID já existe em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange é usado para dizer ao objeto COM CsiSyncClient para tentar carregar o arquivo especificado. O método preparará o arquivo para upload, incluindo a leitura do conteúdo atual do arquivo. Se um upload já estiver pendente, o carregamento anterior será descartado e o novo conteúdo será preparado para carregamento. Se o arquivo estiver aberto para edição em um aplicativo, esse método retornará S_OK sem preparar o arquivo para upload (o aplicativo já deve fazer essa etapa se houver alterações).
  
Esse método permitirá carregamentos se ele tiver sido marcado como uploads bloqueados anteriormente (consulte [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _bstrFileSystemPath_
  
Uma cadeia de caracteres que identifica o arquivo no cliente. Esse valor deve ser um caminho local não vazio com no máximo 256 caracteres. Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi feita. 
  
 _bstrResourceID_
  
Uma cadeia de caracteres que identifica a ResourceID do arquivo. Esse valor deve não estar vazio com um máximo de 128 caracteres. 
  
 _bstrWebPath_
  
Uma cadeia de caracteres que identifica o arquivo no servidor. Esse valor deve ser uma URL não vazia e válida, mas não mais do INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427 . 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O arquivo especificado por  _bstrFileSystemPath_ tem um ResourceID diferente do especificado. Um evento do tipo LSCEventType_OnFilePathConflict é enviado quando esse erro é retornado. Consulte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O arquivo foi excluído no meio da operação.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |A extensão de arquivo determinada não é suportada pelo objeto COM CsiSyncClient. Consulte [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |O objeto COM não programou um upload porque o arquivo no cache tinha as alterações mais recentes do disco.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |O arquivo especificado por  _bstrFileSystemPath_ está ausente ou bloqueado.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath determinado não está na raiz do diretório especificada pelo FileSystemDirectoryHint quando a chamada para Inicializar foi feita.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |O arquivo especificado por  _bstrResourceID_ tem um FileSystemPath diferente do especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado já tem alterações pendentes em um cache diferente e ainda não pode ser associado ao cache do consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |O WebPath fornecido se enquadra em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile associará uma nova URL e um caminho local para uma determinada ResourceID. Se o arquivo especificado pelo ResourceID ainda não existir no cache, será feita uma tentativa de criar e marcá-lo para download.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
Uma cadeia de caracteres que identifica a ResourceID do arquivo. Esse valor deve não estar vazio com um máximo de 128 caracteres. 
  
 _bstrNewFileSystemPath_
  
Uma cadeia de caracteres que especifica o novo caminho local para o arquivo. Esse valor deve ser um caminho local não vazio com no máximo 256 caracteres. Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para Inicializar foi feita. 
  
 _bstrNewWebPath_
  
Uma cadeia de caracteres que especifica a nova URL para o arquivo. Esse valor deve ser uma URL válida não vazia, mas não mais do que INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427 . 
  
 _fBlockUploads_
  
Especifica se os carregamentos para o novo local são permitidos no momento. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O  _bstrNewFileSystemPath_  _ou bstrNewWebPath_ já existem em outro arquivo em qualquer cache. Um evento do tipo LSCEventType_OnFilePathConflict é enviado quando esse erro é retornado. Consulte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |As informações do arquivo foram excluídas do cache enquanto esse método estava sendo executado.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath determinado não está na raiz do diretório especificada pelo FileSystemDirectoryHint quando a chamada para Inicializar foi feita.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado está sincronizando no momento em um aplicativo do Office.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

O ResetCache excluirá o cache associado ao SuppliedID fornecido em Initialize. Isso inclui todas as informações do arquivo, mas deixará os arquivos no cliente e no servidor. Esse método também deixa o objeto em um estado parcialmente não reinicializado. As únicas chamadas válidas depois disso são [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Esse método PODE ser chamado se Initialize falhar e retornar E_LSC_CACHEMISMATCH e excluirá o cache associado à SuppliedID que foi fornecida com a chamada com falha.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parâmetros

Nenhum
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange informa ao objeto COM CsiSyncClient para marcar o arquivo especificado para download. Se o arquivo estiver aberto em um aplicativo do Office para edição, esse método retornará S_OK sem marcar o arquivo para download (o aplicativo já deve realizar essa etapa se houver alterações).
  
Esse método permitirá downloads se tiver sido marcado como downloads bloqueados anteriormente (consulte RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Uma cadeia de caracteres que identifica o arquivo no cliente. Esse valor deve ser um caminho local não vazio com no máximo 256 caracteres. Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para Inicializar foi feita.  <br/> |
|bstrResourceID  <br/> |Uma cadeia de caracteres que identifica a ResourceID do arquivo. Esse valor deve não estar vazio com um máximo de 128 caracteres.  <br/> |
|bstrWebPath  <br/> |Uma cadeia de caracteres que identifica o arquivo no servidor. Esse valor deve ser uma URL válida não vazia, mas não mais do INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427 .  <br/> |
   
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao definir o estado de conectividade do cache.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O arquivo especificado por  _bstrFileSystemPath_ tem um ResourceID diferente do especificado.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |A extensão de arquivo determinada não é suportada pelo objeto COM CsiSyncClient. Consulte GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O arquivo foi excluído no meio da operação.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath determinado não está na raiz do diretório especificada pelo FileSystemDirectoryHint quando a chamada para Inicializar foi feita.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |O arquivo especificado por  _bstrResourceID_ tem um FileSystemPath diferente do especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado já tem alterações pendentes em um cache diferente e ainda não pode ser associado ao cache do consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |O WebPath fornecido se enquadra em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Define o cache em um estado online ou offline. Se estiver offline, o Office não tentará se comunicar com o servidor para arquivos nesse cache, independentemente da configuração  _fBlockUploads_ de cada arquivo individual. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parâmetros

 _fIsOnline_
  
Um booliana que determina o estado de conectividade do cache. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao definir o estado de conectividade do cache.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission é usado para substituir ou restaurar a heurística de sincronização doOffice para o custo de rede e o uso de energia. Quando estiver em uma rede 3G ou outra rede de alto custo, ou quando estiver funcionando com bateria ou conectado, o Office poderá optar por bloquear o tráfego de rede até um horário mais adequado. O consumidor dessa API pode usá-la para substituir a heurística do Office e forçar a sincronização a ocorrer.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parâmetros

 _nspType_
  
Um sinalizador que define qual heurística de custo substituir. Consulte [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Especifica se é necessário forçar a sincronização, substituindo assim essa heurística de custo ou não mais substituí-la. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao substituir a heurística de sincronização.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Descarrega o cache do objeto COM e executa operações de fechamento. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEVE ser chamado antes de destruir o objeto COM. Uma vez chamado, nenhuma outra APIs pode ser chamada, o objeto COM DEVE ser destruído e um novo criado se você deseja continuar as operações. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parâmetros

Nenhum.
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao não reinicializar.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interface IEnumLSCEvent

Essa interface representa uma lista de eventos ILSCEvent.
  
**Funções de membro público**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Recupera o próximo evento da lista de eventos.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parâmetros

 _ppiLSCEvent_
  
Um ponteiro para uma interface ILSCEvent.
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Não há mais eventos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Redefine o enumerador para o primeiro evento.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parâmetros

Nenhum.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
### <a name="interface-ilscevent"></a>Interface ILSCEvent

Essa interface representa um evento de sincronização. Todas as informações sobre o evento podem ser recuperadas da interface.
  
**Funções de membro público**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Observe que esse valor é preenchido quando [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) é chamado, não quando o evento foi criado, portanto, você terá apenas o status atual do arquivo, não o status do arquivo quando o status do conflito for alterado. 
  
Esse valor só é preenchido quando [a Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parâmetros

 _pfIsInConflict_
  
O status de conflito atual do arquivo associado ao evento.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Esse valor só é preenchido quando a [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parâmetros

 _pnError_
  
O erro associado a esse evento.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Esse valor só é preenchido quando a [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parâmetros

 _pbstrETag_
  
A ETag associada a esse evento
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Obtém o tipo desse evento.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parâmetros

 _pnEventType_
  
O tipo de evento deste evento. Consulte [Enum LSCEventType para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) valores válidos. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Obtém o caminho de trabalho local para este evento.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parâmetros

 _pbstrLocalWorkingPath_
  
O caminho local do arquivo ao qual esse evento pertence. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Obtém a ID de recurso do evento.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _pbstrResourceID_
  
ResourceID do arquivo associado a esse evento.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Esse valor só é preenchido quando [a Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnFilePathConflict. Quando uma chamada para [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causaria uma colisão de Caminho da Web ou Caminho Local com outro arquivo no cache de arquivos do Office, esse evento é gerado. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parâmetros

 _pbstrResourceIDAttempted_
  
O ResourceID que gerou esse evento. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Esse valor só é preenchido quando a [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parâmetros

 _pnSyncErrorType_
  
O tipo de erro associado a esse evento. Consulte [Enum LSCEventType para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) valores potenciais. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Esse valor só é preenchido quando [a Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parâmetros

 _pbstrWebPath_
  
Especifica o Caminho da Web associado a esse evento. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

Essa interface contém informações adicionais sobre um evento de sincronização.
  
**Funções de membro público**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Obtém as informações da cadeia de erros sobre um evento de sincronização.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parâmetros

 _pbstrErrorChain_
  
Uma cadeia de caracteres para manter as informações da cadeia de erros. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_NOTIMPL  <br/> |A versão instalada do Office não dá suporte a essa interface  <br/> |
|E_INVALIDARG  <br/> |Um ou mais dos valores de parâmetro são inválidos.  <br/> |
|E_FAIL  <br/> |As informações da cadeia de erros não estão disponíveis.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

Essa interface fornece uma função de retorno de chamada para o objeto COM CSISyncClient.
  
**Funções de membro público**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Esta é uma função de retorno de chamada no objeto dado ao objeto COM CsiSyncClient. Espera-se que, quando ocorrer um evento (consulte [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válidos), o objeto COM CsiSyncClient chamará esse método, sinalizando o consumidor. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parâmetros

 _eEventTypeOccurred_
  
O tipo de evento deste evento. Consulte [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para valores válidos. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK.
  
## <a name="enumerations"></a>Enumerações

CSISyncClient usa as enumerações a seguir.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Esta enumeração especifica as categorias de erros que podem ocorrer durante a sincronização de um arquivo.
  
|Enumerador|Descrição|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |O erro de sincronização desse evento foi inesperado e pode exigir uma consideração especial. Por padrão, o usuário pode ter que intervir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |O erro de sincronização desse evento não precisa de consideração especial. O Office lidará com ele automaticamente.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |O erro de sincronização desse evento requer que o usuário o resolva. Por exemplo, o erro de conflito de mesclagem requer que um usuário abra o documento e mescula-o.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |O erro de sincronização desse evento requer que o consumidor interaia, mas não deve exigir consideração especial pelo usuário.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |O erro de sincronização desse evento exige que o consumidor interaia como um caso especial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

Esta enumeração especifica o tipo de eventos que podem ocorrer para um arquivo específico.
  
|Enumerador|Descrição|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Foram feitas alterações em um arquivo local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Um usuário abriu um arquivo.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Terminei de baixar as alterações de arquivo do servidor.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Terminei de carregar as alterações de arquivo no servidor.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |O estado de conflito de mesclagem de um arquivo foi alterado.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Um arquivo foi adicionado.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Um arquivo foi excluído.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |A sincronização foi habilitada para os arquivos de um usuário.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Começou a baixar as alterações de arquivo do servidor.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Começou a carregar alterações de arquivo no servidor.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Esse evento é gerado quando uma chamada para [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causa uma colisão de caminho da Web ou caminho local com outro arquivo no cache de arquivos do Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Esta enumeração especifica o tipo de eventos que podem ocorrer. O consumidor precisa chamar funções ESPECÍFICAs ILSCLocalSyncClient com base no tipo de evento.
  
|Enumerador|Descrição|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ocorreu um ILSCEvent. O consumidor deve chamar [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar os dados.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |As extensões de arquivo com suporte foram alteradas. O consumidor deve chamar [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar a nova lista de extensões com suporte.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Esta enumeração especifica os sinalizadores usados para uma heurística de custo de rede. 

|Enumerador|Descrição|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True se a heurística de custo para redes caras (como 3G) for substituído.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True se a heurística de custo para uso de energia (como uma bateria) for substituído.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Essa enumeração é usada para representar o status de sincronização de um arquivo. 
  
|Enumerador|Descrição|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True se houver dados pendentes a enviar para o arquivo do servidor.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True se houver dados pendentes para baixar do arquivo do servidor.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True se os dados que o Office tem no arquivo em seu cache é a cópia mais recente dos dados no disco.  <br/> |
   

