---
title: Atualizando propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 172abe64073b11d98bfb5f76999237218ef8944a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581346"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="f9b86-103">Atualizando propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f9b86-103">Updating MAPI properties</span></span>

<span data-ttu-id="f9b86-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9b86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9b86-105">Clientes e provedores de serviços podem atualizar um valor de propriedade chamando:</span><span class="sxs-lookup"><span data-stu-id="f9b86-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="f9b86-106">Um método do objeto [IMAPIProp::SetProps](imapiprop-setprops.md) para atualizar o valor de uma ou mais das propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="f9b86-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="f9b86-107">A função [HrSetOneProp](hrsetoneprop.md) para atualizar a propriedade de apenas um por vez.</span><span class="sxs-lookup"><span data-stu-id="f9b86-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="f9b86-108">Use **HrSetOneProp** somente se o objeto de destino é local; Esta função pode causar degradação do desempenho quando usado com objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="f9b86-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="f9b86-109">O procedimento a seguir ilustra como usar **SetProps** para atualizar a classe de mensagem ou a propriedade PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f9b86-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="f9b86-110">Para atualizar a classe de mensagem de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="f9b86-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="f9b86-111">Alocar uma estrutura de [SPropValue](spropvalue.md) para a classe de mensagem e definir seus membros conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="f9b86-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="f9b86-112">Chame o método de **IMAPIProp::SetProps** da mensagem para definir a nova classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f9b86-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="f9b86-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9b86-113">See also</span></span>

- [<span data-ttu-id="f9b86-114">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="f9b86-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

