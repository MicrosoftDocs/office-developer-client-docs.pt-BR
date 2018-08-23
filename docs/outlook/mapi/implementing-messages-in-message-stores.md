---
title: Implementar mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1d68a5258739a8952df97ddceb07ebe6d9c8d2d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568124"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="7bbc6-103">Implementar mensagens em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="7bbc6-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="7bbc6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bbc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bbc6-105">O [IMessage: IMAPIProp](imessageimapiprop.md) interface é semelhante do [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface nessa derivam de ambas as interfaces do [IMAPIProp: IUnknown](imapipropiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="7bbc6-105">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="7bbc6-106">Clientes usam os métodos **IMAPIProp** para acessar o conteúdo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7bbc6-106">Clients use the **IMAPIProp** methods to access the contents of a message.</span></span> <span data-ttu-id="7bbc6-107">A interface **IMessage** fornece métodos adicionais para a manipulação de mensagens (por exemplo, a adição de anexos ou modificar os destinatários de uma mensagem).</span><span class="sxs-lookup"><span data-stu-id="7bbc6-107">The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message).</span></span> <span data-ttu-id="7bbc6-108">Os métodos na interface do **IMessage** modificam atributos de mensagens que não são armazenadas diretamente nas propriedades da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7bbc6-108">The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7bbc6-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bbc6-109">See also</span></span>



[<span data-ttu-id="7bbc6-110">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="7bbc6-110">Message Store Features</span></span>](message-store-features.md)

