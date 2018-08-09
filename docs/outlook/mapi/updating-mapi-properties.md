---
title: Atualizando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770654"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="7d0de-103">Atualizando propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0de-103">Updating MAPI properties</span></span>

<span data-ttu-id="7d0de-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d0de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d0de-105">Clientes e provedores de serviços podem atualizar um valor de propriedade chamando:</span><span class="sxs-lookup"><span data-stu-id="7d0de-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="7d0de-106">Um método do objeto [IMAPIProp::SetProps](imapiprop-setprops.md) para atualizar o valor de uma ou mais das propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="7d0de-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="7d0de-107">A função [HrSetOneProp](hrsetoneprop.md) para atualizar a propriedade de apenas um por vez.</span><span class="sxs-lookup"><span data-stu-id="7d0de-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="7d0de-108">Use **HrSetOneProp** somente se o objeto de destino é local; Esta função pode causar degradação do desempenho quando usado com objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="7d0de-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="7d0de-109">O procedimento a seguir ilustra como usar **SetProps** para atualizar a classe de mensagem ou a propriedade PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7d0de-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="7d0de-110">Para atualizar a classe de mensagem de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="7d0de-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="7d0de-111">Alocar uma estrutura de [SPropValue](spropvalue.md) para a classe de mensagem e definir seus membros conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="7d0de-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="7d0de-112">Chame o método de **IMAPIProp::SetProps** da mensagem para definir a nova classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7d0de-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="7d0de-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d0de-113">See also</span></span>

- [<span data-ttu-id="7d0de-114">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="7d0de-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

