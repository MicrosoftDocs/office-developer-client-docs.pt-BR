---
title: Localizar o ícone de uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766541"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="4bfc3-103">Localizar o ícone de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="4bfc3-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="4bfc3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4bfc3-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="4bfc3-105">**Para localizar o ícone associado a uma mensagem**</span><span class="sxs-lookup"><span data-stu-id="4bfc3-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="4bfc3-106">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da mensagem para recuperar sua propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4bfc3-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="4bfc3-107">Chame [MAPIOpenFormMgr](mapiopenformmgr.md) para recuperar um ponteiro de interface **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="4bfc3-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="4bfc3-108">Passe o ponteiro **IMAPISession** no parâmetro _pSession_ .</span><span class="sxs-lookup"><span data-stu-id="4bfc3-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="4bfc3-109">Chame [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para recuperar um ponteiro de interface **IMAPIFormInfo** .</span><span class="sxs-lookup"><span data-stu-id="4bfc3-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="4bfc3-110">Use o ponteiro de **IMAPIFormInfo** para chamar [IMAPIProp::GetProps](imapiprop-getprops.md) e recuperar o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) e/ou propriedades **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4bfc3-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

