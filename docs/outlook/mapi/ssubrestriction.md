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
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406322"
---
# <a name="ssubrestriction"></a><span data-ttu-id="b2e31-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="b2e31-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="b2e31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2e31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2e31-105">Descreve uma restrição de subpro objecto que é usada para filtrar as linhas da tabela de anexos ou destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b2e31-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2e31-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b2e31-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2e31-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b2e31-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="b2e31-108">Members</span><span class="sxs-lookup"><span data-stu-id="b2e31-108">Members</span></span>

 <span data-ttu-id="b2e31-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="b2e31-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="b2e31-110">Tipo de subpro objecto a ser usado como o destino da restrição.</span><span class="sxs-lookup"><span data-stu-id="b2e31-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="b2e31-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="b2e31-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="b2e31-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="b2e31-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="b2e31-113">Aplicar a restrição à tabela de destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b2e31-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="b2e31-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="b2e31-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="b2e31-115">Aplicar a restrição à tabela de anexos de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b2e31-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="b2e31-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="b2e31-116">**lpRes**</span></span>
  
> <span data-ttu-id="b2e31-117">Ponteiro para uma [estrutura SRestriction.](srestriction.md)</span><span class="sxs-lookup"><span data-stu-id="b2e31-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2e31-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e31-118">Remarks</span></span>

<span data-ttu-id="b2e31-119">As restrições de subpro object não são suportadas por todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="b2e31-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="b2e31-120">Normalmente, apenas as tabelas de conteúdo de pastas e as pastas de resultados de pesquisa têm suporte para elas.</span><span class="sxs-lookup"><span data-stu-id="b2e31-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="b2e31-121">Por exemplo, restrições de subpro object são usadas para encontrar uma mensagem que tenha um tipo específico de anexo ou destinatário.</span><span class="sxs-lookup"><span data-stu-id="b2e31-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="b2e31-122">Se uma implementação não suportar restrições de subpro object, ela retornará MAPI_E_TOO_COMPLEX de seus métodos [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow.](imapitable-findrow.md)</span><span class="sxs-lookup"><span data-stu-id="b2e31-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="b2e31-123">Para uma discussão geral sobre como funcionam as restrições, consulte [Sobre restrições.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="b2e31-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2e31-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2e31-124">See also</span></span>



[<span data-ttu-id="b2e31-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b2e31-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="b2e31-126">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b2e31-126">MAPI Structures</span></span>](mapi-structures.md)

