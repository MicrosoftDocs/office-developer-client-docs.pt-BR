---
title: Pastas especiais em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 013e62e06e100296a5fc702b68348bb74eb718e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770465"
---
# <a name="special-folders-in-message-stores"></a><span data-ttu-id="0080b-103">Pastas especiais em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="0080b-103">Special Folders in Message Stores</span></span>

  
  
<span data-ttu-id="0080b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0080b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0080b-105">Pastas especiais, como a caixa de entrada, a caixa de saída e a pasta de resultados de pesquisa podem ser criadas com antecedência e protegidas pelo provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0080b-105">Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider.</span></span> <span data-ttu-id="0080b-106">Se as pastas não existirem, MAPI tentará criá-los no repositório de mensagem chamando a função [HrValidateIPMSubtree](hrvalidateipmsubtree.md) .</span><span class="sxs-lookup"><span data-stu-id="0080b-106">If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function.</span></span> <span data-ttu-id="0080b-107">Para obter mais informações, consulte [Pastas especiais de MAPI](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="0080b-107">For more information, see [MAPI Special Folders](mapi-special-folders.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0080b-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="0080b-108">See also</span></span>



[<span data-ttu-id="0080b-109">Implementar pastas em repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="0080b-109">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

