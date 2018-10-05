---
title: Usando CSISyncClient para controlar o Cache de documentos do Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Aprenda a usar CSISyncClient para controlar o Cache de documentos do Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399449"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Usando CSISyncClient para controlar o Cache de documentos do Office (ODC)

Aprenda a usar CSISyncClient para controlar o Cache de documentos do Office (ODC).
  
CSISyncClient é um servidor COM limite de proc (CsiSyncClient.exe) que permite que o Microsoft OneDrive controlar o comportamento do Cache de documentos do Office (ODC). Por exemplo, o OneDrive pode chamar após o ODC via CSISyncClient para carregar e baixar arquivos de e para os pontos de extremidade do MS-FSSHTTP habilitado. Isso permite que o serviço reserva recursos avançados no Office, como transições de coautoria e contínuo de offline para online.
  
CsiSyncClient está disponível na área de trabalho do Office (x86 e x64). Observação: Embora versões mais recentes do Office podem ser enviados com CsiSyncClient, o processo será usado apenas para compatibilidade com versões anteriores. A interface de CsiSyncClient e a metodologia de controlar o ODC serão alterado em futuras versões do Office.
  
A ID de classe está atualmente definida responda apenas a OneDrive.
  
O objeto COM pode ser usado como um servidor de COM limite de proc e executa no CsiSyncClient.exe. Devido às limitações com acesso (que o ODC usa), ele é fornecido com o tipo de bit Office apresentarem, caso x64 Office significa uma x64 x86 ou objeto COM Office significa um x86 objeto COM. Para contornar esta limitação, especificando CLSCTX_LOCAL_SERVER como parte do CoCreateInstance terão o objeto COM sejam hospedados como um servidor fora do proc COM, permitindo cross-bitness compatibilidade.
  
## <a name="interfaces"></a>Interfaces

CSISyncClient usa as seguintes interfaces.
  
### <a name="interface-ilsclocalsyncclient"></a>Interface ILSCLocalSyncClient

Esta é a interface principal usado para sincronizar arquivos no Office.
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
O objeto COM que é exposto é usado como um servidor fora do processo. Especificando CLSCTX_LOCAL_SERVER como parte do CoCreateInstance permite a compatibilidade entre os processos de 32 bits e 64 bits.
  
Depois que você criou o objeto COM co, você deve chamar [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) primeiro. Depois de [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi concluída com êxito, você pode chamar qualquer API sempre que desejar e em qualquer ordem. Você também pode chamar [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) em um objeto já inicializado, mas isso não faz nada. 
  
As exceções para o parágrafo anterior são [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) e [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Depois de chamar [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) no objeto COM, você deve destruir esse objeto e crie um novo. [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) irá excluir sua subcache, excluir todas as informações do arquivo associado no cache, mas deixar os documentos no disco. Ele também deixa intacta para se comunicar com o cache o estado. Isso permite que você chamar [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) novamente para criar um novo cache sem precisar destrua e recriar o objeto COM. 
  
**Funções de membro público**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::DeleteFile

DeleteFile é usado para remover as informações do arquivo do cache. No entanto, esse método deixará o arquivo associado no disco e no servidor.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
A cadeia de caracteres que identifica o ResourceID do arquivo. Este valor deve ser não vazias com um máximo de 128 caracteres. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O ResourceID determinado não está no cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize não foi chamado com êxito no passado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo está sendo sincronizado ou abra e não podem ser excluídas.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges retorna um enumerador de objetos ILSCEvent e também retornará um token que é fornecido para a próxima chamada ao GetChanges, supondo que o consumidor tiver processado o conjunto de eventos anterior. Eventos antes do _nPreviousChangesToken_ especificado serão excluídos e indisponível. Se não houver nenhum evento a serem processados, _pnCurrentChangesToken_ deve ser o mesmo valor que _nPreviousChangesToken_, mas _ppiEvents_ ainda será definido. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parâmetros

 _nPreviousChangesToken_
  
Identifica qual evento última foi processado pelo consumidor. 
  
 _pnCurrentChangesToken_
  
Identifica o evento mais recente que está sendo entregue ao consumidor. Não deve ser nula.
  
 _ppiEvents_
  
Um enumerador para os eventos entregues ao consumidor. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission é usado para consultar se heurística de sincronização do Office de custo de rede e o uso de energia são substituídas. Quando em um 3G ou outra rede de alto custo, ou quando executando em bateria versus sendo conectado, o Office pode optar por bloquear o tráfego de rede até um momento mais oportunidade.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parâmetros

 _nspType_
  
Um sinalizador que define qual heurístico custo à consulta. Consulte [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Especifica se o heurístico custo solicitada no momento é substituído ou não. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus é usado para coletar informações para um arquivo específico: se ela existir no cache, se ele tiver pendentes comunicação com a cópia do servidor e se o Office 2013 tem o máximo até dados de data a partir da cópia local. Requer um sinalizador de bit a bit dos valores de [Enumeração LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar quais informações é o objeto COM CsiSyncClient consultar. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
A cadeia de caracteres que identifica o arquivo no cliente. Este valor deve ser não vazias, com um máximo de 128 caracteres. 
  
 _sfRequestedStatus_
  
Um sinalizador que define quais informações a serem retornadas. Consulte [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
A cadeia de caracteres que identifica a localização do arquivo identificado por _bstrResourceID_ no cliente. Não deve ser nula. 
  
 _pbstrETag_
  
Uma cadeia de caracteres que conterá a eTag do arquivo identificado por _bstrResourceID_. Não deve ser nula. 
  
 _psfFileStatus_
  
Um sinalizador que conterá o status solicitado por meio de _sfRequestedStatus_ para o arquivo identificado por _bstrResourceID_. Não deve ser nula. Consulte [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |As informações do arquivo especificadas por _bstrResourceID_ não existem no cache.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged foi solicitado ou o arquivo especificado por _bstrResourceID_ está bloqueado ou ausente.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions retorna uma lista delimitada de extensões de arquivo que são suportados atualmente pelo objeto CsiSyncClient COM. Observe que esta lista pode mudar e do consumidor serão notificado sobre uma alteração através do objeto IPartnerActivityCallback fornecida no [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (consulte EventOccured). 
  
Um exemplo da cadeia de caracteres retornada é o seguinte: "| docx | docm | pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parâmetros

 _pbstrSupportedFileExtensions_
  
Uma cadeia de caracteres a ser definido com um conjunto delimitada das extensões de arquivo compatíveis com o objeto COM CsiSyncClient. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize deve ser o primeiro método chamado. Caso contrário, todas as outras APIs retornará E_LSC_NOTINITIALIZED. Chamar Initialize em um objeto já inicializado Retorna S_OK e não faz nada. Se E_LSC_CACHEMISMATCH for retornado, o chamador pode chamar [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para excluir o cache associado a determinado SuppliedID. No entanto, nesse caso outras APIs ainda retornará E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parâmetros

 _bstrSuppliedID_
  
Identifica o consumidor e qual armazenar em cache para usar. Deve ser não vazias com um máximo de 32 caracteres. 
  
 _bstrProgID_
  
Identifica o objeto de COM do consumidor para comunicação bidirecional. Deve ser não vazias com um máximo de 39 caracteres. Consulte [ \<ProgID\> chave](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obter mais informações sobre ProgIDs. 
  
 _bstrFileSystemDirectoryHint_
  
Identifica o diretório raiz em que serão armazenados os arquivos locais. Deve ser não vazias com um máximo de 256 caracteres. O diretório já deve existir. 
  
 _pEventCallback_
  
A interface de retorno de chamada que CsiSyncClient receberá uma notificação sobre alterações. Consulte IPartnerActivityCallback::EventOccurred. Este valor não deve ser nula. 
  
 _pfCreatedNewCache_
  
Retorna se um novo cache foi criado. Se nenhum cache está associado com o SuppliedID, um será criado. Este valor não deve ser nula.
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Uma SuppliedID já tem um cache associado a ele, mas tem um ProgId diferente ou um FileSystemDirectoryHint que os fornecidos.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |O FileSystemDirectoryHint (ou uma subpasta) já existe em um cache diferente.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |O ProgID já existe em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange é usado para informar ao objeto COM CsiSyncClient para tentar carregar o arquivo especificado. O método preparará o arquivo para carregar, incluindo ler o conteúdo do arquivo atual. Se um carregamento já estiver pendente, o carregamento anterior será descartado e o novo conteúdo preparado para carregar. Se o arquivo está aberto para edição em um aplicativo, este método retornará S_OK sem preparar o arquivo para carregar (o aplicativo já faça esta etapa se há alterações).
  
Esse método permitirá que carregamentos se ela foi marcada como carrega bloqueado anteriormente (consulte [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _bstrFileSystemPath_
  
Uma cadeia de caracteres que identifica o arquivo no cliente. Este valor deve ser um caminho de local não vazias com um máximo de 256 caracteres. Esse caminho deve estar na árvore de pastas especificada pelo FileSystemDirectoryHint quando a chamada para [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi feita. 
  
 _bstrResourceID_
  
Uma cadeia de caracteres que identifica o ResourceID do arquivo. Este valor deve ser não vazias com um máximo de 128 caracteres. 
  
 _bstrWebPath_
  
Uma cadeia de caracteres que identifica o arquivo no servidor. Este valor deve ser uma URL não vazias, válida, mas não tenha mais de INTERNET_MAX_URL_LENGTH, conforme definido pela https://support.microsoft.com/kb/208427. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O arquivo especificado por _bstrFileSystemPath_ tem um ResourceID diferente do especificado. Um evento do tipo LSCEventType_OnFilePathConflict é enviada quando esse erro é retornado. Consulte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O arquivo foi excluída operação intermediário.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Não há suporte para a extensão de arquivo fornecido pelo objeto CsiSyncClient COM. Consulte [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |O objeto COM não tenha agendado um carregamento porque o arquivo no cache tinha as alterações mais recentes do disco.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |O arquivo especificado por _bstrFileSystemPath_ está ausente ou bloqueado.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath determinado não está sob o diretório raiz especificado pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado já tem as alterações em um cache diferente pendentes e ainda não pode ser associado com o cache do consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |O WebPath fornecido cai em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile associará uma nova URL e o caminho local para um determinado ResourceID. Se o arquivo especificado pelo ResourceID ainda não existir no cache, será feita uma tentativa para criá-la e marcá-la para download.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
Uma cadeia de caracteres que identifica o ResourceID do arquivo. Este valor deve ser não vazias com um máximo de 128 caracteres. 
  
 _bstrNewFileSystemPath_
  
Uma cadeia de caracteres que especifica o novo caminho local para o arquivo. Este valor deve ser um caminho de local não vazias com um máximo de 256 caracteres. Esse caminho deve estar na árvore de pastas especificada pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita. 
  
 _bstrNewWebPath_
  
Uma cadeia de caracteres que especifica a nova URL para o arquivo. Este valor deve ser um URL válido do não vazias, mas não tenha mais de INTERNET_MAX_URL_LENGTH, conforme definido pela https://support.microsoft.com/kb/208427. 
  
 _fBlockUploads_
  
Especifica se carregamentos para o novo local são permitidos no momento. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O _bstrNewFileSystemPath_ ou _bstrNewWebPath_ já existir no outro arquivo em qualquer cache. Um evento do tipo LSCEventType_OnFilePathConflict é enviada quando esse erro é retornado. Consulte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |As informações do arquivo foi excluídas do cache enquanto este método estava em execução.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath determinado não está sob o diretório raiz especificado pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado está sendo sincronizado em um aplicativo do Office.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache excluirá o cache associado a SuppliedID que foi fornecido em Initialize. Isso inclui todas as informações do arquivo, mas deixará os arquivos no cliente e o servidor. Este método também deixa o objeto em um estado parcialmente não inicializado. As chamadas válidas somente depois de fazer isso são [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Este método pode ser chamado se Initialize falha e retorna E_LSC_CACHEMISMATCH e excluirá o cache associado a SuppliedID que foi fornecido com a chamada está falhando.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parâmetros

Nenhum
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha na chamada.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange informa ao objeto COM CsiSyncClient para marcar o arquivo especificado para download. Se o arquivo está aberto em um aplicativo do Office para edição, este método retornará S_OK sem marcar o arquivo para download (o aplicativo já faça esta etapa se há alterações).
  
Esse método permitirá que downloads se ela foi marcada como downloads bloqueado anteriormente (consulte RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Uma cadeia de caracteres que identifica o arquivo no cliente. Este valor deve ser um caminho de local não vazias com um máximo de 256 caracteres. Esse caminho deve estar na árvore de pastas especificada pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.  <br/> |
|bstrResourceID  <br/> |Uma cadeia de caracteres que identifica o ResourceID do arquivo. Este valor deve ser não vazias com um máximo de 128 caracteres.  <br/> |
|bstrWebPath  <br/> |Uma cadeia de caracteres que identifica o arquivo no servidor. Este valor deve ser uma URL válida não vazias, mas não tenha mais de INTERNET_MAX_URL_LENGTH, conforme definido pela https://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha para definir o estado de conectividade do cache.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O arquivo especificado por _bstrFileSystemPath_ tem um ResourceID diferente do especificado.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Não há suporte para a extensão de arquivo fornecido pelo objeto CsiSyncClient COM. Consulte GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O arquivo foi excluído em operação intermediário.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath determinado não está sob o diretório raiz especificado pelo FileSystemDirectoryHint quando a chamada para inicializar foi feita.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado já tem as alterações em um cache diferente pendentes e ainda não pode ser associado com o cache do consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |O WebPath fornecido cai em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Define o cache em um estado online ou offline. Se estiver offline, Office não tentará se comunicar com o servidor de arquivos nesse cache, independentemente da configuração de _fBlockUploads_ de cada arquivo individual. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parâmetros

 _fIsOnline_
  
Um Booleano determinando o estado de conectividade do cache. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha para definir o estado de conectividade do cache.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission é usado para qualquer substituição ou heurística de sincronização do restoreOffice para uso de custo e alimentação de rede. Quando em um 3G ou outra rede de alto custo, ou quando executando em bateria versus sendo conectado, o Office pode optar por bloquear o tráfego de rede até um momento mais oportunidade. O consumidor desse API pode ser usada para substituir heurística do Office e forçar sincronizando para que ela ocorra.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parâmetros

 _nspType_
  
Um sinalizador que define qual heurístico custo substituir. Consulte [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Especifica se é para forçar a sincronização on, substituindo assim que heurístico custo ou não são mais substituí-la. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao substituir heurísticos de sincronização.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Descarrega o cache do objeto COM e realizar operações de fechamento. [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEVE ser chamado antes destruir o objeto COM. Depois que a chamada, outras APIs não pode ser chamados, o objeto COM deve ser destruído e um novo criada se você desejar operações contínuas. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parâmetros

Nenhum.
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha para reverter a.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não tiver sido chamado com êxito no passado.  <br/> |
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
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Não existem mais eventos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Redefine o enumerador para o primeiro evento.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parâmetros

Nenhum.
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
### <a name="interface-ilscevent"></a>Interface ILSCEvent

Essa interface representa um evento de sincronização. Todas as informações sobre o evento podem ser recuperadas da interface.
  
**Funções de membro público**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Observe que esse valor é preenchido quando [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) é chamado, não quando o evento tiver sido criado, portanto você terá somente o status atual do arquivo, não o status do arquivo quando o status de conflito alterado. 
  
Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parâmetros

 _pfIsInConflict_
  
O status atual de conflito do arquivo associado ao evento.
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parâmetros

 _pnError_
  
O erro associado ao evento.
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parâmetros

 _pbstrETag_
  
A ETag associada ao evento
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Obtém o tipo para este evento.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parâmetros

 _pnEventType_
  
O tipo de evento desse evento. Consulte [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para valores válidos. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Obtém o caminho local de trabalho para este evento.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parâmetros

 _pbstrLocalWorkingPath_
  
O caminho local do arquivo para o qual esse evento pertence. 
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Obtém a identificação do recurso para o evento.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _pbstrResourceID_
  
ResourceID do arquivo associado ao evento.
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnFilePathConflict. Quando uma chamada para [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) pode causar um conflito de caminho da Web ou caminho Local com outro arquivo no cache de arquivo do Office, isso evento ser gerado. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parâmetros

 _pbstrResourceIDAttempted_
  
O ResourceID que gerou esse evento obter gerado. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parâmetros

 _pnSyncErrorType_
  
O tipo de erro associado ao evento. Consulte [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para os valores possíveis. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Esse valor é preenchido somente quando o [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parâmetros

 _pbstrWebPath_
  
Especifica o caminho da Web associado ao evento. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK. 
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

Essa interface contém informações adicionais sobre um evento de sincronização.
  
**Funções de membro público**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Obtém as informações de cadeia de erro sobre um evento de sincronização.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parâmetros

 _pbstrErrorChain_
  
Uma cadeia de caracteres para armazenar as informações de cadeia de erro. Não deve ser nula. 
  
##### <a name="return-values"></a>Valores de retorno

|Valor|Descrição|
|:-----|:-----|
|E_NOTIMPL  <br/> |A versão instalada do Office não oferece suporte a essa interface  <br/> |
|E_INVALIDARG  <br/> |Um ou mais dos valores de parâmetro são inválidos.  <br/> |
|E_FAIL  <br/> |As informações de cadeia de erro não estão disponíveis.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

Essa interface fornece uma função de retorno de chamada para o objeto COM CSISyncClient.
  
**Funções de membro público**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Essa é uma função de retorno de chamada no objeto dado ao objeto CsiSyncClient COM. Espera-se que, quando ocorre um evento (consulte [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de evento válidos), o objeto CsiSyncClient COM chamará este método, o consumidor de sinalização. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parâmetros

 _eEventTypeOccurred_
  
O tipo de evento desse evento. Consulte [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para valores válidos. 
  
##### <a name="return-values"></a>Valores de retorno

Sempre retorna S_OK.
  
## <a name="enumerations"></a>Enumerações

CSISyncClient usa as enumerações a seguir.
  
### <a name="enum-lsceventsyncerrortype"></a>Enumeração LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Essa enumeração Especifica as categorias de erros que podem ocorrer durante a sincronização de um arquivo.
  
|Enumerador|Descrição|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |O erro de sincronização desse evento era esperado e pode exigir uma consideração especial. Por padrão, o usuário pode ter de intervir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |O erro de sincronização desse evento não precisa consideração especial. Office manipulará-lo automaticamente.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |O erro de sincronização desse evento exige que um usuário resolvê-lo. Por exemplo, o erro de conflito de mesclagem requer um usuário abrir o documento e mesclar a ele.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |O erro de sincronização desse evento exige que o consumidor intervir, mas não deve exigir uma consideração especial pelo usuário.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |O erro de sincronização desse evento requer o consumidor intervir como um caso especial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enumeração LSCEventType
<a name="Enum_LSCEventType"> </a>

Essa enumeração Especifica o tipo de eventos que podem ocorrer para um arquivo específico.
  
|Enumerador|Descrição|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Foram feitas alterações em um arquivo local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Um usuário abre um arquivo.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Download de alterações no arquivo do servidor concluído.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Concluir a carregar alterações no arquivo para o servidor.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |O estado de conflito de mesclagem de um arquivo foi alterada.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Um arquivo foi adicionado.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Um arquivo foi excluído.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Sincronizando foi habilitado para arquivos do usuário.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Iniciado o download de alterações de arquivo do servidor.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Iniciado carregar alterações no arquivo para o servidor.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Esse evento é gerado quando uma chamada para [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), ou [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) faz com que um conflito de caminho da Web ou caminho Local com outro arquivo no Cache de arquivos do Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enumeração LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Essa enumeração Especifica o tipo de eventos que podem ocorrer. O consumidor precisa chamar funções específicas de ILSCLocalSyncClient com base no tipo de evento.
  
|Enumerador|Descrição|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ocorreu uma ILSCEvent. O consumidor deve chamar [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar os dados.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |As extensões de arquivo com suporte foram alteradas. O consumidor deve chamar [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar a nova lista de extensões aceitas.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enumeração LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Essa enumeração Especifica os sinalizadores usados para uma heurística de custo de rede. 

|Enumerador|Descrição|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True se o heurístico custo para redes caros (por exemplo, 3G) será substituído.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True se o heurístico custo para o uso de energia (por exemplo, uma bateria) será substituído.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enumeração LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Esta enumeração é usada para representar o status de sincronização de um arquivo. 
  
|Enumerador|Descrição|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True se não houver pendentes dados a serem enviados para o arquivo do servidor.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True se não houver dados para fazer o download do arquivo server pendentes.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True se os dados do Office tem no arquivo no seu cache é a cópia mais recente dos dados no disco.  <br/> |
   

