---
title: Abrindo o armazenamento de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768163"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="d7e93-103">Abrindo o armazenamento de mensagens padrão</span><span class="sxs-lookup"><span data-stu-id="d7e93-103">Opening the default message store</span></span>

<span data-ttu-id="d7e93-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7e93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7e93-105">Em qualquer sessão específica, um armazenamento de mensagens atua como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="d7e93-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="d7e93-106">Um armazenamento de mensagens padrão tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="d7e93-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="d7e93-107">A propriedade **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) é definida como TRUE.</span><span class="sxs-lookup"><span data-stu-id="d7e93-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="d7e93-108">O sinalizador STATUS_DEFAULT_STORE é definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7e93-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d7e93-109">MAPI cria automaticamente a subárvore IPM e as pastas raiz para resultados de pesquisa, modos de exibição comuns e exibições pessoais quando o armazenamento de mensagens é aberto.</span><span class="sxs-lookup"><span data-stu-id="d7e93-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="d7e93-110">Para obter mais informações sobre essas pastas, consulte [Subárvore IPM](ipm-subtree.md) e [Pastas especiais de MAPI](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="d7e93-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="d7e93-111">Para recuperar o identificador de entrada para o armazenamento de mensagens padrão, você deve chamar [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir a tabela de repositório de mensagens e aplicar uma restrição apropriada em uma chamada para [HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="d7e93-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="d7e93-112">**HrQueryAllRows** retornará uma linha definidas com uma linha que representa o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="d7e93-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="d7e93-113">A restrição que você passa para **HrQueryAllRows** pode ser realizadas em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="d7e93-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="d7e93-114">Uma restrição **e** que usa uma estrutura de **SAndRestriction** para combinar:</span><span class="sxs-lookup"><span data-stu-id="d7e93-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="d7e93-115">Uma restrição que usa uma estrutura de **SExistRestriction** para testar a existência da propriedade **PR_DEFAULT_STORE** de existir.</span><span class="sxs-lookup"><span data-stu-id="d7e93-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="d7e93-116">Uma restrição de propriedade que usa uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para verificar o valor TRUE na propriedade **PR_DEFAULT_STORE** .</span><span class="sxs-lookup"><span data-stu-id="d7e93-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="d7e93-117">Uma restrição de bitmask que usa uma estrutura de [SBitMaskRestriction](sbitmaskrestriction.md) para a aplicação de STATUS_DEFAULT_STORE como uma máscara contra a propriedade **PR_RESOURCE_FLAGS** .</span><span class="sxs-lookup"><span data-stu-id="d7e93-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d7e93-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7e93-118">See also</span></span>

- [<span data-ttu-id="d7e93-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="d7e93-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="d7e93-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="d7e93-120">SAndRestriction</span></span>](sandrestriction.md)

