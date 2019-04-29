---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409206"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="ab00d-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="ab00d-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="ab00d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab00d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab00d-105">Converte um identificador de entrada interna do repositório de mensagens em um identificador de entrada mais utilizável pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ab00d-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab00d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ab00d-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab00d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ab00d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ab00d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ab00d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab00d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab00d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab00d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ab00d-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab00d-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="ab00d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="ab00d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab00d-112">Parameters</span></span>

 <span data-ttu-id="ab00d-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab00d-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ab00d-114">no Bitmask de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="ab00d-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="ab00d-115">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="ab00d-115">The following flag can be set:</span></span>
    
<span data-ttu-id="ab00d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ab00d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ab00d-117">As cadeias de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ab00d-117">The strings are in Unicode format.</span></span> <span data-ttu-id="ab00d-118">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ab00d-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ab00d-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="ab00d-119">_szDLLName_</span></span>
  
> <span data-ttu-id="ab00d-120">no O nome da DLL do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ab00d-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="ab00d-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="ab00d-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="ab00d-122">no Tamanho, em bytes, do identificador de entrada original para o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ab00d-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="ab00d-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="ab00d-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="ab00d-124">no Ponteiro para uma [](entryid.md) estrutura ENTRYID que contém o identificador de entrada original.</span><span class="sxs-lookup"><span data-stu-id="ab00d-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="ab00d-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="ab00d-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="ab00d-126">bota Ponteiro para o tamanho, em bytes, do novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ab00d-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="ab00d-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="ab00d-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="ab00d-128">bota Ponteiro para um ponteiro para uma \*\*\*\* estrutura ENTRYID que contém o novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ab00d-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab00d-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ab00d-129">Return value</span></span>

<span data-ttu-id="ab00d-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ab00d-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab00d-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab00d-131">Remarks</span></span>

<span data-ttu-id="ab00d-132">Um objeto do repositório de mensagens mantém um identificador de entrada interno que é significativo apenas para os provedores de serviços coresidentes com o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ab00d-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="ab00d-133">Para outros componentes de mensagens, o MAPI fornece uma versão encapsulada do identificador de entrada interna que o torna reconhecível como pertencente ao repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ab00d-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="ab00d-134">Os provedores de serviço de coresidente devem sempre receber o identificador de entrada de repositório de mensagens não wrapped original; os aplicativos cliente devem sempre ter a versão empacotada, que pode ser usada em qualquer lugar no domínio de mensagens e em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="ab00d-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="ab00d-135">Um provedor de serviços pode encapsular um identificador de entrada de repositório de mensagens usando a função **WrapStoreEntryID** ou o método [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , que chama a função **WrapStoreEntryID** .</span><span class="sxs-lookup"><span data-stu-id="ab00d-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="ab00d-136">O provedor deve encapsular o identificador de entrada ao expor a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do repositório de mensagens ou gravá-lo em uma seção de perfil e ao expor o **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) Propriedades.</span><span class="sxs-lookup"><span data-stu-id="ab00d-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="ab00d-137">O MAPI divide um identificador de entrada de repositório de mensagens ao responder a uma chamada a [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="ab00d-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="ab00d-138">Quando um aplicativo cliente passa um identificador de entrada de repositório de mensagens quebrado para MAPI, por exemplo, em uma chamada a [IMAPISession:: OpenEntry](imapisession-openentry.md) , o MAPI desenvolve o identificador de entrada antes de usá-lo para chamar um método de provedor como [IMSProvider:: logon](imsprovider-logon.md) ou [ IMSProvider:: CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="ab00d-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

