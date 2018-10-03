---
title: Constantes MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4f84ed318fa53877acd9d4759b81c140d2b32e6b
ms.sourcegitcommit: 6a8c758e690c4b7f3ab6d40635606efd31a3cc07
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/03/2018
ms.locfileid: "25361482"
---
# <a name="mapi-constants"></a>Constantes MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico contém as definições de constantes, declarações de interface MAPI e identificadores de classe e de interface usados pelas APIs de MAPI.
  
## <a name="class-and-interface-identifiers"></a>Identificadores de classe e interface

Use a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar nomes simbólicos de identificador globalmente exclusivo (GUID) com seus valores, a menos que indicado de outra forma.
  
## <a name="attachment-security-conversion-api"></a>API de conversão de segurança de anexo

Esta seção contém as definições de constantes e os identificadores de interface para a API de segurança de anexo.
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Use a macro MAPIMETHOD definida no mapidefs.h de arquivo de cabeçalho do SDK do Windows para definir a função virtual pura **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Use a macro DECLARE_MAPI_INTERFACE_ definida no mapidefs.h de arquivo de cabeçalho do SDK do Windows para definir a tabela de método virtual para **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>API de conversão de MIME MAPI

Esta seção contém definições de constantes e os identificadores de classe e a interface para a API de conversão de MIME de MAPI.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0x0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0x0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0x1000  <br/> |
|CCSF_NO_MSGID  <br/> |0x4000  <br/> |
|CCSF_GLOBAL_MESSAGE  <br/> |0x00200000  <br/> |
|E_INVALIDARG  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows*  <br/> |
   
### <a name="class-identifiers"></a>Identificadores de classe

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>Identificadores de interface

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>API de estado offline

Esta seção contém definições de constantes e os identificadores de classe e a interface para a API de estado Offline.
  
### <a name="constants"></a>Constantes

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows*  <br/> |
|E_NOINTERFACE  <br/> | *Conforme definido em Winerror de arquivo de cabeçalho do Windows (SDK)*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**Online ou offline** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0x00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>Identificadores de classe

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>Identificadores de interface

```cpp
//{000672B5-0000-0000-c000-000000000046}
DEFINE_GUID(IID_IMAPIOffline, 0x000672B5, 0x0000, 0x0000, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
```

```cpp
//{0317bde5-fc29-44cd-8dcd-36125a3be9ec}
DEFINE_GUID(IID_IMAPIOfflineNotify, 0x0317bde5, 0xfc29, 0x44cd, 0x8d, 0xcd, 0x36, 0x12, 0x5a, 0x3b, 0xe9, 0xec);
```

```cpp
//{42175607-ff3e-4790-bc18-66c8643e6424
DEFINE_GUID(IID_IMAPIOfflineMgr, 0x42175607, 0xFF3E, 0x4790, 0xbc, 0x18, 0x66, 0xc8, 0x64, 0x3e, 0x64, 0x24);
```

## <a name="outlook-named-properties"></a>Propriedades nomeado do Outlook

Esta seção contém as definições de constantes para propriedades nomeadas e seus namespaces e outras constantes relacionadas.
  
### <a name="definitions-for-named-properties"></a>Definições de propriedades nomeadas

```cpp
#define dispidMeetingType0x0026 
#define dispidFileUnder0x8005 
#define dispidYomiFirstName 0x802C 
#define dispidYomiLastName 0x802D 
#define dispidYomiCompanyName 0x802E 
#define dispidWorkAddressStreet 0x8045 
#define dispidWorkAddressCity 0x8046 
#define dispidWorkAddressState 0x8047 
#define dispidWorkAddressPostalCode 0x8048 
#define dispidWorkAddressCountry 0x8049 
#define dispidWorkAddressPostOfficeBox 0x804A 
#define dispidInstMsg 0x8062 
#define dispidEmailDisplayName 0x8080 
#define dispidEmailAddrType 0x8082 
#define dispidEmailEmailAddress 0x8083 
#define dispidEmailOriginalDisplayName 0x8084 
#define dispidEmail1OriginalEntryID0x8085 
#define dispidEmail2DisplayName 0x8090 
#define dispidEmail2AddrType 0x8092 
#define dispidEmail2EmailAddress 0x8093 
#define dispidEmail2OriginalDisplayName 0x8094 
#define dispidEmail2OriginalEntryID0x8095 
#define dispidEmail3DisplayName 0x80A0 
#define dispidEmail3AddrType 0x80A2 
#define dispidEmail3EmailAddress 0x80A3 
#define dispidEmail3OriginalDisplayName 0x80A4 
#define dispidEmail3OriginalEntryID0x80A5 
#define dispidTaskStatus 0x8101 
#define dispidTaskStartDate 0x8104 
#define dispidTaskDueDate 0x8105 
#define dispidTaskActualEffort 0x8110 
#define dispidTaskEstimatedEffort 0x8111 
#define dispidTaskFRecur 0x8126 
#define dispidBusyStatus0x8205 
#define dispidLocation 0x8208 
#define dispidApptStartWhole 0x820D 
#define dispidApptEndWhole 0x820E 
#define dispidApptDuration 0x8213 
#define dispidRecurring 0x8223 
#define dispidTimeZoneStruct0x8233 
#define dispidAllAttendeesString 0x8238 
#define dispidToAttendeesString 0x823B 
#define dispidCCAttendeesString 0x823C 
#define dispidConfCheck0x8240 
#define dispidApptCounterProposal 0x8257 
#define dispidApptTZDefStartDisplay0x825E 
#define dispidApptTZDefEndDisplay0x825F 
#define dispidApptTZDefRecur0x8260 
#define dispidReminderTime0x8502 
#define dispidReminderSet 0x8503 
#define dispidFormStorage0x850F 
#define dispidPageDirStream0x8513 
#define dispidSmartNoAttach 0x8514 
#define dispidCommonStart 0x8516 
#define dispidCommonEnd 0x8517 
#define dispidFormPropStream0x851B 
#define dispidRequest 0x8530 
#define dispidCompanies 0x8539 
#define dispidContacts0x853A 
#define dispidPropDefStream0x8540 
#define dispidScriptStream0x8541 
#define dispidCustomFlag0x8542 
#define dispidReminderNextTime 0x8560 
#define dispidHeaderItem0x8578 
#define dispidUseTNEF0x8582 
#define dispidToDoTitle0x85A4 
#define dispidLogType 0x8700 
#define dispidLogStart 0x8706 
#define dispidLogDuration 0x8707 
#define dispidLogEnd 0x8708 
```

### <a name="definitions-for-namespaces"></a>Definições de namespaces

Os seguintes identificadores identificador global exclusivos (GUIDs) representam os namespaces das propriedades nomeadas.
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment= {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

Consulte a seção repositório MAPI para as definições de PSETID.
  
### <a name="other-constants"></a>Outras constantes

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Conforme definido em mapidefs.h de arquivo de cabeçalho.*  <br/> |
|MNID_STRING  <br/> | *Conforme definido em mapidefs.h de arquivo de cabeçalho.*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>API de replicação

Esta seção contém as definições de constantes, declarações de interface MAPI e identificadores de classe e a interface para a API de replicação.
  
### <a name="constants"></a>Constantes

A seguir está uma estrutura [MAPIUID](mapiuid.md) que identifica um provedor de serviços MAPI: 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0x00010000  <br/> |
|DNT_OK  <br/> |0x00010000  <br/> |
|HSF_LOCAL  <br/> |0x00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0x00000010  <br/> |
|HSF_OK  <br/> |0x00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0X00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0X00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0X00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0x00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0x00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0x00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0x00010000  <br/> |
|UPD_MOVED  <br/> |0x00020000  <br/> |
|UPD_UPDATE  <br/> |0x00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0x00000004  <br/> |
|UPF_DEL  <br/> |0x00000008  <br/> |
|UPF_OK  <br/> |0x00010000  <br/> |
|UPH_OK  <br/> |0x00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0x00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0x00000008  <br/> |
|UPM_HEADER  <br/> |0x00000010  <br/> |
|UPM_OK  <br/> |0x00010000  <br/> |
|UPM_MOVED  <br/> |0x00020000  <br/> |
|UPM_COMMIT  <br/> |0x00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0x00010000  <br/> |
|UPR_COMMIT  <br/> |0x00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0x00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0x00010000  <br/> |
|UPT_OK  <br/> |0x00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0x00010000  <br/> |
|UPV_DIRTY  <br/> |0x00020000  <br/> |
|UPV_COMMIT  <br/> |0x00040000  <br/> |
   
### <a name="interface-declarations"></a>Declarações de interface

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>Identificadores de interface

```cpp
//{4FDEEFF0-0319-11CF-B4CF-00AA0DBBB6E6}
DEFINE_GUID (IID_IPSTX, 0x4FDEEFF0, 0x0319, 0x11CF, 0xB4, 0xCF, 0x00, 0xAA, 0x0D, 0xBB, 0xB6, 0xE6)
```

```cpp
//{2067A790-2A45-11D1-EB86-00A0C90DCA6D}
DEFINE_GUID (IID_IPSTX2, 0x2067A790, 0x2A45, 0x11D1, 0xEB, 0x86, 0x00, 0xA0, 0xC9, 0x0D, 0xCA, 0x6D)
```

```cpp
//{55f15320-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX3, 0x55f15320, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{aa2e2092-ac08-11d2-a2f9-0060b0ec3d4f}
DEFINE_GUID (IID_IPSTX4, 0xaa2e2092, 0xac08, 0x11d2, 0xa2, 0xf9, 0x00, 0x60, 0xb0, 0xec, 0x3d, 0x4f)
```

```cpp
//{55f15322-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX5, 0x55f15322, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{55f15323-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX6, 0x55f15323, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{d2d85db4-840f-49b8-9982-07d2405ec6b7}
DEFINE_GUID (IID_IOSTX, 0xd2d85db4,  0x840f, 0x49b8, 0x99, 0x82, 0x07, 0xd2, 0x40, 0x5e, 0xc6, 0xb7)
```

<br/>

Use os dois seguintes identificadores de interface com [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)ou [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir e ignorar qualquer seleção provedor em um objeto folder e um objeto de mensagem, respectivamente. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>Repositório MAPI

Esta seção contém as definições de constantes e identificadores de interface usado pela APIs essa interface com um repositório MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0X00010000)  <br/> |Um provedor de armazenamento pode especificar **fnevIndexing** no membro **ulEventType** da estrutura de **[notificação](notification.md)** para notificar o indexador que um objeto está pronto para indexação. O membro **info** da estrutura de **notificação** contém uma estrutura **[EXTENDED_NOTIFICATION](extended_notification.md)** .  <br/> |
|FS_NONE  <br/> |0x00  <br/> |Um cliente pode chamar **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** e a seleção para o bitmask retornado. **FS_NONE** indica que a pasta não oferece suporte a compartilhamento.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Um cliente pode chamar **IFolderSupport::GetSupportMask** e a seleção para o bitmask retornado. **FS_SUPPORTS_SHARING** indica que a pasta oferece suporte a compartilhamento.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0X00000001)  <br/> |Identifica o processo que está fazendo com que uma notificação para um indexador que um objeto está pronto para indexação.  <br/> |
|MNID_ID  <br/> |Conforme definido em mapidefs.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows  <br/> |Um valor para o campo **ulKind** da estrutura **[MAPINAMEID](mapinameid.md)** .  <br/> |
|MNID_STRING  <br/> |Conforme definido em mapidefs.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows.  <br/> |Um valor para o campo **ulKind** da estrutura **[MAPINAMEID](mapinameid.md)** .  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0X00000001)  <br/> |Se um cliente especifica **MSCAP_SEL_RESTRICTION** em *mscapSelector* para **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** pode retornar esse valor se o repositório ignora os parâmetros inválidos em uma restrição.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0X00000020)  <br/> |Se um cliente especifica **MSCAP_SEL_FOLDER** em *mscapSelector* para **IMSCapabilities::GetCapabilities**, **GetCapabilities** pode retornar esse valor se o repositório for um repositório não padrão que ofereça suporte a home pages da pasta.  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0X00800000)  <br/> |Um cliente pode obter a propriedade **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** para determinar as características de um armazenamento de mensagens. Se o provedor de armazenamento define o sinalizador **STORE_PUSHER_OK** no bitmask, isso significa que o manipulador de protocolo MAPI não irá rastrear o repositório e o armazenamento é responsável por push quaisquer alterações por meio de notificações para o indexador para ter mensagens indexadas.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Definições de namespaces

Os seguintes identificadores identificador global exclusivos (GUIDs) representam os namespaces propriedades nomeadas. Eles são indexados pelo manipulador de protocolo MAPI (PH) e são documentados como somente leitura.
  
> [!CAUTION]
> As propriedades nomeadas não devem ser usadas para criar ou modificar os itens. 
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment   = {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting       = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

#### <a name="mnidid-properties"></a>Propriedades MNID_ID
  
```cpp
// In PSETID_Address
#define dispidWorkAddressStreet 0x8045
#define dispidWorkAddressCity 0x8046
#define dispidWorkAddressState 0x8047
#define dispidWorkAddressPostalCode 0x8048
#define dispidWorkAddressCountry 0x8049
#define dispidInstMsg 0x8062
#define dispidEmailDisplayName 0x8080
#define dispidEmailOriginalDisplayName 0x8084
```

```cpp
// In PSETID_Appointment
#define dispidLocation 0x8208
#define dispidApptStartWhole 0x820D
#define dispidApptEndWhole 0x820E
#define dispidApptDuration 0x8213
#define dispidRecurring 0x8223
#define dispidAllAttendeesString 0x8238
#define dispidToAttendeesString 0x823B
#define dispidCCAttendeesString 0x823C
```

```cpp
// In PSETID_Common
#define dispidReminderSet 0x8503
#define dispidSmartNoAttach 0x8514
#define dispidCommonStart 0x8516
#define dispidCommonEnd 0x8517
#define dispidRequest 0x8530
#define dispidCompanies 0x8539
#define dispidReminderNextTime 0x8560
```

```cpp
// In PSETID_Log (also known as Journal)
#define dispidLogType 0x8700
#define dispidLogStart 0x8706
#define dispidLogDuration 0x8707
#define dispidLogEnd 0x8708MNID_STRING properties
```

```cpp
// In PSETID_Task
#define dispidTaskStartDate 0x8104
#define dispidTaskDueDate 0x8105
#define dispidTaskActualEffort 0x8110
#define dispidTaskEstimatedEffort 0x8111
#define dispidTaskFRecur 0x8126
```

#### <a name="mnidstring-properties"></a>Propriedades MNID_STRING
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a>Identificadores de interface

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Use o `DEFINE_OLEGUID` macro definida em guiddef.h de arquivo de cabeçalho do SDK do Windows para associar o seguinte nome simbólico GUID seu valor. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>Constantes de catálogo de endereços de MAPI

Esta seção contém as definições de constantes para o catálogo de endereços de MAPI.
  
### <a name="constants"></a>Constantes

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0X00000001)  <br/> |A pasta raiz para um objeto de catálogo de endereços MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0X00000002)  <br/> |Uma subpasta contida na pasta raiz do objeto de catálogo de endereços MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0X00000003)  <br/> |Um objeto de contêiner de catálogo de endereços.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0X00000004)  <br/> |Um objeto de usuário de mensagens.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0X00000005)  <br/> |Um objeto de lista de distribuição.  <br/> |
   
## <a name="additional-mapi-constants"></a>Constantes MAPI adicionais

Esta seção contém definições constantes, incluindo códigos de erro e os identificadores de interface usados pelo APIs de MAPI não anteriormente expostos e documentadas.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0X00000001)  <br/> |Quando um cliente chama o método [IAddrBook::Details](iaddrbook-details.md) , o cliente deve definir o sinalizador **DIALOG_MODAL** no parâmetro _ulFlags_ para exibir a caixa de diálogo modal mostrando os detalhes sobre uma entrada de catálogo de endereço específica. Essa constante é definido em mapidefs.h.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |No Outlook 2007, repositórios de PST com quebra têm regras e filtragem de spam processado em novas mensagens, antes de clientes MAPI são notificados das novas mensagens. Um cliente usando o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem em repositórios de PST ou o provedor deve definir o sinalizador **ITEMPROC_FORCE** no parâmetro _ulFlags_ do método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar ao arquivo PST as regras de repositório que a mensagem é qualificada para processamento antes que o repositório notificará qualquer cliente escuta a partir da chegada da nova mensagem. Observe que tais regras processamento só se aplica às novas mensagens criadas em um servidor que não seja um Microsoft Exchange Server, pois o Exchange Server processa as regras para mensagens no servidor. Daí o provedor ou criar a mensagem de cliente deve passar por esse sinalizador em combinação com **NON_EMS_XP_SAVE**, indicando que o servidor não é um servidor Exchange.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Um cliente pode chamar a função [MAPILogonEx](mapilogonex.md) , definindo o sinalizador **MAPI_BG_SESSION** no parâmetro _flFlags_ para efetuar logon em uma sessão e realizar qualquer operação em segundo plano. Em geral, se um cliente pretende fazer processamento em um segmento de plano de fundo ou em um processo separado no modo não invasiva para o segmento de primeiro plano, ele deve chamar [MAPILogonEx](mapilogonex.md) com o sinalizador **MAPI_BG_SESSION** . Um exemplo em que esse recurso é usado é um aplicativo de cliente, como um mecanismo de indexação, abrindo um arquivo de pastas particulares (PST) para acesso de tipo de plano de fundo.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Um cliente pode chamar o método [IAddrBook::OpenEntry](iaddrbook-openentry.md) , definindo o sinalizador **MAPI_CACHE_ONLY** no parâmetro _ulFlags_ para abrir uma entrada do catálogo de endereços e para acessá-lo subsequentemente apenas do cache. Um exemplo em que esse recurso é usado é um aplicativo cliente que deseja abrir a lista de endereços Global no modo cache do Exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000c  <br/> |Esse valor pode ser passado para a função de MAPISendMail de MAPI simples no parâmetro _ulFlags_ para especificar que uma caixa de diálogo sem janela restrita é exibida, o aplicativo de email padrão. Se nem esse sinalizador nem MAPI_DIALOG (0x00000008) estiver definida, nenhuma caixa de diálogo é exibida.  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Se o Microsoft Office Outlook está no modo cache do Exchange e um repositório foi aberto em modo de cache, um provedor de cliente ou serviço pode chamar [IMsgStore::OpenEntry](imsgstore-openentry.md), definindo o sinalizador **MAPI_NO_CACHE** no parâmetro _ulFlags_ para abrir um item ou um pasta em que o armazenamento remoto. Observe que, se você abrir o armazenamento de mensagens com o sinalizador **MDB_ONLINE** no servidor remoto, você não precisará usar o sinalizador **MAPI_NO_CACHE** .  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |Um provedor de cliente ou serviço pode chamar a função [OpenIMsgOnIStg](openimsgonistg.md) , definindo o sinalizador **MAPI_UNICODE** no parâmetro _ulFlags_ para criar os arquivos do. msg Unicode. O resultante [IMessage: IMAPIProp](imessageimapiprop.md) arquivo mostra **STORE_UNICODE_OK** em sua [Propriedade canônico de PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) e oferece suporte a Unicode propriedades. Essa constante é definido em mapidefs.h.  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Se o Outlook está no modo cache do Exchange, um provedor de cliente ou serviço pode chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) , definindo o sinalizador **MDB_ONLINE** no parâmetro _ulFlags_ para substituir a conexão ao repositório de mensagem local e abrir repositório de servidor remoto. Observe que você não pode abrir um repositório do Exchange no modo de cache e no modo em cache não ao mesmo tempo na mesma sessão MAPI. Se você já abriu o armazenamento de mensagens em cache, você deve fechar ou o repositório antes de abri-lo com esse sinalizador ou abra uma nova sessão MAPI, onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |Um cliente pode chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , definindo o sinalizador **NON_EMS_XP_SAVE** no parâmetro _ulFlags_ para indicar que a mensagem não foi entregue a partir de um servidor Exchange. Esse sinalizador deve ser usado em conjunto com o sinalizador **ITEMPROC_FORCE** no parâmetro _ulFlags_ para indicar um repositório PST que a mensagem é qualificada para regras de processamento antes do PST repositório notifica qualquer cliente escuta de chegada do Mensagem. Isso as regras de processamento só se aplica às novas mensagens que são criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não seja um servidor do Exchange (nesse caso o servidor do Exchange seria já processados regras na mensagem).  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Um cliente pode chamar [IMAPIProp::SaveChanges](imapiprop-savechanges.md), definindo o sinalizador **SPAMFILTER_ONSAVE** no parâmetro _ulFlags_ para habilitar uma mensagem que está sendo salvo de filtragem de spam. Suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente é Simple Mail Transfer Protocol (SMTP) e a mensagem está sendo salva um repositório para um arquivo de pastas particulares (. PST).  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Se esse sinalizador é definido na [Propriedade canônico de PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de um repositório PST encapsulado, indica que, quando uma nova mensagem chega na loja, o repositório tiver regras e filtragem de spam processadas na mensagem separadamente. O repositório chama [IMAPISupport::Notify](imapisupport-notify.md), a definição de **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e passar os detalhes da nova mensagem para um cliente de escutando. Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem.  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |Se esse sinalizador é incluído na [Propriedade canônico de PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), indica que o repositório suporta o armazenamento de Unicode. Um cliente pode consultar a presença do sinalizador para decidir se deseja solicitar ou salvar a informação de Unicode para o repositório.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Definições de itens em uma pasta de arquivamento

As seguintes definições constantes são valores usados para definir a [Propriedade canônico de PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Definições de exibição de objetos remotos

As definições de constante e a macro a seguir são para a exibição de objetos remotos. Para obter mais informações, consulte a [Propriedade canônico de PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).
  
```cpp
#define DTE_FLAG_REMOTE_VALID0x80000000 
#define DTE_FLAG_ACL_CAPABLE    0x40000000 
#define DTE_MASK_REMOTE        0x0000ff00 
#define DTE_MASK_LOCAL        0x000000ff 
  
#define DTE_IS_REMOTE_VALID(v)(!!((v) & DTE_FLAG_REMOTE_VALID)) 
#define DTE_IS_ACL_CAPABLE(v)(!!((v) & DTE_FLAG_ACL_CAPABLE)) 
#define DTE_REMOTE(v)(((v) & DTE_MASK_REMOTE) >> 8) 
#define DTE_LOCAL(v)((v) & DTE_MASK_LOCAL) 
  
#define DT_ROOM((ULONG) 0x00000007) 
#define DT_EQUIPMENT((ULONG) 0x00000008) 
#define DT_SEC_DISTLIST((ULONG) 0x00000009)
```

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Definições de catálogo de endereços do Exchange e mensagem armazenam os códigos de erro

O exemplo a seguir contém definições de códigos de erro para o catálogo de endereços do Exchange e o armazenamento de mensagens que têm a capacidade de reconexão. A última chamada para um Catálogo Global desconectados (GC) pode resultar em erro **MAPI_E_END_OF_SESSION** , que precisa ser repetidos. 
  
MAPI suporta reconexão do Outlook para um servidor GC sem reconfiguração especial, mas algum outro erro códigos podem ser retornados ao cliente.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Retornados quando uma conexão foi desconectada.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |Retornados quando o token de conexão de chamada de procedimento remoto (RPC) está desatualizado. Se o token da transação atual for diferente do token de conexão o que significa que ele tem reconectados, portanto **MAPI_E_RECONNECTED** é retornado e pode ser tratada da mesma forma **MAPI_E_END_OF_SESSION**. A chamada deve ser repetida.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Retornado quando a conexão estiver offline. Normalmente, isso significa que algo ocorreu no ambiente, como falha do servidor ou perda de conectividade de rede. Esse erro é mais provável ocorrer ao usar o modo cache perfil e tentar ignorar o cache para se comunicar com o servidor. Se o cache nunca conseguiu inicialmente estabelecer uma conexão ao servidor, talvez seja no estado em que **MAPI_E_OFFLINE** poderia representar offline.  <br/> |
   
Nenhum dos dois erros anteriores serão retornados em todos os cenários em que eles provavelmente seriam exibidos aplicar. Na maioria dos casos, **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** serão retornados. Nenhuma serão exibidas usando o download de [cliente MAPI do Microsoft Exchange Server e Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) . 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Cotas do modo de cache de definições de caixa de correio do Exchange Server

As seguintes definições constantes são usadas pelo Microsoft Outlook 2010 e Microsoft Outlook 2013 para definir a troca de cache cotas de perfil de modo que são equivalentes para as cotas de caixa de correio do Exchange caso contrário, disponíveis apenas com um perfil online.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Essas propriedades mapeiam a suas propriedades online correspondentes e contêm os mesmos valores em quilobytes. PR_QUOTA_WARNING mapeia para PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND para PR_QUOTA_PROHIBIT_SEND_QUOTA e PR_QUOTA_RECEIVE para PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Definições para o formato da mensagem

As seguintes definições constantes são valores que são usados para definir a [Propriedade canônico de PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Definições para usando RPC sobre HTTP

Consulte o tópico da [Propriedade canônico de PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) para definições de constantes usada como sinalizadores para definir a propriedade. 
  
Consulte o tópico da [Propriedade canônico de PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) para definições de constantes usada para definir a propriedade. 
  
### <a name="identifiers"></a>Identificadores

Use o `DEFINE_OLEGUID` macro definida em guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar os seguintes nomes simbólicos de GUID com seus valores. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

O identificador a seguir se destina a seção de perfil de Capone de um catálogo de endereços, que contém uma propriedade [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que desativa efetivamente o padrão para oferecer suporte a várias caixas de correio do Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contêiner especificado pelo [SetDefaultDir](iaddrbook-setdefaultdir.md).
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>Identificadores de interface

#### <a name="imapisync"></a>IMAPISync
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a>IMAPISyncProgressCallback
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a>IID_IContabAdmin
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a>IID_IMAPISECUREMESSAGE
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a>IID_IMAPIGetSession
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a>Identificadores de interface do manipulador de substituição de PST

#### <a name="iidipstoverridereq"></a>IID_IPSTOVERRIDEREQ
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a>IID_IPSTOVERRIDE1
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a>Confira também

- [Sobre as adições de MAPI](about-mapi-additions.md) 
- [Sobre as propriedades nomeadas usadas pelo Outlook](about-named-properties-used-by-outlook.md)
- [Acessar um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Abrir um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Gerenciar mensagens em um OST sem solicitar uma sincronização do modo cache do Exchange](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

