---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767484"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="bc1e3-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="bc1e3-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="bc1e3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc1e3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc1e3-105">Designa um serviço de mensagem a ser o fornecedor da identidade principal para o perfil.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="bc1e3-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="bc1e3-106">Parameters</span></span>

 <span data-ttu-id="bc1e3-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="bc1e3-107">_lpUID_</span></span>
  
> <span data-ttu-id="bc1e3-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem para fornecer a identidade principal, ou nulo, o que indica que o **SetPrimaryIdentity** deve desmarcar a identidade atual.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="bc1e3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc1e3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bc1e3-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc1e3-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bc1e3-111">Return value</span></span>

<span data-ttu-id="bc1e3-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc1e3-112">S_OK</span></span> 
  
> <span data-ttu-id="bc1e3-113">O serviço de mensagem foi atribuído com êxito o fornecedor da identidade principal.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="bc1e3-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="bc1e3-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="bc1e3-115">**SetPrimaryIdentity** tentou designar um serviço de mensagem que tem o sinalizador SERVICE_NO_PRIMARY_IDENTITY definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bc1e3-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc1e3-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="bc1e3-116">Remarks</span></span>

<span data-ttu-id="bc1e3-117">O método **IMsgServiceAdmin::SetPrimaryIdentity** estabelece um serviço de mensagem como o fornecedor da identidade principal para o perfil.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="bc1e3-118">A identidade principal é normalmente o usuário que está conectado ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="bc1e3-119">Ela é representada por três propriedades:</span><span class="sxs-lookup"><span data-stu-id="bc1e3-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="bc1e3-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc1e3-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="bc1e3-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc1e3-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="bc1e3-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc1e3-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="bc1e3-123">Cada provedor de serviço no serviço de mensagem designada define essas três propriedades como o nome para exibição, o identificador de entrada e a chave de pesquisa do usuário mensagens que fornece a identidade principal.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="bc1e3-124">Os clientes podem recuperar o identificador de entrada a identidade principal chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="bc1e3-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="bc1e3-125">A propriedade **PR_RESOURCE_FLAGS** é definida para STATUS_PRIMARY_IDENTITY para cada provedor que seja membro do serviço de mensagem que fornece a identidade principal e SERVICE_PRIMARY_IDENTITY para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="bc1e3-126">Quando um provedor de serviços, será possível fornecer a identidade do principal para o seu serviço de mensagem, ela define **PR_RESOURCE_FLAGS** para STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="bc1e3-127">**SetPrimaryIdentity** define a propriedade **PR_RESOURCE_FLAGS** de cada serviço de mensagem que não está fornecendo a identidade principal a SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="bc1e3-128">Cada provedor de serviços de mensagem MAPI tem informações sobre pode estabelecer uma identidade de cada um dos seus usuários quando um cliente fizer logon no serviço.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="bc1e3-129">No entanto, como MAPI oferece suporte a conexões com vários provedores de serviço para cada sessão MAPI, há uma estável definição da identidade de um usuário específico para a sessão MAPI como um todo; a identidade do usuário depende de qual serviço está envolvido.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="bc1e3-130">Os clientes podem chamar **SetPrimaryIdentity** para designar uma das muitas identidades estabelecidas para um usuário pelos serviços de mensagem como a identidade do principal para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="bc1e3-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc1e3-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc1e3-131">See also</span></span>



[<span data-ttu-id="bc1e3-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="bc1e3-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="bc1e3-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="bc1e3-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="bc1e3-134">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc1e3-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

