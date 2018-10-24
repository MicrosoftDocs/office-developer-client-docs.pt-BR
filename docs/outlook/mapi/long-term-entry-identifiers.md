---
title: Identificadores de entradas de longo prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e624ab4f39ef5a5385119779b0780ee7173a3ee7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586918"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="fe4d8-103">Identificadores de entradas de longo prazo</span><span class="sxs-lookup"><span data-stu-id="fe4d8-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="fe4d8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe4d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe4d8-105">Um identificador de entrada de longo prazo é atribuído por um provedor de serviço a um objeto quando um objeto exige um identificador com um tempo de vida prolongado.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="fe4d8-106">Identificadores de entrada de longo prazo sempre são válidos por semanas ou meses e podem ser válidos em outras estações de trabalho, dependendo do provedor.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="fe4d8-107">Os identificadores de longo prazo criados por provedores de catálogo de endereço para destinatários personalizados são válidos universal.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="fe4d8-108">Identificadores de entrada de longo prazo são atribuídos a armazenamentos de mensagens, pastas, mensagens, contêineres do catálogo de endereços, mensagens usuários e distribuição de listas.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="fe4d8-109">Quando os aplicativos cliente chamam o método [IMAPIProp::GetProps](imapiprop-getprops.md) desses objetos, sempre é um identificador de entrada de longo prazo que é retornado.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="fe4d8-110">Identificadores de entrada de longo prazo devem ser exclusivos entre todos os repositórios de mensagem no perfil ativo; Portanto, quando uma mensagem ou a pasta é copiada do repositório de uma mensagem para outro, ele deve ser atribuído um novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="fe4d8-111">Quando um objeto de repositório de mensagem é movido, o provedor de armazenamento de mensagem que implementa a movimentação determina se o identificador de entrada original permanecerá válido.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="fe4d8-112">Alguns provedores de serviços atribuem novos identificadores de entrada aos objetos movidos; outros não.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="fe4d8-113">Se houver uma alteração, o novo identificador de entrada será incluído nas informações do passado para clientes quando eles são notificados sobre a movimentação.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="fe4d8-114">Normalmente, provedores de armazenamento de mensagem implementam o seguinte comportamento quando movem pastas:</span><span class="sxs-lookup"><span data-stu-id="fe4d8-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="fe4d8-115">Quando uma pasta é movida do repositório de uma mensagem para outro repositório de um tipo diferente, o identificador de entrada é garantido para alterar.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="fe4d8-116">Quando uma pasta é movida do repositório de uma mensagem para outro repositório do mesmo tipo, o identificador de entrada quase sempre é alterado.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="fe4d8-117">Quando uma pasta é movida para outro local dentro do mesmo repositório de mensagem, o identificador de entrada pode ou não pode mudar, dependendo do provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="fe4d8-118">Renomear uma pasta sem alterar sua pasta pai geralmente não faz com que o identificador de entrada alterar.</span><span class="sxs-lookup"><span data-stu-id="fe4d8-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe4d8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe4d8-119">See also</span></span>



[<span data-ttu-id="fe4d8-120">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="fe4d8-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

