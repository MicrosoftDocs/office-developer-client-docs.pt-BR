---
title: Abrir um repositório de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436024"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="1a14a-103">Abrir um repositório de mensagens padrão</span><span class="sxs-lookup"><span data-stu-id="1a14a-103">Opening the default message store</span></span>

<span data-ttu-id="1a14a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a14a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a14a-105">Em qualquer sessão específica, um armazenamento de mensagens atua como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="1a14a-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="1a14a-106">Um armazenamento de mensagens padrão tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="1a14a-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="1a14a-107">A **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) é definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="1a14a-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="1a14a-108">O STATUS_DEFAULT_STORE sinalizador é definido **na propriedade PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1a14a-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="1a14a-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span><span class="sxs-lookup"><span data-stu-id="1a14a-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="1a14a-110">Para obter mais informações sobre essas pastas, consulte [Subárvore IPM](ipm-subtree.md) e [Pastas Especiais MAPI.](mapi-special-folders.md)</span><span class="sxs-lookup"><span data-stu-id="1a14a-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="1a14a-111">Para recuperar o identificador de entrada para o armazenamento de mensagens padrão, você deve chamar [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela de armazenamento de mensagens e aplicar uma restrição apropriada em uma chamada para [HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="1a14a-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="1a14a-112">**HrQueryAllRows** retornará um conjunto de linhas com a única linha que representa o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="1a14a-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="1a14a-113">A restrição que você passa **para HrQueryAllRows** pode assumir em um dos seguintes formulários:</span><span class="sxs-lookup"><span data-stu-id="1a14a-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="1a14a-114">Uma **restrição AND** que usa uma **estrutura SAndRestriction** para combinar:</span><span class="sxs-lookup"><span data-stu-id="1a14a-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="1a14a-115">Existe uma restrição que usa **uma estrutura SExistRestriction** para testar a existência da **PR_DEFAULT_STORE** propriedade.</span><span class="sxs-lookup"><span data-stu-id="1a14a-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="1a14a-116">Uma restrição de propriedade que usa uma [estrutura SPropertyRestriction](spropertyrestriction.md) para verificar o valor TRUE na **PR_DEFAULT_STORE** propriedade.</span><span class="sxs-lookup"><span data-stu-id="1a14a-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="1a14a-117">Uma restrição de bitmask que usa uma estrutura [SBitMaskRestriction](sbitmaskrestriction.md) para aplicar STATUS_DEFAULT_STORE como uma máscara contra a **PR_RESOURCE_FLAGS** propriedade.</span><span class="sxs-lookup"><span data-stu-id="1a14a-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1a14a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a14a-118">See also</span></span>

- [<span data-ttu-id="1a14a-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="1a14a-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="1a14a-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="1a14a-120">SAndRestriction</span></span>](sandrestriction.md)

