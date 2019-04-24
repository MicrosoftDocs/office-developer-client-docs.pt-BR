---
title: Constantes de MAPI
manager: soliver
ms.date: 10/02/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: Definições constantes declarações de interface MAPI e identificadores de classe e interface usados pelo APIs MAPI.
ms.openlocfilehash: 343b777550d88276a1f5cad19f12ae7fc09c6244
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318918"
---
# <a name="mapi-constants"></a><span data-ttu-id="5793a-103">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="5793a-103">MAPI constants</span></span>

<span data-ttu-id="5793a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5793a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5793a-105">Esse tópico contém constantes declarações de interface MAPI e identificadores de classe e interface usados pelo APIs MAPI.</span><span class="sxs-lookup"><span data-stu-id="5793a-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="5793a-106">Identificadores de classe e interface</span><span class="sxs-lookup"><span data-stu-id="5793a-106">Class and interface identifiers</span></span>

<span data-ttu-id="5793a-107">Use a macro DEFINE_GUID estipulada no Microsoft Windows Software Development Kit (SDK do Windows) no arquivo cabeçalho guiddef.h para associar os nomes dos simbólico de identificador global exclusivo (GUID) com seus valores, a menos que indicado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5793a-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="5793a-108">API de conversão de segurança de anexos</span><span class="sxs-lookup"><span data-stu-id="5793a-108">Attachment security conversion API</span></span>

<span data-ttu-id="5793a-109">Esta seção contém definições constantes e identificadores interface para a API de segurança de anexos.</span><span class="sxs-lookup"><span data-stu-id="5793a-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="5793a-110">Use a macro MAPIMETHOD estipulada no arquivo cabeçalho mapidefs.h do SDK do Windows\* para definir a função virtual pura \*\* [IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5793a-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="5793a-111">Usar a macro DECLARE_MAPI_INTERFACE_ estipulada a no arquivo cabeçalho mapidefs.h do SDK do Windows\* para definir a tabela virtual método \*\* [IAttachmentSecurity](iattachmentsecurityiunknown.md)\*\*.</span><span class="sxs-lookup"><span data-stu-id="5793a-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="5793a-112">Sobre a API de conversão MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="5793a-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="5793a-113">Esta seção contém definições constantes e identificadores de classe e interface para a API de conversão de MAPI MIME.</span><span class="sxs-lookup"><span data-stu-id="5793a-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="5793a-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="5793a-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5793a-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="5793a-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="5793a-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="5793a-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="5793a-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="5793a-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="5793a-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="5793a-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="5793a-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="5793a-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="5793a-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="5793a-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="5793a-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="5793a-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="5793a-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="5793a-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="5793a-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="5793a-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="5793a-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="5793a-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="5793a-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="5793a-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="5793a-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="5793a-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="5793a-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="5793a-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="5793a-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="5793a-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="5793a-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="5793a-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="5793a-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="5793a-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="5793a-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5793a-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="5793a-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="5793a-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="5793a-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5793a-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="5793a-134">*Conforme definido no arquivo cabeçalho winerror.h* do Microsoft Software Development Kit do Windows (SDK do Windows)</span><span class="sxs-lookup"><span data-stu-id="5793a-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="5793a-135">Identificadores de classe</span><span class="sxs-lookup"><span data-stu-id="5793a-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="5793a-136">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="5793a-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="5793a-137">API de estado offline</span><span class="sxs-lookup"><span data-stu-id="5793a-137">Offline State API</span></span>

<span data-ttu-id="5793a-138">Esta seção contém definições constantes e identificadores de classe e interface para o API de estado offline.</span><span class="sxs-lookup"><span data-stu-id="5793a-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="5793a-139">Constantes</span><span class="sxs-lookup"><span data-stu-id="5793a-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5793a-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5793a-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="5793a-141">*Conforme definido no arquivo cabeçalho winerror.h* do Microsoft Software Development Kit do Windows (SDK do Windows)</span><span class="sxs-lookup"><span data-stu-id="5793a-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="5793a-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="5793a-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="5793a-143">*Conforme definido na Winerror de arquivo do cabeçalho (SDK) do Windows*</span><span class="sxs-lookup"><span data-stu-id="5793a-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="5793a-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5793a-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="5793a-145">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="5793a-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="5793a-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5793a-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="5793a-147">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="5793a-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="5793a-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="5793a-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="5793a-149">1</span><span class="sxs-lookup"><span data-stu-id="5793a-149">1</span></span>  <br/> |
|<span data-ttu-id="5793a-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5793a-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="5793a-151">0x1</span><span class="sxs-lookup"><span data-stu-id="5793a-151">0x1</span></span>  <br/> |
|<span data-ttu-id="5793a-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5793a-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="5793a-153">0x2</span><span class="sxs-lookup"><span data-stu-id="5793a-153">0x2</span></span>  <br/> |
|<span data-ttu-id="5793a-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="5793a-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="5793a-155">0x00002000</span><span class="sxs-lookup"><span data-stu-id="5793a-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="5793a-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5793a-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="5793a-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5793a-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="5793a-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="5793a-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="5793a-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="5793a-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="5793a-160">**Online ou offline**</span><span class="sxs-lookup"><span data-stu-id="5793a-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="5793a-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="5793a-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="5793a-162">0x00000003</span><span class="sxs-lookup"><span data-stu-id="5793a-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="5793a-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5793a-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="5793a-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5793a-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="5793a-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="5793a-167">Identificadores de classe</span><span class="sxs-lookup"><span data-stu-id="5793a-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="5793a-168">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="5793a-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="5793a-169">Propriedades denominadas do Outlook</span><span class="sxs-lookup"><span data-stu-id="5793a-169">Outlook named properties</span></span>

<span data-ttu-id="5793a-170">Esta seção contém definições constantes para propriedades nomeadas e suas namespaces e outras constantes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5793a-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="5793a-171">Definições para propriedades nomeadas:</span><span class="sxs-lookup"><span data-stu-id="5793a-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="5793a-172">Definições de namespaces</span><span class="sxs-lookup"><span data-stu-id="5793a-172">Definitions for namespaces</span></span>

<span data-ttu-id="5793a-173">Os seguintes identificadores globais exclusivos (GUIDs) representam os namespaces de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="5793a-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="5793a-174">Confira a seção MAPI Store para as definições de PSETID.</span><span class="sxs-lookup"><span data-stu-id="5793a-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="5793a-175">Outras constantes</span><span class="sxs-lookup"><span data-stu-id="5793a-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5793a-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="5793a-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="5793a-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="5793a-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="5793a-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="5793a-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="5793a-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="5793a-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="5793a-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="5793a-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="5793a-181">*Conforme definido em mapidefs.h de arquivo o cabeçalho.*</span><span class="sxs-lookup"><span data-stu-id="5793a-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="5793a-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5793a-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="5793a-183">*Conforme definido em mapidefs.h de arquivo o cabeçalho.*</span><span class="sxs-lookup"><span data-stu-id="5793a-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="5793a-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="5793a-184">mtgNone</span></span>  <br/> |<span data-ttu-id="5793a-185">0x0</span><span class="sxs-lookup"><span data-stu-id="5793a-185">0x0</span></span>  <br/> |
|<span data-ttu-id="5793a-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="5793a-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="5793a-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="5793a-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="5793a-189">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="5793a-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="5793a-191">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5793a-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="5793a-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="5793a-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="5793a-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="5793a-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="5793a-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="5793a-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="5793a-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="5793a-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="5793a-196">Replicação API</span><span class="sxs-lookup"><span data-stu-id="5793a-196">Replication API</span></span>

<span data-ttu-id="5793a-197">Esse tópico contém constantes declarações de interface MAPI e identificadores de classe e interface usados para a replicação do API.</span><span class="sxs-lookup"><span data-stu-id="5793a-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="5793a-198">Constantes</span><span class="sxs-lookup"><span data-stu-id="5793a-198">Constants</span></span>

<span data-ttu-id="5793a-199">A seguir uma [MAPIUID](mapiuid.md) estrutura para identificar um provedor de serviços MAPI:</span><span class="sxs-lookup"><span data-stu-id="5793a-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="5793a-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="5793a-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="5793a-203">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5793a-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="5793a-205">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5793a-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="5793a-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="5793a-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="5793a-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5793a-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="5793a-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="5793a-209">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5793a-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="5793a-211">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="5793a-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="5793a-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="5793a-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="5793a-213">((ULONG) 0X00001000)</span><span class="sxs-lookup"><span data-stu-id="5793a-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="5793a-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="5793a-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="5793a-215">((ULONG) 0X00000002)</span><span class="sxs-lookup"><span data-stu-id="5793a-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="5793a-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="5793a-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="5793a-217">,0</span><span class="sxs-lookup"><span data-stu-id="5793a-217">0</span></span>  <br/> |
|<span data-ttu-id="5793a-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="5793a-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="5793a-219">1</span><span class="sxs-lookup"><span data-stu-id="5793a-219">1</span></span>  <br/> |
|<span data-ttu-id="5793a-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5793a-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="5793a-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="5793a-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="5793a-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="5793a-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5793a-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="5793a-225">0x00000040</span><span class="sxs-lookup"><span data-stu-id="5793a-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="5793a-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="5793a-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="5793a-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5793a-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="5793a-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="5793a-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="5793a-229">0x00000200</span><span class="sxs-lookup"><span data-stu-id="5793a-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="5793a-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="5793a-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="5793a-231">0x00001000</span><span class="sxs-lookup"><span data-stu-id="5793a-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="5793a-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="5793a-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="5793a-233">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5793a-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="5793a-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="5793a-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="5793a-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="5793a-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="5793a-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="5793a-237">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="5793a-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="5793a-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="5793a-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="5793a-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="5793a-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="5793a-243">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="5793a-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="5793a-245">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5793a-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="5793a-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="5793a-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="5793a-247">0x00040000</span><span class="sxs-lookup"><span data-stu-id="5793a-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="5793a-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="5793a-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="5793a-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="5793a-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="5793a-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="5793a-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="5793a-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="5793a-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="5793a-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="5793a-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="5793a-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="5793a-255">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5793a-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="5793a-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="5793a-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="5793a-257">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5793a-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="5793a-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="5793a-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="5793a-261">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="5793a-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="5793a-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="5793a-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="5793a-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="5793a-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="5793a-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="5793a-267">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5793a-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="5793a-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="5793a-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="5793a-269">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5793a-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="5793a-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="5793a-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="5793a-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5793a-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="5793a-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="5793a-273">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="5793a-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="5793a-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5793a-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="5793a-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="5793a-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="5793a-277">0x00040000</span><span class="sxs-lookup"><span data-stu-id="5793a-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="5793a-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="5793a-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="5793a-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="5793a-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="5793a-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="5793a-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="5793a-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="5793a-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="5793a-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="5793a-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="5793a-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="5793a-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="5793a-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="5793a-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="5793a-287">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="5793a-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="5793a-289">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5793a-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="5793a-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="5793a-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="5793a-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="5793a-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="5793a-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5793a-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="5793a-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="5793a-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="5793a-295">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5793a-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="5793a-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="5793a-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="5793a-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5793a-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="5793a-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="5793a-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="5793a-301">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="5793a-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="5793a-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5793a-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="5793a-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="5793a-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="5793a-305">0x00010000</span><span class="sxs-lookup"><span data-stu-id="5793a-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="5793a-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="5793a-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="5793a-307">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5793a-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="5793a-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="5793a-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="5793a-309">0x00040000</span><span class="sxs-lookup"><span data-stu-id="5793a-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="5793a-310">Declaração de interfaces</span><span class="sxs-lookup"><span data-stu-id="5793a-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="5793a-311">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="5793a-311">Interface identifiers</span></span>

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

<span data-ttu-id="5793a-312">Use os seguintes identificadores de interface com [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), ou [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir e ignorar qualquer verificação de provedor em objeto de pasta e objeto uma mensagem, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5793a-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="5793a-313">Armazenamento de MAPI</span><span class="sxs-lookup"><span data-stu-id="5793a-313">MAPI store</span></span>

<span data-ttu-id="5793a-314">Esta seção contém definições constantes e identificadores interface usadas por APIs essa interface com o armazenamento de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5793a-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="5793a-315">Constantes</span><span class="sxs-lookup"><span data-stu-id="5793a-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="5793a-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="5793a-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="5793a-317">((ULONG) 0X00010000)</span><span class="sxs-lookup"><span data-stu-id="5793a-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="5793a-318">Um provedor de armazenamento pode especificar**fnevIndexing** no **ulEventType** parte da \*\* [notificação](notification.md) \*\* estrutura para notificar indexador Se um objeto está pronto para indexação.</span><span class="sxs-lookup"><span data-stu-id="5793a-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="5793a-319">A **estrutura** do membro de informações da \*\*estrutura de \*\*NOTIFICAÇÃO contém **[uma estrutura de ](extended_notification.md)** EXTENDED_NOTIFICATION.</span><span class="sxs-lookup"><span data-stu-id="5793a-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="5793a-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="5793a-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="5793a-321">0x00</span><span class="sxs-lookup"><span data-stu-id="5793a-321">0x00</span></span>  <br/> |<span data-ttu-id="5793a-322">Um cliente pode chamar \*\* [IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md) \*\* e verificar se há uma retornada máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="5793a-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="5793a-323">**FS_NONE** indica que a pasta não suporta o compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="5793a-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="5793a-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="5793a-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="5793a-325">0x01</span><span class="sxs-lookup"><span data-stu-id="5793a-325">0x01</span></span>  <br/> |<span data-ttu-id="5793a-326">Um cliente pode chamar \*\* \*\*IFolderSupport::GetSupportMask e verificar se há uma retornada máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="5793a-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="5793a-327">**FS_SUPPORTS_SHARING** indica se a pasta é compatível com compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="5793a-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="5793a-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="5793a-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="5793a-329">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="5793a-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="5793a-330">Identifica o processo que está fazendo com que uma notificação para um indexador um objeto esteja pronta para indexação.</span><span class="sxs-lookup"><span data-stu-id="5793a-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="5793a-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="5793a-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="5793a-332">Conforme definido no arquivo cabeçalho mapidefs.h Kit de desenvolvimento em Microsoft Software Development Kit do Windows (SDK do Windows)\*.</span><span class="sxs-lookup"><span data-stu-id="5793a-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="5793a-333">Um valor para o **campo** uIKIND\*\* [da estrutura](mapinameid.md) \*\* MAPINAMEID.</span><span class="sxs-lookup"><span data-stu-id="5793a-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="5793a-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="5793a-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="5793a-335">Conforme definido no arquivo cabeçalho mapidefs.h do Microsoft Software Development Kit do Windows (SDK do Windows).</span><span class="sxs-lookup"><span data-stu-id="5793a-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="5793a-336">Um valor para o **campo** uIKIND\*\* [da estrutura](mapinameid.md) \*\* MAPINAMEID.</span><span class="sxs-lookup"><span data-stu-id="5793a-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="5793a-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="5793a-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="5793a-338">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="5793a-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="5793a-339">Se um cliente especificar **MSCAP_SEL_RESTRICTION** no *mscapSelector* para \*\* [IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)\*\*, **GetCapabilities** esse valor pode retornar se o repositório ignorar parâmetros inválidos em uma restrição.</span><span class="sxs-lookup"><span data-stu-id="5793a-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="5793a-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="5793a-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="5793a-341">((ULONG) 0X00000020)</span><span class="sxs-lookup"><span data-stu-id="5793a-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="5793a-342">Se um cliente especificar **MSCAP_SEL_RESTRICTION** no *mscapSelector* para \*\* IMSCapabilities::GetCapabilities\*\*, **GetCapabilities** esse valor pode retornar se o repositório for um repositório não padrão que suporta pasta de home pages.</span><span class="sxs-lookup"><span data-stu-id="5793a-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="5793a-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="5793a-344">((ULONG) 0X00800000)</span><span class="sxs-lookup"><span data-stu-id="5793a-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="5793a-345">Um cliente pode chegar à propriedade \*\* [PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) \*\* para determinar as características de um repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5793a-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="5793a-346">Se o provedor de armazenamento definir **STORE_PUSHER_OK** como sinalizador em máscara de bit, significa que o identificador de protocolo MAPI não irá rastrear o armazenamento e o armazenamento é responsável por enviar quaisquer alterações através das notificações para o indexador e enviar mensagens indexadas.</span><span class="sxs-lookup"><span data-stu-id="5793a-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="5793a-347">Definições de namespaces</span><span class="sxs-lookup"><span data-stu-id="5793a-347">Definitions for namespaces</span></span>

<span data-ttu-id="5793a-348">Os seguintes identificadores globais exclusivos (GUIDs) representam os namespaces das propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="5793a-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="5793a-349">Eles são indexados pelo protocolo identificador MAPI (PH) e documentados como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5793a-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="5793a-350">As propriedades nomeadas não devem ser usadas para criar ou modificar itens.</span><span class="sxs-lookup"><span data-stu-id="5793a-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="5793a-351">Propriedades do MNID_ID </span><span class="sxs-lookup"><span data-stu-id="5793a-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="5793a-352">Propriedades do MNID_STRING </span><span class="sxs-lookup"><span data-stu-id="5793a-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="5793a-353">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="5793a-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="5793a-354">Use o `DEFINE_OLEGUID` macro definido no cabeçalho guiddef do SDK do Windows para associar o seguinte nome simbólico GUID ao seu valor.</span><span class="sxs-lookup"><span data-stu-id="5793a-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="5793a-355">Constantes de catálogo de endereços MAPI</span><span class="sxs-lookup"><span data-stu-id="5793a-355">MAPI Address Book constants</span></span>

<span data-ttu-id="5793a-356">Esta seção contém definições constantes para o catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="5793a-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="5793a-357">Constantes</span><span class="sxs-lookup"><span data-stu-id="5793a-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="5793a-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="5793a-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="5793a-359">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="5793a-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="5793a-360">Pasta raiz para um objeto de catálogos de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="5793a-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="5793a-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="5793a-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="5793a-362">((ULONG) 0X00000002)</span><span class="sxs-lookup"><span data-stu-id="5793a-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="5793a-363">Uma subpasta contida na pasta raiz do objeto de catálogos de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="5793a-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="5793a-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="5793a-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="5793a-365">((ULONG) 0X00000003)</span><span class="sxs-lookup"><span data-stu-id="5793a-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="5793a-366">Abrir o contêiner de um objeto do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="5793a-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="5793a-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="5793a-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="5793a-368">((ULONG) 0X00000004)</span><span class="sxs-lookup"><span data-stu-id="5793a-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="5793a-369">Um objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5793a-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="5793a-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5793a-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="5793a-371">((ULONG) 0X00000005)</span><span class="sxs-lookup"><span data-stu-id="5793a-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="5793a-372">0" não é um objeto de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="5793a-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="5793a-373">Constantes de MAPI adicionais</span><span class="sxs-lookup"><span data-stu-id="5793a-373">Additional MAPI constants</span></span>

<span data-ttu-id="5793a-374">Esta seção contém constantes definições, como códigos de erro e identificadores de interface usados pelo APIs MAPI não expostos e documentados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5793a-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="5793a-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="5793a-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="5793a-376">((ULONG) 0X00000001)</span><span class="sxs-lookup"><span data-stu-id="5793a-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="5793a-377">Quando um cliente pede o [método](iaddrbook-details.md)IAddrBook::Details, o cliente deve definir o parâmetro**DIALOG_MODAL** sinalizado na _ulFlags_ para exibir a caixa de diálogo modal, mostrando detalhes sobre uma entrada de catálogo de endereços específico.</span><span class="sxs-lookup"><span data-stu-id="5793a-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="5793a-378">Essa constante é definida em mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="5793a-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="5793a-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="5793a-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="5793a-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="5793a-380">0x00000800</span></span>  <br/> |<span data-ttu-id="5793a-381">No Outlook 2007, repositório Wrapped PST ajustados tem regras e filtragem de spam processadas em novas mensagens antes de serem notificados clientes MAPI de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="5793a-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="5793a-382">Um provedor ou cliente usando o método[IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para criar uma nova mensagem em repositórios de PST deve-se configurar a sinalização**ITEMPROC_FORCE** no parâmetro _ulFlags_ do método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para indicar para a loja PST que a mensagem está disponível para as regras de processamento antes que a loja notifique qualquer cliente sobre a chegada de uma mensagem nova.</span><span class="sxs-lookup"><span data-stu-id="5793a-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="5793a-383">Observe que essas regras de processamento só se aplicam às novas mensagens criadas em um servidor Microsoft Exchange Server, porque o servidor Exchange processa as regras para mensagens no servidor.</span><span class="sxs-lookup"><span data-stu-id="5793a-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="5793a-384">Longo o provedor ou cliente que criar a mensagem deve passar esse sinalizador em combinação com **NON_EMS_XP_SAVE**, que indica que o servidor não é um servidor do Exchange.</span><span class="sxs-lookup"><span data-stu-id="5793a-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="5793a-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="5793a-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="5793a-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="5793a-386">0x00200000</span></span>  <br/> |<span data-ttu-id="5793a-387">Um cliente pode acionar a função[MAPILogonEx](mapilogonex.md) e configurar o **MAPI_BG_SESSION** sinalizado no parâmetro_flFlags_ para fazer logon em uma sessão e executar as operações na tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="5793a-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="5793a-388">Em geral, se um cliente pretende fazer o processamento em uma conversa de tela de fundo ou em um processo separado em uma forma que seja a conversa do primeiro plano seja discreta, ele deve acionar [MAPILogonEx](mapilogonex.md) com o sinalizador**MAPI_BG_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="5793a-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="5793a-389">Um exemplo em que isso é usado é um aplicativo do cliente, assim como um mecanismo de indexação, abrindo um arquivo de pastas particulares (PST) para o acesso de tipo plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="5793a-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="5793a-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5793a-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="5793a-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="5793a-391">0x00004000</span></span>  <br/> |<span data-ttu-id="5793a-392">Um cliente pode ligar para o método [IAddrBook::OpenEntry](iaddrbook-openentry.md) Configurando o **MAPI_CACHE_ONLY** sinalizado no parâmetro _ulFlags_ para abrir uma entrada do catálogo de endereços e acessá-los posteriormente apenas a partir do cache.</span><span class="sxs-lookup"><span data-stu-id="5793a-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="5793a-393">Um exemplo em que isso é usado é um aplicativo do cliente, que deseja abrir a lista de endereços Global no modo cache do Exchange, acessar uma entrada de catálogo de endereços do cache sem criar tráfego entre o cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="5793a-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="5793a-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="5793a-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="5793a-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="5793a-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="5793a-396">Esse valor pode ser passado para a função MAPISendMail MAPI simples no parâmetro _ulFlags_ para especificar que uma caixa de diálogo sem janela restrita é exibida no aplicativo de email padrão.</span><span class="sxs-lookup"><span data-stu-id="5793a-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="5793a-397">Se nem esse sinalizador nem o MAPI_DIALOG (0x00000008) estiverem definidos, a caixa de diálogo não é exibida.</span><span class="sxs-lookup"><span data-stu-id="5793a-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="5793a-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="5793a-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="5793a-399">0x00000200</span><span class="sxs-lookup"><span data-stu-id="5793a-399">0x00000200</span></span>  <br/> |<span data-ttu-id="5793a-400">Se o Microsoft Office Outlook estiver no modo cache do Exchange e um repositório estiver aberto no modo de cache, um cliente ou provedores de serviços podem acionar [IMsgStore::OpenEntry](imsgstore-openentry.md), configurando o sinalizador**MAPI_NO_CACHE** no parâmetro _ulFlags_ para abrir um item ou uma pasta no repositório de dados remoto.</span><span class="sxs-lookup"><span data-stu-id="5793a-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="5793a-401">Observe que, se você abrir o armazenamento de mensagens com o sinalizador **MDB_ONLINE** no servidor remoto não será necessário usar o sinalizador**MAPI_NO_CACHE**.</span><span class="sxs-lookup"><span data-stu-id="5793a-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="5793a-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5793a-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="5793a-403">0x80000000</span><span class="sxs-lookup"><span data-stu-id="5793a-403">0x80000000</span></span>  <br/> |<span data-ttu-id="5793a-404">Um cliente ou provedores de serviços podem acionar a função [OpenIMsgOnIStg](openimsgonistg.md) definindo a sinalização **MAPI_UNICODE** no parâmetro_ulFlags_ para criar arquivos Unicode. msg.</span><span class="sxs-lookup"><span data-stu-id="5793a-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="5793a-405">O arquivo resultante [IMessage: IMAPIProp](imessageimapiprop.md) mostra **STORE_UNICODE_OK** na sua [propriedade Canonical PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) e é compatível com propriedades Unicode.</span><span class="sxs-lookup"><span data-stu-id="5793a-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="5793a-406">Essa constante é definida em mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="5793a-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="5793a-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5793a-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="5793a-408">0x00000100</span><span class="sxs-lookup"><span data-stu-id="5793a-408">0x00000100</span></span>  <br/> |<span data-ttu-id="5793a-409">Se o Outlook estiver no modo cache do Exchange, um cliente ou serviço pode acionar o método[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) configurando o **MDB_ONLINE** sinalizado no parâmetro_ulFlags_ para substituir a conexão do armazenamento de mensagem local e abrir o repositório no servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="5793a-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="5793a-410">Observe que você não pode abrir um repositório do Exchange no modo de cache e no modo em não-cache ao mesmo tempo na mesma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="5793a-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="5793a-411">Se você já tiver aberto o arquivo de cache mensagens, você deve fechar o repositório antes de abri-lo com esse sinalizador ou abrir uma nova sessão MAPI onde você pode abrir o armazenamento do Exchange no servidor remoto usando esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="5793a-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="5793a-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="5793a-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="5793a-413">0x00001000</span><span class="sxs-lookup"><span data-stu-id="5793a-413">0x00001000</span></span>  <br/> |<span data-ttu-id="5793a-414">Um cliente pode acionar o [IMAPIProp::SaveChanges](imapiprop-savechanges.md)  Configurando o **NON_EMS_XP_SAVE** sinalizado no parâmetro_ulFlags_ para indicar que a mensagem não foi enviada do Exchange server.</span><span class="sxs-lookup"><span data-stu-id="5793a-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="5793a-415">Esse sinalizador deve ser usado em combinação com o **ITEMPROC_FORCE** sinalizado no parâmetro _ulFlags_ para indicar em um repsitório de PST que a mensagem está qualificada para processar antes do repositório de PST notificar qualquer cliente sobre a chegada de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5793a-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="5793a-416">Essas regras de processamento só se aplicam às novas mensagens que são criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não é um servidor do Exchange (nesse caso o servidor Exchange já teria regras processadas na mensagem).</span><span class="sxs-lookup"><span data-stu-id="5793a-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="5793a-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="5793a-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="5793a-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="5793a-418">0x00000080</span></span>  <br/> |<span data-ttu-id="5793a-419">Um cliente pode acionar [IMAPIProp::SaveChanges](imapiprop-savechanges.md), para configurar o **SPAMFILTER_ONSAVE** sinalizado no parâmetro _ulFlags_ para habilitar o filtro de spam em uma mensagem que está sendo salva.</span><span class="sxs-lookup"><span data-stu-id="5793a-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="5793a-420">O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).</span><span class="sxs-lookup"><span data-stu-id="5793a-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="5793a-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="5793a-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="5793a-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="5793a-422">0x00200000</span></span>  <br/> |<span data-ttu-id="5793a-423">Se esse sinalizador estiver definido na [propriedade Canonical PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) de um repositório de PST isso indica que, quando chegar uma nova mensagem no repositório, repositório tem regras e filtragem de spam processadas na mensagem separadamente.</span><span class="sxs-lookup"><span data-stu-id="5793a-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="5793a-424">O repositório chama a configuração [IMAPISupport::Notify](imapisupport-notify.md)em**fnevNewMail** na [notificação](notification.md)estrutura que é autenticada como um  parâmetro e passando os detalhes do novo mensagem para o cliente de escuta.</span><span class="sxs-lookup"><span data-stu-id="5793a-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="5793a-425">Posteriormente, quando o cliente de escutará recebe a notificação, ele não processará regras na mensagem.</span><span class="sxs-lookup"><span data-stu-id="5793a-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="5793a-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="5793a-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="5793a-427">0x00040000</span><span class="sxs-lookup"><span data-stu-id="5793a-427">0x00040000</span></span>  <br/> |<span data-ttu-id="5793a-428">Se esse sinalizador estiver incluído na [propriedade Canonical PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md), isso indica o repositório compatível com o armazenamento Unicode.</span><span class="sxs-lookup"><span data-stu-id="5793a-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="5793a-429">Um cliente pode pesquisar a presença de sinalizador para decidir se vai solicitar ou salvar informações do Unicode no repositório.</span><span class="sxs-lookup"><span data-stu-id="5793a-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="5793a-430">Definições para arquivar itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="5793a-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="5793a-431">As seguintes definições constantes são valores usados para configurar a [propriedade Canonical PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="5793a-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="5793a-432">Definições para exibir objetos remotos</span><span class="sxs-lookup"><span data-stu-id="5793a-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="5793a-433">As seguintes definições de constante e macro são para exibir objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="5793a-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="5793a-434">Para saber mais, confira a [propriedade Canonical PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="5793a-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="5793a-435">As definições de catálogo de endereços do Exchange e mensagem armazenam códigos de erro</span><span class="sxs-lookup"><span data-stu-id="5793a-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="5793a-436">Estas são as definições de código de erro para o catálogo de endereços do Exchange e o Message Store, que possui o recurso reconexão.</span><span class="sxs-lookup"><span data-stu-id="5793a-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="5793a-437">Última chamada para um catálogo global desconectado pode resultar no erro **MAPI_E_END_OF_SESSION** e precisará ser repetida.</span><span class="sxs-lookup"><span data-stu-id="5793a-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="5793a-438">O MAPI do Outlook aceita reconexão em um servidor GC sem uma reconfiguração especial, mas alguns códigos de erro podem ser retornados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="5793a-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="5793a-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="5793a-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="5793a-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="5793a-440">0x80040200</span></span>  <br/> |<span data-ttu-id="5793a-441">Retornado quando uma conexão tiver sido desconectada.</span><span class="sxs-lookup"><span data-stu-id="5793a-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="5793a-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="5793a-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="5793a-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="5793a-443">0x80040125</span></span>  <br/> |<span data-ttu-id="5793a-444">Retornado quando o token de conexão do procedimento remoto (RPC) estiver desatualizado.</span><span class="sxs-lookup"><span data-stu-id="5793a-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="5793a-445">Se o token da transação é diferente do token de conexão que significa que se reconectou, isso é retornado**MAPI_E_RECONNECTED** e pode ser tratado na mesma **MAPI_E_END_OF_SESSION**.</span><span class="sxs-lookup"><span data-stu-id="5793a-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="5793a-446">A chamada deve ser repetida.</span><span class="sxs-lookup"><span data-stu-id="5793a-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="5793a-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5793a-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="5793a-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="5793a-448">0x80040126</span></span>  <br/> |<span data-ttu-id="5793a-449">Retornado quando a conexão está offline.</span><span class="sxs-lookup"><span data-stu-id="5793a-449">Returned when the connection is offline.</span></span> <span data-ttu-id="5793a-450">Normalmente, isso significa que algo ocorreu no ambiente, como falha no servidor ou perda de conectividade de rede.</span><span class="sxs-lookup"><span data-stu-id="5793a-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="5793a-451">Esse erro é mais provável que ocorra ao usar um modo cache do perfil tentando ignorar o cache de se comunicar com o servidor.</span><span class="sxs-lookup"><span data-stu-id="5793a-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="5793a-452">Se o cache não conseguir estabelecer uma conexão com o servidor, o estado offline**MAPI_E_OFFLINE** pode surgir.</span><span class="sxs-lookup"><span data-stu-id="5793a-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="5793a-453">Nenhuma dos dois erros anteriores será retornado em todos os cenários onde eles poderiam ser usados.</span><span class="sxs-lookup"><span data-stu-id="5793a-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="5793a-454">Na maioria dos casos **MAPI\_E_NETWORK_ERROR** ou **MAPI_E_CALL_FAILED** será retornado.</span><span class="sxs-lookup"><span data-stu-id="5793a-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="5793a-455">Nem irá aparecer usando o download do [MAPI do cliente Microsoft Exchange Server e Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440).</span><span class="sxs-lookup"><span data-stu-id="5793a-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="5793a-456">Definições para cotas de modo em cache para o Exchange Server Mailbox.</span><span class="sxs-lookup"><span data-stu-id="5793a-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="5793a-457">As seguintes definições constantes são usadas pelo Microsoft Outlook 2010 e Microsoft Outlook 2013 para configurar as cotas de perfil do Exchange de modo que são equivalentes às cotas da caixa de correio Exchange em outros casos disponíveis somente com um perfil online.</span><span class="sxs-lookup"><span data-stu-id="5793a-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="5793a-458">Essas propriedades mapeiam suas propriedades online correspondentes e contêm os mesmos valores em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="5793a-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="5793a-459">Mapear PR_QUOTA_WARNING para PR_STORAGE_QUOTA_LIMIT PR_QUOTA_SEND para PR_QUOTA_PROHIBIT_SEND_QUOTA e PR_QUOTA_RECEIVE para PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="5793a-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="5793a-460">Definições para formato da mensagem</span><span class="sxs-lookup"><span data-stu-id="5793a-460">Definitions for message format</span></span>

<span data-ttu-id="5793a-461">As seguintes definições constantes são valores usados para configurar a [propriedade Canonical PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="5793a-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="5793a-462">Definições para usar RPC sobre HTTP\*</span><span class="sxs-lookup"><span data-stu-id="5793a-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="5793a-463">Confira as [propriedades Canonical das definições de tópico constante PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) usadas como sinalizadores para definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5793a-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="5793a-464">Confira as [propriedades Canonical das definições de tópico constante PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) usadas para definir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="5793a-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="5793a-465">Identificadores</span><span class="sxs-lookup"><span data-stu-id="5793a-465">Identifiers</span></span>

<span data-ttu-id="5793a-466">Use a `DEFINE_OLEGUID` macro estipulada no arquivo cabeçalho guiddef.h do Microsoft Software Development Kit do Windows (SDK do Windows) para associar os seguintes nomes simbólicos GUID e seus valores.</span><span class="sxs-lookup"><span data-stu-id="5793a-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="5793a-467">O seguinte identificador é para o perfil Capone de um catálogo de endereços, que em suporte com multiplas caixas de correio Exchange ([MultiEx](using-multiple-exchange-accounts.md)) contendo a propriedade[PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) que efetivamente desativa o contêiner padrão especificado pelo [SetDefaultDir](iaddrbook-setdefaultdir.md).</span><span class="sxs-lookup"><span data-stu-id="5793a-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="5793a-468">Identificadores de interface</span><span class="sxs-lookup"><span data-stu-id="5793a-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="5793a-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="5793a-469">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="5793a-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="5793a-470">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="5793a-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="5793a-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="5793a-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="5793a-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="5793a-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="5793a-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="5793a-474">Identificadores de interface de substituição do PST</span><span class="sxs-lookup"><span data-stu-id="5793a-474">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="5793a-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="5793a-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="5793a-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="5793a-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="5793a-477">Confira também</span><span class="sxs-lookup"><span data-stu-id="5793a-477">See also</span></span>

- [<span data-ttu-id="5793a-478">Sobre as adições de MAPI</span><span class="sxs-lookup"><span data-stu-id="5793a-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="5793a-479">Sobre as propriedades nomeadas usadas pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="5793a-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="5793a-480">Acessar o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="5793a-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="5793a-481">Abrir o Store em um servidor remoto quando o Outlook estiver no modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="5793a-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="5793a-482">Gerenciar mensagens em um OST sem solicitar uma sincronização do modo cache do Exchange</span><span class="sxs-lookup"><span data-stu-id="5793a-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

