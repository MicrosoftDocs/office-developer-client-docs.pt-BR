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
ms.openlocfilehash: e35760ddb20f40a176d789be2db6c282fac05af8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586302"
---
# <a name="mapi-constants"></a><span data-ttu-id="11d19-103">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="11d19-103">MAPI constants</span></span>

<span data-ttu-id="11d19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11d19-105">Este tópico contém as definições de constantes, declarações de interface MAPI e identificadores de classe e de interface usados pelas APIs de MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="11d19-106">Identificadores de classe e interface</span><span class="sxs-lookup"><span data-stu-id="11d19-106">Class and interface identifiers</span></span>

<span data-ttu-id="11d19-107">Use a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar nomes simbólicos de identificador globalmente exclusivo (GUID) com seus valores, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="11d19-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="11d19-108">API de conversão de segurança de anexo</span><span class="sxs-lookup"><span data-stu-id="11d19-108">Attachment security conversion API</span></span>

<span data-ttu-id="11d19-109">Esta seção contém as definições de constantes e os identificadores de interface para a API de segurança de anexo.</span><span class="sxs-lookup"><span data-stu-id="11d19-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="11d19-110">Use a macro MAPIMETHOD definida no mapidefs.h de arquivo de cabeçalho do SDK do Windows para definir a função virtual pura **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span><span class="sxs-lookup"><span data-stu-id="11d19-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="11d19-111">Use a macro DECLARE_MAPI_INTERFACE_ definida no mapidefs.h de arquivo de cabeçalho do SDK do Windows para definir a tabela de método virtual para **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="11d19-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="11d19-112">API de conversão de MIME MAPI</span><span class="sxs-lookup"><span data-stu-id="11d19-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="11d19-113">Esta seção contém definições de constantes e os identificadores de classe e a interface para a API de conversão de MIME de MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="11d19-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="11d19-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11d19-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="11d19-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="11d19-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="11d19-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="11d19-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="11d19-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="11d19-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="11d19-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="11d19-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="11d19-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="11d19-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="11d19-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="11d19-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="11d19-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="11d19-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="11d19-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="11d19-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="11d19-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="11d19-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="11d19-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="11d19-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="11d19-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="11d19-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="11d19-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="11d19-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="11d19-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="11d19-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="11d19-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="11d19-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="11d19-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="11d19-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="11d19-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="11d19-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="11d19-131">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="11d19-132">*Conforme definido em Winerror de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="11d19-132">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="11d19-133">Identificadores de classe</span><span class="sxs-lookup"><span data-stu-id="11d19-133">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="11d19-134">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="11d19-134">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="11d19-135">API de estado offline</span><span class="sxs-lookup"><span data-stu-id="11d19-135">Offline State API</span></span>

<span data-ttu-id="11d19-136">Esta seção contém definições de constantes e os identificadores de classe e a interface para a API de estado Offline.</span><span class="sxs-lookup"><span data-stu-id="11d19-136">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="11d19-137">Constantes</span><span class="sxs-lookup"><span data-stu-id="11d19-137">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11d19-138">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="11d19-138">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="11d19-139">*Conforme definido em Winerror de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows*</span><span class="sxs-lookup"><span data-stu-id="11d19-139">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="11d19-140">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="11d19-140">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="11d19-141">*Conforme definido em Winerror de arquivo de cabeçalho do Windows (SDK)*</span><span class="sxs-lookup"><span data-stu-id="11d19-141">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="11d19-142">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="11d19-142">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="11d19-143">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="11d19-143">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="11d19-144">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="11d19-144">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="11d19-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="11d19-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="11d19-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="11d19-146">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="11d19-147">1</span><span class="sxs-lookup"><span data-stu-id="11d19-147">1</span></span>  <br/> |
|<span data-ttu-id="11d19-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="11d19-148">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="11d19-149">0x1</span><span class="sxs-lookup"><span data-stu-id="11d19-149">0x1</span></span>  <br/> |
|<span data-ttu-id="11d19-150">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="11d19-150">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="11d19-151">0x2</span><span class="sxs-lookup"><span data-stu-id="11d19-151">0x2</span></span>  <br/> |
|<span data-ttu-id="11d19-152">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="11d19-152">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="11d19-153">0x00002000</span><span class="sxs-lookup"><span data-stu-id="11d19-153">0x00002000</span></span>  <br/> |
|<span data-ttu-id="11d19-154">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="11d19-154">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="11d19-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="11d19-155">0x00000000</span></span>  <br/> |
|<span data-ttu-id="11d19-156">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="11d19-156">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="11d19-157">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="11d19-157">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="11d19-158">**Online ou offline**</span><span class="sxs-lookup"><span data-stu-id="11d19-158">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="11d19-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="11d19-159">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="11d19-160">0x00000003</span><span class="sxs-lookup"><span data-stu-id="11d19-160">0x00000003</span></span>  <br/> |
|<span data-ttu-id="11d19-161">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="11d19-161">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="11d19-162">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-162">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-163">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="11d19-163">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="11d19-164">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-164">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="11d19-165">Identificadores de classe</span><span class="sxs-lookup"><span data-stu-id="11d19-165">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="11d19-166">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="11d19-166">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="11d19-167">Propriedades nomeado do Outlook</span><span class="sxs-lookup"><span data-stu-id="11d19-167">Outlook named properties</span></span>

<span data-ttu-id="11d19-168">Esta seção contém as definições de constantes para propriedades nomeadas e seus namespaces e outras constantes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="11d19-168">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="11d19-169">Definições de propriedades nomeadas</span><span class="sxs-lookup"><span data-stu-id="11d19-169">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="11d19-170">Definições de namespaces</span><span class="sxs-lookup"><span data-stu-id="11d19-170">Definitions for namespaces</span></span>

<span data-ttu-id="11d19-171">Os seguintes identificadores identificador global exclusivos (GUIDs) representam os namespaces das propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="11d19-171">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="11d19-172">Consulte a seção repositório MAPI para as definições de PSETID.</span><span class="sxs-lookup"><span data-stu-id="11d19-172">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="11d19-173">Outras constantes</span><span class="sxs-lookup"><span data-stu-id="11d19-173">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11d19-174">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="11d19-174">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="11d19-175">0xD000000</span><span class="sxs-lookup"><span data-stu-id="11d19-175">0xD000000</span></span>  <br/> |
|<span data-ttu-id="11d19-176">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="11d19-176">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="11d19-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="11d19-177">0x2000000</span></span>  <br/> |
|<span data-ttu-id="11d19-178">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="11d19-178">MNID_ID</span></span>  <br/> | <span data-ttu-id="11d19-179">*Conforme definido em mapidefs.h de arquivo de cabeçalho.*</span><span class="sxs-lookup"><span data-stu-id="11d19-179">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="11d19-180">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="11d19-180">MNID_STRING</span></span>  <br/> | <span data-ttu-id="11d19-181">*Conforme definido em mapidefs.h de arquivo de cabeçalho.*</span><span class="sxs-lookup"><span data-stu-id="11d19-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="11d19-182">mtgNone</span><span class="sxs-lookup"><span data-stu-id="11d19-182">mtgNone</span></span>  <br/> |<span data-ttu-id="11d19-183">0x0</span><span class="sxs-lookup"><span data-stu-id="11d19-183">0x0</span></span>  <br/> |
|<span data-ttu-id="11d19-184">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="11d19-184">mtgRequest</span></span>  <br/> |<span data-ttu-id="11d19-185">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-185">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-186">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="11d19-186">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="11d19-187">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-187">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-188">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="11d19-188">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="11d19-189">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11d19-189">0x00020000</span></span>  <br/> |
|<span data-ttu-id="11d19-190">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="11d19-190">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="11d19-191">0x00080000</span><span class="sxs-lookup"><span data-stu-id="11d19-191">0x00080000</span></span>  <br/> |
|<span data-ttu-id="11d19-192">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="11d19-192">mtgDelegated</span></span>  <br/> |<span data-ttu-id="11d19-193">0x00100000</span><span class="sxs-lookup"><span data-stu-id="11d19-193">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="11d19-194">API de replicação</span><span class="sxs-lookup"><span data-stu-id="11d19-194">Replication API</span></span>

<span data-ttu-id="11d19-195">Esta seção contém as definições de constantes, declarações de interface MAPI e identificadores de classe e a interface para a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="11d19-195">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="11d19-196">Constantes</span><span class="sxs-lookup"><span data-stu-id="11d19-196">Constants</span></span>

<span data-ttu-id="11d19-197">A seguir está uma estrutura [MAPIUID](mapiuid.md) que identifica um provedor de serviços MAPI:</span><span class="sxs-lookup"><span data-stu-id="11d19-197">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="11d19-198">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-198">DNH_OK</span></span>  <br/> |<span data-ttu-id="11d19-199">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-199">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-200">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-200">DNT_OK</span></span>  <br/> |<span data-ttu-id="11d19-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-202">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="11d19-202">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="11d19-203">0x00000008</span><span class="sxs-lookup"><span data-stu-id="11d19-203">0x00000008</span></span>  <br/> |
|<span data-ttu-id="11d19-204">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="11d19-204">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="11d19-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11d19-205">0x00000010</span></span>  <br/> |
|<span data-ttu-id="11d19-206">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-206">HSF_OK</span></span>  <br/> |<span data-ttu-id="11d19-207">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-207">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-208">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11d19-208">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="11d19-209">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="11d19-209">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="11d19-210">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="11d19-210">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="11d19-211">((ULONG) 0X00001000)</span><span class="sxs-lookup"><span data-stu-id="11d19-211">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="11d19-212">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="11d19-212">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="11d19-213">((ULONG) 0X00000002)</span><span class="sxs-lookup"><span data-stu-id="11d19-213">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="11d19-214">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="11d19-214">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="11d19-215">0</span><span class="sxs-lookup"><span data-stu-id="11d19-215">0</span></span>  <br/> |
|<span data-ttu-id="11d19-216">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="11d19-216">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="11d19-217">1</span><span class="sxs-lookup"><span data-stu-id="11d19-217">1</span></span>  <br/> |
|<span data-ttu-id="11d19-218">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="11d19-218">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="11d19-219">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-219">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-220">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="11d19-220">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="11d19-221">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-221">0x00000002</span></span>  <br/> |
|<span data-ttu-id="11d19-222">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="11d19-222">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="11d19-223">0x00000040</span><span class="sxs-lookup"><span data-stu-id="11d19-223">0x00000040</span></span>  <br/> |
|<span data-ttu-id="11d19-224">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="11d19-224">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="11d19-225">0x00000080</span><span class="sxs-lookup"><span data-stu-id="11d19-225">0x00000080</span></span>  <br/> |
|<span data-ttu-id="11d19-226">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="11d19-226">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="11d19-227">0x00000200</span><span class="sxs-lookup"><span data-stu-id="11d19-227">0x00000200</span></span>  <br/> |
|<span data-ttu-id="11d19-228">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="11d19-228">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="11d19-229">0x00001000</span><span class="sxs-lookup"><span data-stu-id="11d19-229">0x00001000</span></span>  <br/> |
|<span data-ttu-id="11d19-230">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="11d19-230">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="11d19-231">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11d19-231">0x00020000</span></span>  <br/> |
|<span data-ttu-id="11d19-232">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="11d19-232">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="11d19-233">0x02000000</span><span class="sxs-lookup"><span data-stu-id="11d19-233">0x02000000</span></span>  <br/> |
|<span data-ttu-id="11d19-234">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-234">UPC_OK</span></span>  <br/> |<span data-ttu-id="11d19-235">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-235">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-236">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="11d19-236">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="11d19-237">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-237">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-238">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="11d19-238">UPD_MOV</span></span>  <br/> |<span data-ttu-id="11d19-239">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-239">0x00000002</span></span>  <br/> |
|<span data-ttu-id="11d19-240">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-240">UPD_OK</span></span>  <br/> |<span data-ttu-id="11d19-241">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-241">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-242">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="11d19-242">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="11d19-243">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11d19-243">0x00020000</span></span>  <br/> |
|<span data-ttu-id="11d19-244">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="11d19-244">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="11d19-245">0x00040000</span><span class="sxs-lookup"><span data-stu-id="11d19-245">0x00040000</span></span>  <br/> |
|<span data-ttu-id="11d19-246">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="11d19-246">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="11d19-247">0x00080000</span><span class="sxs-lookup"><span data-stu-id="11d19-247">0x00080000</span></span>  <br/> |
|<span data-ttu-id="11d19-248">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="11d19-248">UPF_NEW</span></span>  <br/> |<span data-ttu-id="11d19-249">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-249">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-250">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="11d19-250">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="11d19-251">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-251">0x00000002</span></span>  <br/> |
|<span data-ttu-id="11d19-252">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="11d19-252">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="11d19-253">0x00000004</span><span class="sxs-lookup"><span data-stu-id="11d19-253">0x00000004</span></span>  <br/> |
|<span data-ttu-id="11d19-254">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="11d19-254">UPF_DEL</span></span>  <br/> |<span data-ttu-id="11d19-255">0x00000008</span><span class="sxs-lookup"><span data-stu-id="11d19-255">0x00000008</span></span>  <br/> |
|<span data-ttu-id="11d19-256">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-256">UPF_OK</span></span>  <br/> |<span data-ttu-id="11d19-257">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-257">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-258">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-258">UPH_OK</span></span>  <br/> |<span data-ttu-id="11d19-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-260">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="11d19-260">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="11d19-261">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-261">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-262">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="11d19-262">UPM_NEW</span></span>  <br/> |<span data-ttu-id="11d19-263">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-263">0x00000002</span></span>  <br/> |
|<span data-ttu-id="11d19-264">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="11d19-264">UPM_MOV</span></span>  <br/> |<span data-ttu-id="11d19-265">0x00000004</span><span class="sxs-lookup"><span data-stu-id="11d19-265">0x00000004</span></span>  <br/> |
|<span data-ttu-id="11d19-266">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="11d19-266">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="11d19-267">0x00000008</span><span class="sxs-lookup"><span data-stu-id="11d19-267">0x00000008</span></span>  <br/> |
|<span data-ttu-id="11d19-268">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="11d19-268">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="11d19-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11d19-269">0x00000010</span></span>  <br/> |
|<span data-ttu-id="11d19-270">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-270">UPM_OK</span></span>  <br/> |<span data-ttu-id="11d19-271">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-271">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-272">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="11d19-272">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="11d19-273">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11d19-273">0x00020000</span></span>  <br/> |
|<span data-ttu-id="11d19-274">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="11d19-274">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="11d19-275">0x00040000</span><span class="sxs-lookup"><span data-stu-id="11d19-275">0x00040000</span></span>  <br/> |
|<span data-ttu-id="11d19-276">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="11d19-276">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="11d19-277">0x00080000</span><span class="sxs-lookup"><span data-stu-id="11d19-277">0x00080000</span></span>  <br/> |
|<span data-ttu-id="11d19-278">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="11d19-278">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="11d19-279">0x00100000</span><span class="sxs-lookup"><span data-stu-id="11d19-279">0x00100000</span></span>  <br/> |
|<span data-ttu-id="11d19-280">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="11d19-280">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="11d19-281">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-281">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-282">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="11d19-282">UPR_READ</span></span>  <br/> |<span data-ttu-id="11d19-283">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-283">0x00000002</span></span>  <br/> |
|<span data-ttu-id="11d19-284">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-284">UPR_OK</span></span>  <br/> |<span data-ttu-id="11d19-285">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-285">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-286">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="11d19-286">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="11d19-287">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11d19-287">0x00020000</span></span>  <br/> |
|<span data-ttu-id="11d19-288">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="11d19-288">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="11d19-289">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-289">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-290">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="11d19-290">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="11d19-291">0x00000002</span><span class="sxs-lookup"><span data-stu-id="11d19-291">0x00000002</span></span>  <br/> |
|<span data-ttu-id="11d19-292">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="11d19-292">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="11d19-293">0x00000004</span><span class="sxs-lookup"><span data-stu-id="11d19-293">0x00000004</span></span>  <br/> |
|<span data-ttu-id="11d19-294">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="11d19-294">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="11d19-295">0x00000080</span><span class="sxs-lookup"><span data-stu-id="11d19-295">0x00000080</span></span>  <br/> |
|<span data-ttu-id="11d19-296">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-296">UPS_OK</span></span>  <br/> |<span data-ttu-id="11d19-297">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-297">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-298">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-298">UPT_OK</span></span>  <br/> |<span data-ttu-id="11d19-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-300">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="11d19-300">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="11d19-301">0x00000001</span><span class="sxs-lookup"><span data-stu-id="11d19-301">0x00000001</span></span>  <br/> |
|<span data-ttu-id="11d19-302">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="11d19-302">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="11d19-303">0x00010000</span><span class="sxs-lookup"><span data-stu-id="11d19-303">0x00010000</span></span>  <br/> |
|<span data-ttu-id="11d19-304">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="11d19-304">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="11d19-305">0x00020000</span><span class="sxs-lookup"><span data-stu-id="11d19-305">0x00020000</span></span>  <br/> |
|<span data-ttu-id="11d19-306">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="11d19-306">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="11d19-307">0x00040000</span><span class="sxs-lookup"><span data-stu-id="11d19-307">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="11d19-308">Declarações de interface</span><span class="sxs-lookup"><span data-stu-id="11d19-308">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="11d19-309">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="11d19-309">Interface identifiers</span></span>

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

<span data-ttu-id="11d19-310">Use os dois seguintes identificadores de interface com [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)ou [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir e ignorar qualquer seleção provedor em um objeto folder e um objeto de mensagem, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="11d19-310">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="11d19-311">Repositório MAPI</span><span class="sxs-lookup"><span data-stu-id="11d19-311">MAPI store</span></span>

<span data-ttu-id="11d19-312">Esta seção contém as definições de constantes e identificadores de interface usado pela APIs essa interface com um repositório MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-312">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="11d19-313">Constantes</span><span class="sxs-lookup"><span data-stu-id="11d19-313">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="11d19-314">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="11d19-314">fnevIndexing</span></span>  <br/> |<span data-ttu-id="11d19-315">((ULONG) 0X00010000)</span><span class="sxs-lookup"><span data-stu-id="11d19-315">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="11d19-316">Um provedor de armazenamento pode especificar **fnevIndexing** no membro **ulEventType** da estrutura de **[notificação](notification.md)** para notificar o indexador que um objeto está pronto para indexação.</span><span class="sxs-lookup"><span data-stu-id="11d19-316">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="11d19-317">O membro **info** da estrutura de **notificação** contém uma estrutura **[EXTENDED_NOTIFICATION](extended_notification.md)** .</span><span class="sxs-lookup"><span data-stu-id="11d19-317">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="11d19-318">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="11d19-318">FS_NONE</span></span>  <br/> |<span data-ttu-id="11d19-319">0x00</span><span class="sxs-lookup"><span data-stu-id="11d19-319">0x00</span></span>  <br/> |<span data-ttu-id="11d19-320">Um cliente pode chamar **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** e a seleção para o bitmask retornado.</span><span class="sxs-lookup"><span data-stu-id="11d19-320">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="11d19-321">**FS_NONE** indica que a pasta não oferece suporte a compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="11d19-321">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="11d19-322">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="11d19-322">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="11d19-323">0x01</span><span class="sxs-lookup"><span data-stu-id="11d19-323">0x01</span></span>  <br/> |<span data-ttu-id="11d19-324">Um cliente pode chamar **IFolderSupport::GetSupportMask** e a seleção para o bitmask retornado.</span><span class="sxs-lookup"><span data-stu-id="11d19-324">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="11d19-325">**FS_SUPPORTS_SHARING** indica que a pasta oferece suporte a compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="11d19-325">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="11d19-326">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="11d19-326">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="11d19-327">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="11d19-327">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="11d19-328">Identifica o processo que está fazendo com que uma notificação para um indexador que um objeto está pronto para indexação.</span><span class="sxs-lookup"><span data-stu-id="11d19-328">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="11d19-329">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="11d19-329">MNID_ID</span></span>  <br/> |<span data-ttu-id="11d19-330">Conforme definido em mapidefs.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="11d19-330">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="11d19-331">Um valor para o campo **ulKind** da estrutura **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="11d19-331">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="11d19-332">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="11d19-332">MNID_STRING</span></span>  <br/> |<span data-ttu-id="11d19-333">Conforme definido em mapidefs.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="11d19-333">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="11d19-334">Um valor para o campo **ulKind** da estrutura **[MAPINAMEID](mapinameid.md)** .</span><span class="sxs-lookup"><span data-stu-id="11d19-334">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="11d19-335">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="11d19-335">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="11d19-336">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="11d19-336">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="11d19-337">Se um cliente especifica **MSCAP_SEL_RESTRICTION** em *mscapSelector* para **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** pode retornar esse valor se o repositório ignora os parâmetros inválidos em uma restrição.</span><span class="sxs-lookup"><span data-stu-id="11d19-337">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="11d19-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="11d19-338">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="11d19-339">((ULONG) 0X00000020)</span><span class="sxs-lookup"><span data-stu-id="11d19-339">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="11d19-340">Se um cliente especifica **MSCAP_SEL_FOLDER** em *mscapSelector* para **IMSCapabilities::GetCapabilities**, **GetCapabilities** pode retornar esse valor se o repositório for um repositório não padrão que ofereça suporte a home pages da pasta.</span><span class="sxs-lookup"><span data-stu-id="11d19-340">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="11d19-341">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-341">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="11d19-342">((ULONG) 0X00800000)</span><span class="sxs-lookup"><span data-stu-id="11d19-342">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="11d19-343">Um cliente pode obter a propriedade **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** para determinar as características de um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11d19-343">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="11d19-344">Se o provedor de armazenamento define o sinalizador **STORE_PUSHER_OK** no bitmask, isso significa que o manipulador de protocolo MAPI não irá rastrear o repositório e o armazenamento é responsável por push quaisquer alterações por meio de notificações para o indexador para ter mensagens indexadas.</span><span class="sxs-lookup"><span data-stu-id="11d19-344">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="11d19-345">Definições de namespaces</span><span class="sxs-lookup"><span data-stu-id="11d19-345">Definitions for namespaces</span></span>

<span data-ttu-id="11d19-346">Os seguintes identificadores identificador global exclusivos (GUIDs) representam os namespaces propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="11d19-346">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="11d19-347">Eles são indexados pelo manipulador de protocolo MAPI (PH) e são documentados como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="11d19-347">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="11d19-348">As propriedades nomeadas não devem ser usadas para criar ou modificar os itens.</span><span class="sxs-lookup"><span data-stu-id="11d19-348">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="11d19-349">Propriedades MNID_ID</span><span class="sxs-lookup"><span data-stu-id="11d19-349">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="11d19-350">Propriedades MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="11d19-350">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="11d19-351">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="11d19-351">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="11d19-352">Use o `DEFINE_OLEGUID` macro definida em guiddef.h de arquivo de cabeçalho do SDK do Windows para associar o seguinte nome simbólico GUID seu valor.</span><span class="sxs-lookup"><span data-stu-id="11d19-352">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="11d19-353">Constantes de catálogo de endereços de MAPI</span><span class="sxs-lookup"><span data-stu-id="11d19-353">MAPI Address Book constants</span></span>

<span data-ttu-id="11d19-354">Esta seção contém as definições de constantes para o catálogo de endereços de MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-354">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="11d19-355">Constantes</span><span class="sxs-lookup"><span data-stu-id="11d19-355">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="11d19-356">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="11d19-356">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="11d19-357">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="11d19-357">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="11d19-358">A pasta raiz para um objeto de catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-358">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="11d19-359">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="11d19-359">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="11d19-360">((ULONG) 0X00000002)</span><span class="sxs-lookup"><span data-stu-id="11d19-360">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="11d19-361">Uma subpasta contida na pasta raiz do objeto de catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-361">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="11d19-362">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="11d19-362">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="11d19-363">((ULONG) 0X00000003)</span><span class="sxs-lookup"><span data-stu-id="11d19-363">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="11d19-364">Um objeto de contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="11d19-364">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="11d19-365">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="11d19-365">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="11d19-366">((ULONG) 0X00000004)</span><span class="sxs-lookup"><span data-stu-id="11d19-366">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="11d19-367">Um objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11d19-367">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="11d19-368">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="11d19-368">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="11d19-369">((ULONG) 0X00000005)</span><span class="sxs-lookup"><span data-stu-id="11d19-369">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="11d19-370">Um objeto de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="11d19-370">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="11d19-371">Constantes MAPI adicionais</span><span class="sxs-lookup"><span data-stu-id="11d19-371">Additional MAPI constants</span></span>

<span data-ttu-id="11d19-372">Esta seção contém definições constantes, incluindo códigos de erro e os identificadores de interface usados pelo APIs de MAPI não anteriormente expostos e documentadas.</span><span class="sxs-lookup"><span data-stu-id="11d19-372">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="11d19-373">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="11d19-373">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="11d19-374">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="11d19-374">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="11d19-375">Quando um cliente chama o método [IAddrBook::Details](iaddrbook-details.md) , o cliente deve definir o sinalizador **DIALOG_MODAL** no parâmetro _ulFlags_ para exibir a caixa de diálogo modal mostrando os detalhes sobre uma entrada de catálogo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="11d19-375">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="11d19-376">Essa constante é definido em mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="11d19-376">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="11d19-377">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="11d19-377">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="11d19-378">0x00000800</span><span class="sxs-lookup"><span data-stu-id="11d19-378">0x00000800</span></span>  <br/> |<span data-ttu-id="11d19-379">No Outlook 2007, repositórios de PST com quebra têm regras e filtragem de spam processado em novas mensagens, antes de clientes MAPI são notificados das novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="11d19-379">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="11d19-380">Um cliente usando o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem em repositórios de PST ou o provedor deve definir o sinalizador **ITEMPROC_FORCE** no parâmetro _ulFlags_ do método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar ao arquivo PST as regras de repositório que a mensagem é qualificada para processamento antes que o repositório notificará qualquer cliente escuta a partir da chegada da nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="11d19-380">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="11d19-381">Observe que tais regras processamento só se aplica às novas mensagens criadas em um servidor que não seja um Microsoft Exchange Server, pois o Exchange Server processa as regras para mensagens no servidor.</span><span class="sxs-lookup"><span data-stu-id="11d19-381">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="11d19-382">Daí o provedor ou criar a mensagem de cliente deve passar por esse sinalizador em combinação com **NON_EMS_XP_SAVE**, indicando que o servidor não é um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="11d19-382">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="11d19-383">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="11d19-383">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="11d19-384">0x00200000</span><span class="sxs-lookup"><span data-stu-id="11d19-384">0x00200000</span></span>  <br/> |<span data-ttu-id="11d19-385">Um cliente pode chamar a função [MAPILogonEx](mapilogonex.md) , definindo o sinalizador **MAPI_BG_SESSION** no parâmetro _flFlags_ para efetuar logon em uma sessão e realizar qualquer operação em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="11d19-385">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="11d19-386">Em geral, se um cliente pretende fazer processamento em um segmento de plano de fundo ou em um processo separado no modo não invasiva para o segmento de primeiro plano, ele deve chamar [MAPILogonEx](mapilogonex.md) com o sinalizador **MAPI_BG_SESSION** .</span><span class="sxs-lookup"><span data-stu-id="11d19-386">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="11d19-387">Um exemplo em que esse recurso é usado é um aplicativo de cliente, como um mecanismo de indexação, abrindo um arquivo de pastas particulares (PST) para acesso de tipo de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="11d19-387">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="11d19-388">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="11d19-388">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="11d19-389">0x00004000</span><span class="sxs-lookup"><span data-stu-id="11d19-389">0x00004000</span></span>  <br/> |<span data-ttu-id="11d19-390">Um cliente pode chamar o método [IAddrBook::OpenEntry](iaddrbook-openentry.md) , definindo o sinalizador **MAPI_CACHE_ONLY** no parâmetro _ulFlags_ para abrir uma entrada do catálogo de endereços e para acessá-lo subsequentemente apenas do cache.</span><span class="sxs-lookup"><span data-stu-id="11d19-390">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="11d19-391">Um exemplo em que esse recurso é usado é um aplicativo cliente que deseja abrir a lista de endereços Global no modo cache do Exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="11d19-391">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="11d19-392">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="11d19-392">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="11d19-393">0x0000000c</span><span class="sxs-lookup"><span data-stu-id="11d19-393">0x0000000C</span></span>  <br/> |<span data-ttu-id="11d19-394">Esse valor pode ser passado para a função de MAPISendMail de MAPI simples no parâmetro _ulFlags_ para especificar que uma caixa de diálogo sem janela restrita é exibida, o aplicativo de email padrão.</span><span class="sxs-lookup"><span data-stu-id="11d19-394">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="11d19-395">Se nem esse sinalizador nem MAPI_DIALOG (0x00000008) estiver definida, nenhuma caixa de diálogo é exibida.</span><span class="sxs-lookup"><span data-stu-id="11d19-395">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="11d19-396">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="11d19-396">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="11d19-397">0x00000200</span><span class="sxs-lookup"><span data-stu-id="11d19-397">0x00000200</span></span>  <br/> |<span data-ttu-id="11d19-398">Se o Microsoft Office Outlook está no modo cache do Exchange e um repositório foi aberto em modo de cache, um provedor de cliente ou serviço pode chamar [IMsgStore::OpenEntry](imsgstore-openentry.md), definindo o sinalizador **MAPI_NO_CACHE** no parâmetro _ulFlags_ para abrir um item ou um pasta em que o armazenamento remoto.</span><span class="sxs-lookup"><span data-stu-id="11d19-398">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="11d19-399">Observe que, se você abrir o armazenamento de mensagens com o sinalizador **MDB_ONLINE** no servidor remoto, você não precisará usar o sinalizador **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="11d19-399">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="11d19-400">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="11d19-400">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="11d19-401">0x80000000</span><span class="sxs-lookup"><span data-stu-id="11d19-401">0x80000000</span></span>  <br/> |<span data-ttu-id="11d19-402">Um provedor de cliente ou serviço pode chamar a função [OpenIMsgOnIStg](openimsgonistg.md) , definindo o sinalizador **MAPI_UNICODE** no parâmetro _ulFlags_ para criar os arquivos do. msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="11d19-402">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="11d19-403">O resultante [IMessage: IMAPIProp](imessageimapiprop.md) arquivo mostra **STORE_UNICODE_OK** em sua [Propriedade canônico de PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) e oferece suporte a Unicode propriedades.</span><span class="sxs-lookup"><span data-stu-id="11d19-403">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="11d19-404">Essa constante é definido em mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="11d19-404">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="11d19-405">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="11d19-405">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="11d19-406">0x00000100</span><span class="sxs-lookup"><span data-stu-id="11d19-406">0x00000100</span></span>  <br/> |<span data-ttu-id="11d19-407">Se o Outlook está no modo cache do Exchange, um provedor de cliente ou serviço pode chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) , definindo o sinalizador **MDB_ONLINE** no parâmetro _ulFlags_ para substituir a conexão ao repositório de mensagem local e abrir repositório de servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="11d19-407">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="11d19-408">Observe que você não pode abrir um repositório do Exchange no modo de cache e no modo em cache não ao mesmo tempo na mesma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="11d19-408">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="11d19-409">Se você já abriu o armazenamento de mensagens em cache, você deve fechar ou o repositório antes de abri-lo com esse sinalizador ou abra uma nova sessão MAPI, onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="11d19-409">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="11d19-410">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="11d19-410">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="11d19-411">0x00001000</span><span class="sxs-lookup"><span data-stu-id="11d19-411">0x00001000</span></span>  <br/> |<span data-ttu-id="11d19-412">Um cliente pode chamar o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) , definindo o sinalizador **NON_EMS_XP_SAVE** no parâmetro _ulFlags_ para indicar que a mensagem não foi entregue a partir de um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="11d19-412">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="11d19-413">Esse sinalizador deve ser usado em conjunto com o sinalizador **ITEMPROC_FORCE** no parâmetro _ulFlags_ para indicar um repositório PST que a mensagem é qualificada para regras de processamento antes do PST repositório notifica qualquer cliente escuta de chegada do Mensagem.</span><span class="sxs-lookup"><span data-stu-id="11d19-413">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="11d19-414">Isso as regras de processamento só se aplica às novas mensagens que são criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não seja um servidor do Exchange (nesse caso o servidor do Exchange seria já processados regras na mensagem).</span><span class="sxs-lookup"><span data-stu-id="11d19-414">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="11d19-415">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="11d19-415">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="11d19-416">0x00000080</span><span class="sxs-lookup"><span data-stu-id="11d19-416">0x00000080</span></span>  <br/> |<span data-ttu-id="11d19-417">Um cliente pode chamar [IMAPIProp::SaveChanges](imapiprop-savechanges.md), definindo o sinalizador **SPAMFILTER_ONSAVE** no parâmetro _ulFlags_ para habilitar uma mensagem que está sendo salvo de filtragem de spam.</span><span class="sxs-lookup"><span data-stu-id="11d19-417">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="11d19-418">Suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente é Simple Mail Transfer Protocol (SMTP) e a mensagem está sendo salva um repositório para um arquivo de pastas particulares (. PST).</span><span class="sxs-lookup"><span data-stu-id="11d19-418">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="11d19-419">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="11d19-419">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="11d19-420">0x00200000</span><span class="sxs-lookup"><span data-stu-id="11d19-420">0x00200000</span></span>  <br/> |<span data-ttu-id="11d19-421">Se esse sinalizador é definido na [Propriedade canônico de PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de um repositório PST encapsulado, indica que, quando uma nova mensagem chega na loja, o repositório tiver regras e filtragem de spam processadas na mensagem separadamente.</span><span class="sxs-lookup"><span data-stu-id="11d19-421">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="11d19-422">O repositório chama [IMAPISupport::Notify](imapisupport-notify.md), a definição de **fnevNewMail** na estrutura de [notificação](notification.md) que é passada como um parâmetro e passar os detalhes da nova mensagem para um cliente de escutando.</span><span class="sxs-lookup"><span data-stu-id="11d19-422">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="11d19-423">Subsequentemente, quando o cliente escutando recebe a notificação, ele não processar regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="11d19-423">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="11d19-424">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="11d19-424">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="11d19-425">0x00040000</span><span class="sxs-lookup"><span data-stu-id="11d19-425">0x00040000</span></span>  <br/> |<span data-ttu-id="11d19-426">Se esse sinalizador é incluído na [Propriedade canônico de PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), indica que o repositório suporta o armazenamento de Unicode.</span><span class="sxs-lookup"><span data-stu-id="11d19-426">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="11d19-427">Um cliente pode consultar a presença do sinalizador para decidir se deseja solicitar ou salvar a informação de Unicode para o repositório.</span><span class="sxs-lookup"><span data-stu-id="11d19-427">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="11d19-428">Definições de itens em uma pasta de arquivamento</span><span class="sxs-lookup"><span data-stu-id="11d19-428">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="11d19-429">As seguintes definições constantes são valores usados para definir a [Propriedade canônico de PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="11d19-429">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="11d19-430">Definições de exibição de objetos remotos</span><span class="sxs-lookup"><span data-stu-id="11d19-430">Definitions for displaying remote objects</span></span>

<span data-ttu-id="11d19-431">As definições de constante e a macro a seguir são para a exibição de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="11d19-431">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="11d19-432">Para obter mais informações, consulte a [Propriedade canônico de PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="11d19-432">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="11d19-433">Definições de catálogo de endereços do Exchange e mensagem armazenam os códigos de erro</span><span class="sxs-lookup"><span data-stu-id="11d19-433">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="11d19-434">O exemplo a seguir contém definições de códigos de erro para o catálogo de endereços do Exchange e o armazenamento de mensagens que têm a capacidade de reconexão.</span><span class="sxs-lookup"><span data-stu-id="11d19-434">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="11d19-435">A última chamada para um Catálogo Global desconectados (GC) pode resultar em erro **MAPI_E_END_OF_SESSION** , que precisa ser repetidos.</span><span class="sxs-lookup"><span data-stu-id="11d19-435">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="11d19-436">MAPI suporta reconexão do Outlook para um servidor GC sem reconfiguração especial, mas algum outro erro códigos podem ser retornados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="11d19-436">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="11d19-437">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="11d19-437">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="11d19-438">0x80040200</span><span class="sxs-lookup"><span data-stu-id="11d19-438">0x80040200</span></span>  <br/> |<span data-ttu-id="11d19-439">Retornados quando uma conexão foi desconectada.</span><span class="sxs-lookup"><span data-stu-id="11d19-439">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="11d19-440">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="11d19-440">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="11d19-441">0x80040125</span><span class="sxs-lookup"><span data-stu-id="11d19-441">0x80040125</span></span>  <br/> |<span data-ttu-id="11d19-442">Retornados quando o token de conexão de chamada de procedimento remoto (RPC) está desatualizado.</span><span class="sxs-lookup"><span data-stu-id="11d19-442">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="11d19-443">Se o token da transação atual for diferente do token de conexão o que significa que ele tem reconectados, portanto **MAPI_E_RECONNECTED** é retornado e pode ser tratada da mesma forma **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="11d19-443">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="11d19-444">A chamada deve ser repetida.</span><span class="sxs-lookup"><span data-stu-id="11d19-444">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="11d19-445">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="11d19-445">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="11d19-446">0x80040126</span><span class="sxs-lookup"><span data-stu-id="11d19-446">0x80040126</span></span>  <br/> |<span data-ttu-id="11d19-447">Retornado quando a conexão estiver offline.</span><span class="sxs-lookup"><span data-stu-id="11d19-447">Returned when the connection is offline.</span></span> <span data-ttu-id="11d19-448">Normalmente, isso significa que algo ocorreu no ambiente, como falha do servidor ou perda de conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="11d19-448">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="11d19-449">Esse erro é mais provável ocorrer ao usar o modo cache perfil e tentar ignorar o cache para se comunicar com o servidor.</span><span class="sxs-lookup"><span data-stu-id="11d19-449">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="11d19-450">Se o cache nunca conseguiu inicialmente estabelecer uma conexão ao servidor, talvez seja no estado em que **MAPI_E_OFFLINE** poderia representar offline.</span><span class="sxs-lookup"><span data-stu-id="11d19-450">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="11d19-451">Nenhum dos dois erros anteriores serão retornados em todos os cenários em que eles provavelmente seriam exibidos aplicar.</span><span class="sxs-lookup"><span data-stu-id="11d19-451">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="11d19-452">Na maioria dos casos, **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** serão retornados.</span><span class="sxs-lookup"><span data-stu-id="11d19-452">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="11d19-453">Nenhuma serão exibidas usando o download de [cliente MAPI do Microsoft Exchange Server e Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) .</span><span class="sxs-lookup"><span data-stu-id="11d19-453">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="11d19-454">Cotas do modo de cache de definições de caixa de correio do Exchange Server</span><span class="sxs-lookup"><span data-stu-id="11d19-454">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="11d19-455">As seguintes definições constantes são usadas pelo Microsoft Outlook 2010 e Microsoft Outlook 2013 para definir a troca de cache cotas de perfil de modo que são equivalentes para as cotas de caixa de correio do Exchange caso contrário, disponíveis apenas com um perfil online.</span><span class="sxs-lookup"><span data-stu-id="11d19-455">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="11d19-456">Essas propriedades mapeiam a suas propriedades online correspondentes e contêm os mesmos valores em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="11d19-456">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="11d19-457">PR_QUOTA_WARNING mapeia para PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND para PR_QUOTA_PROHIBIT_SEND_QUOTA e PR_QUOTA_RECEIVE para PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="11d19-457">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="11d19-458">Definições para o formato da mensagem</span><span class="sxs-lookup"><span data-stu-id="11d19-458">Definitions for message format</span></span>

<span data-ttu-id="11d19-459">As seguintes definições constantes são valores que são usados para definir a [Propriedade canônico de PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="11d19-459">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="11d19-460">Definições para usando RPC sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="11d19-460">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="11d19-461">Consulte o tópico da [Propriedade canônico de PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) para definições de constantes usada como sinalizadores para definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="11d19-461">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="11d19-462">Consulte o tópico da [Propriedade canônico de PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) para definições de constantes usada para definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="11d19-462">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="11d19-463">Identificadores</span><span class="sxs-lookup"><span data-stu-id="11d19-463">Identifiers</span></span>

<span data-ttu-id="11d19-464">Use o `DEFINE_OLEGUID` macro definida em guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar os seguintes nomes simbólicos de GUID com seus valores.</span><span class="sxs-lookup"><span data-stu-id="11d19-464">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="11d19-465">O identificador a seguir se destina a seção de perfil de Capone de um catálogo de endereços, que contém uma propriedade [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que desativa efetivamente o padrão para oferecer suporte a várias caixas de correio do Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contêiner especificado pelo [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="11d19-465">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="11d19-466">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="11d19-466">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="11d19-467">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="11d19-467">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="11d19-468">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="11d19-468">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="11d19-469">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="11d19-469">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="11d19-470">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="11d19-470">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="11d19-471">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="11d19-471">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="11d19-472">Identificadores de interface do manipulador de substituição de PST</span><span class="sxs-lookup"><span data-stu-id="11d19-472">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="11d19-473">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="11d19-473">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="11d19-474">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="11d19-474">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="11d19-475">Confira também</span><span class="sxs-lookup"><span data-stu-id="11d19-475">See also</span></span>

- [<span data-ttu-id="11d19-476">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="11d19-476">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="11d19-477">Sobre as propriedades nomeadas usadas pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="11d19-477">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="11d19-478">Acessar um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="11d19-478">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="11d19-479">Abrir um repositório em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="11d19-479">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="11d19-480">Gerenciar mensagens em um OST sem solicitar uma sincronização do modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="11d19-480">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

