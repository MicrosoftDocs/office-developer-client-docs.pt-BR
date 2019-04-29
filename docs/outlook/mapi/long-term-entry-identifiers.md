---
title: Identificadores de entrada de longo prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409220"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="5ebce-103">Identificadores de entrada de longo prazo</span><span class="sxs-lookup"><span data-stu-id="5ebce-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="5ebce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ebce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ebce-105">Um identificador de entrada de longo prazo é atribuído por um provedor de serviços a um objeto quando um objeto requer um identificador com uma vida útil prolongada.</span><span class="sxs-lookup"><span data-stu-id="5ebce-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="5ebce-106">Os identificadores de entrada de longo prazo são sempre válidos para semanas ou meses e podem ser válidos em outras estações de trabalho, dependendo do provedor.</span><span class="sxs-lookup"><span data-stu-id="5ebce-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="5ebce-107">Os identificadores de longo prazo criados por provedores de catálogo de endereços para destinatários personalizados são válidos universalmente.</span><span class="sxs-lookup"><span data-stu-id="5ebce-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="5ebce-108">Os identificadores de entrada de longo prazo são atribuídos a repositórios de mensagens, pastas, mensagens, contêineres de catálogos de endereços, usuários de mensagens e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="5ebce-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="5ebce-109">Quando os aplicativos cliente chamam o método [IMAPIProp::](imapiprop-getprops.md) GetProps desses objetos, é sempre um identificador de entrada de longo prazo que é retornado.</span><span class="sxs-lookup"><span data-stu-id="5ebce-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="5ebce-110">Os identificadores de entrada de longo prazo devem ser exclusivos em todos os repositórios de mensagens no perfil ativo; Portanto, quando uma mensagem ou pasta é copiada de um repositório de mensagens para outro, ela deve ser atribuída a um novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="5ebce-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="5ebce-111">Quando um objeto do repositório de mensagens é movido, o provedor de armazenamento de mensagens que implementa a movimentação determina se o identificador de entrada original permanecerá válido.</span><span class="sxs-lookup"><span data-stu-id="5ebce-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="5ebce-112">Alguns provedores de serviços atribuem novos identificadores de entrada a objetos movidos; outros não.</span><span class="sxs-lookup"><span data-stu-id="5ebce-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="5ebce-113">Se houver uma alteração, o novo identificador de entrada será incluído nas informações passadas aos clientes quando eles forem notificados sobre a movimentação.</span><span class="sxs-lookup"><span data-stu-id="5ebce-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="5ebce-114">Normalmente, os provedores de repositórios de mensagens implementam o seguinte comportamento quando movem pastas:</span><span class="sxs-lookup"><span data-stu-id="5ebce-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="5ebce-115">Quando uma pasta é movida de um repositório de mensagens para outro repositório de um tipo diferente, o identificador de entrada é garantido para alteração.</span><span class="sxs-lookup"><span data-stu-id="5ebce-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="5ebce-116">Quando uma pasta é movida de um repositório de mensagens para outro repositório do mesmo tipo, o identificador de entrada quase sempre é alterado.</span><span class="sxs-lookup"><span data-stu-id="5ebce-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="5ebce-117">Quando uma pasta é movida para outro local no mesmo repositório de mensagens, o identificador de entrada pode ou não ser alterado, dependendo do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5ebce-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="5ebce-118">A renomeação de uma pasta sem alterar sua pasta pai normalmente não faz com que o identificador de entrada seja alterado.</span><span class="sxs-lookup"><span data-stu-id="5ebce-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ebce-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ebce-119">See also</span></span>



[<span data-ttu-id="5ebce-120">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="5ebce-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

