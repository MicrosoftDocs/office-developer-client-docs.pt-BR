---
title: Usando o CSISyncClient para controlar o cache de documentos do Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Saiba como usar o CSISyncClient para controlar o cache de documentos do Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346253"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Usando o CSISyncClient para controlar o cache de documentos do Office (ODC)

Saiba como usar o CSISyncClient para controlar o cache de documentos do Office (ODC).
  
CSISyncClient é um servidor COM fora de processamento (CsiSyncClient. exe) que permite que o Microsoft OneDrive controle o comportamento do cache de documentos do Office (ODC). Por exemplo, o OneDrive pode chamar no ODC via CSISyncClient para carregar e baixar arquivos para e de pontos de extremidade habilitados para MS-FSSHTTP. Isso permite recursos avançados de suporte de serviço no Office, como transições de coautoria e sem interrupções de offline para online.
  
O CsiSyncClient está disponível na área de trabalho do Office (tanto x86 quanto x64). Observação: embora as versões mais recentes do Office possam ser fornecidas com o CsiSyncClient, o processo será usado apenas para compatibilidade com versões anteriores. A interface CsiSyncClient e a metodologia de controle do ODC serão alteradas em futuras versões do Office.
  
A ID de classe está atualmente definida para responder apenas ao OneDrive.
  
O objeto COM é utilizável como um servidor COM fora do processamento e é executado no CsiSyncClient. exe. Devido às limitações com o Access (que o ODC usa), ele é fornecido com o tipo de bit que o Office entra, de modo que o Office x64 significa um objeto COM x64 ou o x86 Office significa um objeto COM x86. Para contornar essa limitação, especificar CLSCTX_LOCAL_SERVER como parte do CoCreateInstance terá o objeto COM hospedado como um servidor COM fora de processamento, permitindo a compatibilidade de bits cruzados.
  
## <a name="interfaces"></a>Interfaces

O CSISyncClient usa as seguintes interfaces.
  
### <a name="interface-ilsclocalsyncclient"></a>Interface ILSCLocalSyncClient

Esta é a interface principal usada para sincronizar arquivos no Office.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
O objeto COM que é exposto é usado como um servidor fora de processamento. A especificação de CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite a compatibilidade entre processos de 64 bits e 32 bits.
  
Depois de criar o objeto COM, você deve chamar [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) primeiro. Após o [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ter sido concluída com êxito, você pode chamar qualquer API com a frequência desejada e em qualquer ordem. Você também pode chamar [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) em um objeto já inicializado, mas isso não faz nada. 
  
As exceções para o parágrafo anterior são [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) e [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Depois de chamar [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) no objeto com, você deve destruir o objeto e criar um novo. [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) excluirá seu subcache, excluirá todas as informações de arquivo associadas no cache, mas deixará os documentos em disco. Também deixa o estado intacto para se comunicar com o cache. Isso permite chamar [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) novamente para criar um novo cache sem ter que destruir e recriar o objeto com. 
  
**Funções de membro público**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile é usado para remover as informações de arquivo do cache. No enTanto, esse método deixará o arquivo associado no disco e no servidor.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
A cadeia de caracteres que identifica o reSourceid do arquivo. Este valor deve ser não vazio com um máximo de 128 caracteres. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O reSourceid fornecido não está no cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |A inicialização não foi chamada com êxito no passado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo está atualmente sincronizando ou aberto e não pode ser excluído.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient:: getChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges retorna um enumerador de objetos ILSCEvent e também retorna um token que é fornecido à próxima chamada a getChanges, supondo que o consumidor tenha processado o conjunto de eventos anterior. Os eventos antes do _nPreviousChangesToken_ especificado serão excluídos e não estarão disponíveis. Se não houver eventos a serem processados, _pnCurrentChangesToken_ deverá ser o mesmo valor que _NPreviousChangesToken_, mas _ppiEvents_ ainda será definido. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parâmetros

 _nPreviousChangesToken_
  
Identifica qual evento foi processado pela última vez pelo consumidor. 
  
 _pnCurrentChangesToken_
  
Identifica o evento mais recente que está sendo entregue ao consumidor. Não deve ser nulo.
  
 _ppiEvents_
  
Um enumerador para os eventos enviados para o consumidor. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: GetClientNetworkSyncPermission

O GetClientNetworkSyncPermission é usado para consultar se a heurística de sincronização do Office para o uso de custos e energia de rede é substituída. Quando em uma rede 3G ou de alto custo ou durante a execução da bateria em vez de serem conectadas, o Office pode optar por bloquear o tráfego de rede até um tempo mais Opportune.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parâmetros

 _nspType_
  
Um sinalizador que define o custo heurístico a ser consultado. Consulte [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Especifica se o heurístico de custo solicitado está substituído ou não no momento. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient:: GetFileStatus

O GetFileStatus é usado para coletar informações de um arquivo específico: se ele existe no cache, se ele tem comunicação pendente com a cópia do servidor e se o Office 2013 tem os dados mais atualizados da cópia local. Requer um sinalizador bit a bit de [Enumeração LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) valores para determinar quais informações o objeto com do CsiSyncClient deve consultar. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
A cadeia de caracteres que identifica o arquivo no cliente. Este valor deve ser não vazio, com no máximo 128 caracteres. 
  
 _sfRequestedStatus_
  
Um sinalizador que define as informações a serem retornadas. Consulte [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
A cadeia de caracteres que identifica o local do arquivo identificado por _bstrResourceID_ no cliente. Não deve ser nulo. 
  
 _pbstrETag_
  
Uma cadeia de caracteres que conterá a eTag para o arquivo identificado por _bstrResourceID_. Não deve ser nulo. 
  
 _psfFileStatus_
  
Um sinalizador que conterá o status solicitado via _sfRequestedStatus_ para o arquivo identificado por _bstrResourceID_. Não deve ser nulo. Consulte [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |As informações de arquivo especificadas por _bstrResourceID_ não existem no cache.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged foi solicitado ou o arquivo especificado por _bstrResourceID_ está bloqueado ou ausente.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient:: GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions retorna uma lista de extensões de arquivo delimitadas por pipe que atualmente têm suporte no objeto COM do CsiSyncClient. Observe que essa lista pode ser alterada, e o consumidor será notificado sobre uma alteração por meio do objeto IPartnerActivityCallback fornecido em [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (consulte EventOccured). 
  
Um exemplo da cadeia de caracteres retornada é o seguinte: "| docx | docm | pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parâmetros

 _pbstrSupportedFileExtensions_
  
Uma cadeia de caracteres a ser definida com um conjunto delimitado por pipe de extensões de arquivo suportadas pelo objeto COM CsiSyncClient. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient:: Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize deve ser o primeiro método chamado. Caso contrário, todas as outras APIs retornarão E_LSC_NOTINITIALIZED. Chamar Initialize em um objeto já inicializado retorna S_OK e não faz nada. Se E_LSC_CACHEMISMATCH for retornado, o chamador poderá chamar [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para excluir o cache associado ao fornecido fornecido. No enTanto, nesse caso, outras APIs ainda retornarão E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parâmetros

 _bstrSuppliedID_
  
Identifica o consumidor e o cache a ser usado. Deve ser não vazio com um máximo de 32 caracteres. 
  
 _bstrProgID_
  
Identifica o objeto COM do consumidor para comunicação bidirecional. Deve ser não vazio com um máximo de 39 caracteres. Confira [ \<a tecla ProgID\> ](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obter mais informações sobre ProgIDs. 
  
 _bstrFileSystemDirectoryHint_
  
Identifica a raiz do diretório no qual os arquivos locais serão armazenados. Deve ser não vazio com um máximo de 256 caracteres. O diretório já deve existir. 
  
 _pEventCallback_
  
A interface de retorno de chamada para a qual o CsiSyncClient irá notificar as alterações. Consulte IPartnerActivityCallback:: EventOccurred. Esse valor não deve ser nulo. 
  
 _pfCreatedNewCache_
  
Retorna se um novo cache foi criado. Se nenhum cache estiver associado ao fornecido, será criado um. Esse valor não deve ser nulo.
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Um fornecido já tem um cache associado a ele, mas tem um ProgId ou FileSystemDirectoryHint diferente dos fornecidos.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |O FileSystemDirectoryHint (ou uma subpasta) já existe em um cache diferente.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |O ProgID já existe em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient:: LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange é usado para dizer ao objeto COM do CsiSyncClient que tentará carregar o arquivo especificado. O método irá preparar o arquivo para carregamento, incluindo a leitura do conteúdo atual do arquivo. Se um upload já estiver pendente, o carregamento anterior será descartado e o novo conteúdo preparado para carregar. Se o arquivo estiver aberto para edição em um aplicativo, esse método retornará S_OK sem preparar o arquivo para carregamento (o aplicativo já deve fazer essa etapa se houver alterações).
  
Este método permitirá carregamentos se ele tiver sido marcado como uploads bloqueados anteriormente (consulte [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)RenameFile).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _bstrFileSystemPath_
  
Uma cadeia de caracteres que identifica o arquivo no cliente. Este valor deve ser um caminho local não vazio com um máximo de 256 caracteres. Este caminho deve estar na árvore de diretório especificada por FileSystemDirectoryHint quando a chamada para [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) foi feita. 
  
 _bstrResourceID_
  
Uma cadeia de caracteres que identifica a reSourceid do arquivo. Este valor deve ser não vazio com um máximo de 128 caracteres. 
  
 _bstrWebPath_
  
Uma cadeia de caracteres que identifica o arquivo no servidor. Esse valor deve ser não vazio, uma URL válida, mas não mais de INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O arquivo especificado por _bstrFileSystemPath_ tem um ResourceId diferente do especificado. Um evento do tipo LSCEventType_OnFilePathConflict é enviado quando esse erro é retornado. ConFira [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O arquivo foi excluído de operação intermediária.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |A extensão de arquivo fornecida não é suportada pelo objeto COM CsiSyncClient. Consulte [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |O objeto COM não agendou um carregamento porque o arquivo no cache tinha as alterações mais recentes do disco.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |O arquivo especificado por _bstrFileSystemPath_ está ausente ou bloqueado.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath fornecido não está na raiz do diretório especificado pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado já tem alterações pendentes em um cache diferente e ainda não pode ser associado ao cache do consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |O webPath fornecido está em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient:: RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile associará uma nova URL e um caminho local para um determinado reSourceid. Se o arquivo especificado pelo reSourceid ainda não existir no cache, uma tentativa será feita para criá-lo e marcá-lo para download.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parâmetros

 _bstrResourceID_
  
Uma cadeia de caracteres que identifica a reSourceid do arquivo. Este valor deve ser não vazio com um máximo de 128 caracteres. 
  
 _bstrNewFileSystemPath_
  
Uma cadeia de caracteres que especifica o novo caminho local para o arquivo. Este valor deve ser um caminho local não vazio com um máximo de 256 caracteres. Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita. 
  
 _bstrNewWebPath_
  
Uma cadeia de caracteres que especifica a nova URL para o arquivo. Esse valor deve ser uma URL válida não vazia, mas não mais do que INTERNET_MAX_URL_LENGTH, conforme definido https://support.microsoft.com/kb/208427por. 
  
 _fBlockUploads_
  
Especifica se os carregamentos no novo local são permitidos no momento. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O _bstrNewFileSystemPath_ ou o _bstrNewWebPath_ já existem em outro arquivo em qualquer cache. Um evento do tipo LSCEventType_OnFilePathConflict é enviado quando esse erro é retornado. ConFira [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |As informações do arquivo foram excluídas do cache enquanto esse método estava em execução.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath fornecido não está na raiz do diretório especificado pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado está atualmente sincronizando em um aplicativo do Office.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient:: ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

O ResetCache excluirá o cache associado ao fornecido, fornecido na inicialização. Isso inclui todas as informações do arquivo, mas deixará os arquivos no cliente e no servidor. Esse método também deixa o objeto em um estado parcialmente não inicializado. As únicas chamadas válidas depois disso são [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ou [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Este método pode ser chamado se a inicialização falhar e retornar E_LSC_CACHEMISMATCH, e excluirá o cache associado ao fornecido que foi fornecido com a chamada com falha.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parameters

Nenhuma
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Ocorreu uma falha na chamada.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient:: ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange informa ao objeto COM do CsiSyncClient para marcar o arquivo especificado para download. Se o arquivo estiver aberto em um aplicativo do Office para edição, este método retornará S_OK sem marcar o arquivo para download (o aplicativo já deve fazer essa etapa se houver alterações).
  
Este método permitirá downloads se ele foi marcado como downloads bloqueados anteriormente (consulte RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Uma cadeia de caracteres que identifica o arquivo no cliente. Este valor deve ser um caminho local não vazio com um máximo de 256 caracteres. Esse caminho deve estar na árvore de diretório especificada pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.  <br/> |
|bstrResourceID  <br/> |Uma cadeia de caracteres que identifica a reSourceid do arquivo. Este valor deve ser não vazio com um máximo de 128 caracteres.  <br/> |
|bstrWebPath  <br/> |Uma cadeia de caracteres que identifica o arquivo no servidor. Este valor deve ser uma URL válida não vazia, mas não mais de INTERNET_MAX_URL_LENGTH, conforme definido por https://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao definir o estado de conectividade do cache.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |O arquivo especificado por _bstrFileSystemPath_ tem um ResourceId diferente do especificado.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |A extensão de arquivo fornecida não é suportada pelo objeto COM CsiSyncClient. Consulte GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |O arquivo foi excluído em meados da operação.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |O FileSystemPath fornecido não está na raiz do diretório especificado pelo FileSystemDirectoryHint quando a chamada para Initialize foi feita.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |O arquivo especificado por _bstrResourceID_ tem um FileSystemPath diferente do especificado.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |O arquivo especificado já tem alterações pendentes em um cache diferente e ainda não pode ser associado ao cache do consumidor.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |O webPath fornecido está em um cache diferente.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient:: SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Define o cache em um estado online ou offline. Se estiver offline, o Office não tentará se comunicar com o servidor para nenhum arquivo desse cache, independentemente da configuração _fBlockUploads_ de cada arquivo individual. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parâmetros

 _fIsOnline_
  
Um booliano que determina o estado de conectividade do cache. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao definir o estado de conectividade do cache.  <br/> |
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission é usado para substituir ou restoreOffice a heurística de sincronização para o custo de rede e o uso de energia. Quando em uma rede 3G ou de alto custo ou durante a execução da bateria em vez de serem conectadas, o Office pode optar por bloquear o tráfego de rede até um tempo mais Opportune. O consumidor dessa API pode usá-la para substituir a heurística do Office e forçar a sincronização.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parâmetros

 _nspType_
  
Um sinalizador que define qual heurística de custo será substituída. Consulte [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Especifica se a sincronização deve ser forçada, substituindo o custo heurístico ou não mais a substituir. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao substituir a heurística de sincronização.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient:: Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Descarrega o cache do objeto COM e realiza operações de fechamento. [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEVE ser chamado antes de destruir o objeto COM. Uma vez chamado, nenhuma outra API pode ser chamada, o objeto COM deve ser destruído e um novo criado se você quiser continuar as operações. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parâmetros

Nenhum.
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_FAIL  <br/> |Falha ao cancelar a inicialização.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) não foi chamado com êxito no passado.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Interface IEnumLSCEvent

Esta interface representa uma lista de eventos ILSCEvent.
  
**Funções de membro público**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent:: FNext

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
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent:: Reset

Redefine o enumerador para o primeiro evento.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parâmetros

Nenhum.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
### <a name="interface-ilscevent"></a>Interface ILSCEvent

Esta interface representa um evento de sincronização. Todas as informações sobre o evento podem ser recuperadas da interface.
  
**Funções de membro público**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent:: GetConflictStatus

Observe que esse valor é preenchido quando [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges é chamado, não quando o evento foi criado, de modo que você só terá o status atual do arquivo, e não o status do arquivo quando o status de conflito for alterado. 
  
Esse valor será preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento for LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parâmetros

 _pfIsInConflict_
  
O status atual de conflito do arquivo associado ao evento.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent:: GetError

Esse valor é preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parâmetros

 _pnError_
  
O erro associado a este evento.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent:: getETag

Esse valor é preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parâmetros

 _pbstrETag_
  
A ETag associada a este evento
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent:: getEventtype

Obtém o tipo deste evento.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parâmetros

 _pnEventType_
  
O tipo de evento desse evento. ConFira [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para valores válidos. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent:: GetLocalWorkingPath

Obtém o caminho de trabalho local para esse evento.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parâmetros

 _pbstrLocalWorkingPath_
  
O caminho local do arquivo ao qual esse evento pertence. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent:: getResourceid

Obtém a ID de recurso para o evento.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parâmetros

 _pbstrResourceID_
  
O reSourceid do arquivo associado a esse evento.
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent:: GetResourceIDAttempted

Esse valor será preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento for LSCEventType_OnFilePathConflict. Quando uma chamada para [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) renameFile causar um conflito de caminho local ou caminho da Web com outro arquivo no cache de arquivos do Office, essa evento é gerado. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parâmetros

 _pbstrResourceIDAttempted_
  
O reSourceid que provocou esse evento para ser gerado. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent:: GetSyncErrorType

Esse valor é preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento é LSCEventType_OnServerChangesDownloaded ou LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parâmetros

 _pnSyncErrorType_
  
O tipo de erro associado a esse evento. Consulte [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para obter os valores possíveis. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_INVALIDARG  <br/> |Um ou mais parâmetros são inválidos.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent:: GetWebPath

Esse valor será preenchido apenas quando a [LSCEventType de enumeração](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) do evento for LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parâmetros

 _pbstrWebPath_
  
Especifica o caminho da Web associado a esse evento. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK. 
  
### <a name="interface-ilscevent2"></a>Interface ILSCEvent2

Esta interface contém informações adicionais sobre um evento de sincronização.
  
**Funções de membro público**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2:: GetErrorChain

Obtém as informações da cadeia de erros sobre um evento de sincronização.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parâmetros

 _pbstrErrorChain_
  
Uma cadeia de caracteres para armazenar as informações da cadeia de erros. Não deve ser nulo. 
  
##### <a name="return-values"></a>Valor de retorno

|Valor|Descrição|
|:-----|:-----|
|E_NOTIMPL  <br/> |A versão instalada do Office não tem suporte para essa interface  <br/> |
|E_INVALIDARG  <br/> |Um ou mais dos valores de parâmetro são inválidos.  <br/> |
|E_FAIL  <br/> |As informações da cadeia de erros não estão disponíveis.  <br/> |
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Interface IPartnerActivityCallback

Esta interface fornece uma função de retorno de chamada para o objeto COM CSISyncClient.
  
**Funções de membro público**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback:: EventOccurred

Esta é uma função de retorno de chamada no objeto fornecido ao objeto COM CsiSyncClient. É esperado que, quando ocorrer um evento (consulte [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válidos), o objeto com do CsiSyncClient chamará esse método, sinalizando o consumidor. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parâmetros

 _eEventTypeOccurred_
  
O tipo de evento desse evento. ConFira [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para valores válidos. 
  
##### <a name="return-values"></a>Valor de retorno

Sempre retorna S_OK.
  
## <a name="enumerations"></a>Enumerações

O CSISyncClient usa as seguintes enumerações.
  
### <a name="enum-lsceventsyncerrortype"></a>Enumerar LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Essa enumeração Especifica as categorias de erros que podem ocorrer durante a sincronização de um arquivo.
  
|Enumera|Descrição|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |O erro de sincronização desse evento foi inesperado e pode exigir consideração especial. Por padrão, o usuário pode ter que intervir.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |O erro de sincronização desse evento não precisa de consideração especial. O Office vai tratá-lo automaticamente.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |O erro de sincronização desse evento requer um usuário para resolvê-lo. Por exemplo, o erro de conflito de mesclagem exige que um usuário abra o documento e mescle-o.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |O erro de sincronização desse evento exige que o consumidor intervenha, mas não deve exigir consideração especial pelo usuário.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |O erro de sincronização desse evento exige que o consumidor fique interinterveniente como um caso especial.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enumerar LSCEventType
<a name="Enum_LSCEventType"> </a>

Essa enumeração Especifica o tipo de eventos que podem ocorrer para um arquivo específico.
  
|Enumera|Descrição|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Foram feitas alterações em um arquivo local.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Um usuário abriu um arquivo.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Concluído o download de alterações de arquivo do servidor.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Concluído o carregamento de alterações de arquivo no servidor.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |O estado de conflito de mesclagem de um arquivo foi alterado.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Um arquivo foi adicionado.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Um arquivo foi excluído.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |A sincronização foi habilitada para os arquivos de um usuário.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Iniciado o download de alterações de arquivo do servidor.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Iniciado o carregamento de alterações de arquivo no servidor.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Esse evento é gerado quando uma chamada para [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)ou [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) RenameFile causa um conflito de caminho local ou caminho da Web com outro arquivo no Cache de arquivos do Office.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enumerar LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Essa enumeração Especifica o tipo de eventos que podem ocorrer. O consumidor precisa chamar funções específicas do ILSCLocalSyncClient com base no tipo de evento.
  
|Enumera|Descrição|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ocorreu um ILSCEvent. O consumidor deve chamar [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges para recuperar os dados.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |As extensões de arquivo com suporte foram alteradas. O consumidor deve chamar [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar a nova lista de extensões com suporte.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enumerar LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Essa enumeração Especifica os sinalizadores usados para um heurístico de custo de rede. 

|Enumera|Descrição|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True se o custo heurístico para redes caras (como 3G) é substituído.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True se o custo heurístico para uso de energia (como uma bateria) é substituído.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enumerar LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Essa enumeração é usada para representar o status de sincronização de um arquivo. 
  
|Enumera|Descrição|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True se houver dados pendentes para enviar ao arquivo de servidor.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True se houver dados pendentes para baixar do arquivo de servidor.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True se os dados que o Office tem no arquivo em seu cache é a cópia mais recente dos dados no disco.  <br/> |
   

