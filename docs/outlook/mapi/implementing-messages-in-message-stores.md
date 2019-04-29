---
title: Implementar mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 223dfa2ac990875e98e876ab491bf09caf63e874
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416640"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="434a4-103">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="434a4-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="434a4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="434a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="434a4-105">A interface [IMessage: IMAPIProp](imessageimapiprop.md) é semelhante à interface [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) em que ambas as interfaces derivam da interface [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="434a4-105">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="434a4-106">Os clientes usam os métodos **IMAPIProp** para acessar o conteúdo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="434a4-106">Clients use the **IMAPIProp** methods to access the contents of a message.</span></span> <span data-ttu-id="434a4-107">A interface **IMessage** fornece métodos adicionais para a manipulação de mensagens (por exemplo, adição de anexos ou modificação dos destinatários de uma mensagem).</span><span class="sxs-lookup"><span data-stu-id="434a4-107">The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message).</span></span> <span data-ttu-id="434a4-108">Os métodos na interface **IMessage** modificam atributos de mensagens que não são armazenadas diretamente nas propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="434a4-108">The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="434a4-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="434a4-109">See also</span></span>



[<span data-ttu-id="434a4-110">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="434a4-110">Message Store Features</span></span>](message-store-features.md)

