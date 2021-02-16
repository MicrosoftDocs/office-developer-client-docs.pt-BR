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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430361"
---
# <a name="imsgserviceadminsetprimaryidentity"></a><span data-ttu-id="e1a2f-103">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a2f-103">IMsgServiceAdmin::SetPrimaryIdentity</span></span>

  
  
<span data-ttu-id="e1a2f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1a2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1a2f-105">Designa um serviço de mensagens para ser o fornecedor da identidade principal do perfil.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-105">Designates a message service to be the supplier of the primary identity for the profile.</span></span>
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a><span data-ttu-id="e1a2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1a2f-106">Parameters</span></span>

 <span data-ttu-id="e1a2f-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="e1a2f-107">_lpUID_</span></span>
  
> <span data-ttu-id="e1a2f-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens para fornecer a identidade principal, ou NULL, que indica que **SetPrimaryIdentity** deve limpar a identidade atual.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to supply the primary identity, or NULL, which indicates that **SetPrimaryIdentity** should clear the current identity.</span></span> 
    
 <span data-ttu-id="e1a2f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1a2f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e1a2f-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-110">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1a2f-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e1a2f-111">Return value</span></span>

<span data-ttu-id="e1a2f-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1a2f-112">S_OK</span></span> 
  
> <span data-ttu-id="e1a2f-113">O serviço de mensagens foi atribuído com êxito ao fornecedor da identidade principal.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-113">The message service was successfully assigned the supplier of the primary identity.</span></span>
    
<span data-ttu-id="e1a2f-114">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="e1a2f-114">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e1a2f-115">**SetPrimaryIdentity** tentou designar um serviço de mensagem que tem o sinalizador SERVICE_NO_PRIMARY_IDENTITY definido em sua **propriedade PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1a2f-115">**SetPrimaryIdentity** attempted to designate a message service that has the SERVICE_NO_PRIMARY_IDENTITY flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1a2f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1a2f-116">Remarks</span></span>

<span data-ttu-id="e1a2f-117">O **método IMsgServiceAdmin::SetPrimaryIdentity** estabelece um serviço de mensagens como fornecedor da identidade principal do perfil.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-117">The **IMsgServiceAdmin::SetPrimaryIdentity** method establishes a message service as the supplier of the primary identity for the profile.</span></span> <span data-ttu-id="e1a2f-118">Normalmente, a identidade principal é o usuário que está conectado ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-118">The primary identity is typically the user who is logged on to the message service.</span></span> <span data-ttu-id="e1a2f-119">Ele é representado por três propriedades:</span><span class="sxs-lookup"><span data-stu-id="e1a2f-119">It is represented by three properties:</span></span> 
  
- <span data-ttu-id="e1a2f-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1a2f-120">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))</span></span>
    
- <span data-ttu-id="e1a2f-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1a2f-121">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="e1a2f-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e1a2f-122">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))</span></span>
    
<span data-ttu-id="e1a2f-123">Cada provedor de serviços no serviço de mensagens designado define essas três propriedades como o nome de exibição, o identificador de entrada e a chave de pesquisa do usuário de mensagens que fornece a identidade principal.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-123">Every service provider in the designated message service sets these three properties to the display name, entry identifier, and search key of the messaging user that supplies the primary identity.</span></span> <span data-ttu-id="e1a2f-124">Os clientes podem recuperar o identificador de entrada da identidade principal chamando o [método IMAPISession::QueryIdentity.](imapisession-queryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="e1a2f-124">Clients can retrieve the primary identity's entry identifier by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method.</span></span> 
  
<span data-ttu-id="e1a2f-125">A **PR_RESOURCE_FLAGS** propriedade é definida como STATUS_PRIMARY_IDENTITY para todos os provedores que são membros do serviço de mensagens que fornece a identidade principal e SERVICE_PRIMARY_IDENTITY para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-125">The **PR_RESOURCE_FLAGS** property is set to STATUS_PRIMARY_IDENTITY for every provider that is a member of the message service that supplies the primary identity, and to SERVICE_PRIMARY_IDENTITY for the message service.</span></span> <span data-ttu-id="e1a2f-126">Quando um provedor de serviços não pode fornecer a identidade principal para seu serviço de mensagens, ele **define** PR_RESOURCE_FLAGS como STATUS_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-126">When a service provider cannot supply the primary identity for its message service, it sets **PR_RESOURCE_FLAGS** to STATUS_NO_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="e1a2f-127">**SetPrimaryIdentity** define  PR_RESOURCE_FLAGS propriedade de cada serviço de mensagens que não está fornecendo a identidade principal para SERVICE_NO_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-127">**SetPrimaryIdentity** sets the **PR_RESOURCE_FLAGS** property of each message service that is not supplying the primary identity to SERVICE_NO_PRIMARY_IDENTITY.</span></span> 
  
<span data-ttu-id="e1a2f-128">Cada provedor de serviços de mensagens sobre o quais o MAPI tem informações pode estabelecer uma identidade para cada um de seus usuários quando um cliente faz o login no serviço.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-128">Each message service provider that MAPI has information about can establish an identity for each of its users when a client logs on to the service.</span></span> <span data-ttu-id="e1a2f-129">No entanto, como o MAPI dá suporte a conexões com vários provedores de serviços para cada sessão MAPI, não há uma definição forte da identidade de um usuário específico para a sessão MAPI como um todo; a identidade de um usuário depende de qual serviço está envolvido.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-129">However, because MAPI supports connections to multiple service providers for each MAPI session, there is no firm definition of a particular user's identity for the MAPI session as a whole; a user's identity depends on which service is involved.</span></span> <span data-ttu-id="e1a2f-130">Os clientes podem **chamar SetPrimaryIdentity** para designar uma das muitas identidades estabelecidas para um usuário pelos serviços de mensagem como a identidade principal desse usuário.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-130">Clients can call **SetPrimaryIdentity** to designate one of the many identities established for a user by message services as the primary identity for that user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1a2f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1a2f-131">See also</span></span>



[<span data-ttu-id="e1a2f-132">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="e1a2f-132">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
  
[<span data-ttu-id="e1a2f-133">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e1a2f-133">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e1a2f-134">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1a2f-134">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

