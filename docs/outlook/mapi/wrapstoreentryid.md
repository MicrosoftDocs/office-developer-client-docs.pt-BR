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
ms.openlocfilehash: aff46cca7a7d530b2eede1790176058e3b91abc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770721"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="4ace7-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="4ace7-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="4ace7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ace7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ace7-105">Converte o identificador de entrada interna do repositório de uma mensagem para um identificador de entrada mais utilizável pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4ace7-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ace7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4ace7-106">Header file:</span></span>  <br/> |<span data-ttu-id="4ace7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ace7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4ace7-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4ace7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ace7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4ace7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4ace7-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4ace7-110">Called by:</span></span>  <br/> |<span data-ttu-id="4ace7-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="4ace7-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4ace7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ace7-112">Parameters</span></span>

 <span data-ttu-id="4ace7-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ace7-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4ace7-114">[in] Bitmask dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="4ace7-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="4ace7-115">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="4ace7-115">The following flag can be set:</span></span>
    
<span data-ttu-id="4ace7-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4ace7-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4ace7-117">As cadeias de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4ace7-117">The strings are in Unicode format.</span></span> <span data-ttu-id="4ace7-118">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="4ace7-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="4ace7-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="4ace7-119">_szDLLName_</span></span>
  
> <span data-ttu-id="4ace7-120">[in] O nome do provedor de armazenamento de mensagem DLL.</span><span class="sxs-lookup"><span data-stu-id="4ace7-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="4ace7-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="4ace7-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="4ace7-122">[in] Tamanho, em bytes, do identificador de entrada original para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4ace7-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="4ace7-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="4ace7-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="4ace7-124">[in] Ponteiro para uma estrutura [ENTRYID](entryid.md) que contém o identificador de entrada original.</span><span class="sxs-lookup"><span data-stu-id="4ace7-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="4ace7-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="4ace7-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="4ace7-126">[out] Ponteiro para o tamanho, em bytes, de um novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ace7-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="4ace7-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="4ace7-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="4ace7-128">[out] Ponteiro para um ponteiro para uma estrutura **ENTRYID** que contém o novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="4ace7-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4ace7-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4ace7-129">Return value</span></span>

<span data-ttu-id="4ace7-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4ace7-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ace7-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ace7-131">Remarks</span></span>

<span data-ttu-id="4ace7-132">Um objeto de repositório de mensagem mantém um identificador interno de entrada que é significativo apenas para coresident de provedores de serviço com esse armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4ace7-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="4ace7-133">Para outros componentes de mensagens, MAPI fornece uma versão com quebra do identificador interno de entrada que torna reconhecível conforme que pertencem ao repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4ace7-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="4ace7-134">Provedores de serviços de coresident devem sempre ser dada o identificador de entrada de repositório desfeita da mensagem original; aplicativos cliente devem sempre ser dada a versão com quebra, que é, em seguida, pode ser usada em qualquer lugar no domínio de mensagens e em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="4ace7-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="4ace7-135">Um provedor de serviços pode quebrar um identificador de entrada do repositório de mensagem usando a função **WrapStoreEntryID** ou o método [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , que chama a função **WrapStoreEntryID** .</span><span class="sxs-lookup"><span data-stu-id="4ace7-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="4ace7-136">O provedor deve quebrar o identificador de entrada ao expor **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do armazenamento de mensagens propriedade ou gravá-lo em uma seção de perfil e ao expor **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) propriedade.</span><span class="sxs-lookup"><span data-stu-id="4ace7-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="4ace7-137">Um identificador de entrada do repositório de mensagem é disposto MAPI ao responder a uma chamada [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="4ace7-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="4ace7-138">Quando um aplicativo cliente passa um identificador de entrada do repositório de mensagem com quebra para MAPI, por exemplo em uma chamada de [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI ou não, o identificador de entrada para utilizá-lo para chamar um método de provedor, como [IMSProvider::Logon](imsprovider-logon.md) ou [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="4ace7-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

