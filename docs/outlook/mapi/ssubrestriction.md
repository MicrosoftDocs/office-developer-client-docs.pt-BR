---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 152f3032876d6473f1716afa46507196cd5ecc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770493"
---
# <a name="ssubrestriction"></a><span data-ttu-id="0421a-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="0421a-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="0421a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0421a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0421a-105">Descreve uma restrição de subsites do objeto que é usada para filtrar as linhas de anexo de uma mensagem ou tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="0421a-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0421a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0421a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0421a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0421a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="0421a-108">Members</span><span class="sxs-lookup"><span data-stu-id="0421a-108">Members</span></span>

 <span data-ttu-id="0421a-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="0421a-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="0421a-110">Tipo de objeto sub-recurso para servir como o destino para a restrição.</span><span class="sxs-lookup"><span data-stu-id="0421a-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="0421a-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="0421a-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="0421a-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="0421a-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="0421a-113">Aplica a restrição a tabela de destinatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0421a-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="0421a-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="0421a-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="0421a-115">Aplica a restrição a tabela de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0421a-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="0421a-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="0421a-116">**lpRes**</span></span>
  
> <span data-ttu-id="0421a-117">Ponteiro para uma estrutura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="0421a-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0421a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0421a-118">Remarks</span></span>

<span data-ttu-id="0421a-119">Restrições do objeto sub-recurso não são compatíveis com todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="0421a-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="0421a-120">Normalmente, tabelas de conteúdo da pasta somente e pastas de resultados de pesquisa dão suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="0421a-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="0421a-121">Por exemplo, restrições de objeto sub-recurso são usadas para localizar uma mensagem que tenha um tipo de anexo ou um destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="0421a-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="0421a-122">Se uma implementação não oferece suporte a restrições do objeto subsites, ele retornará MAPI_E_TOO_COMPLEX de seus métodos [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="0421a-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="0421a-123">Para obter uma discussão geral de como funcionam os restrições, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="0421a-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0421a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0421a-124">See also</span></span>



[<span data-ttu-id="0421a-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="0421a-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="0421a-126">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0421a-126">MAPI Structures</span></span>](mapi-structures.md)

