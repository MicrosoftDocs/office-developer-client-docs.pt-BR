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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336411"
---
# <a name="ssubrestriction"></a><span data-ttu-id="40653-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="40653-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="40653-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40653-105">Descreve uma restrição de subobjeto que é usada para filtrar as linhas da tabela de associação ou de destinatário de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="40653-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="40653-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="40653-106">Header file:</span></span>  <br/> |<span data-ttu-id="40653-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="40653-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="40653-108">Members</span><span class="sxs-lookup"><span data-stu-id="40653-108">Members</span></span>

 <span data-ttu-id="40653-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="40653-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="40653-110">Tipo de subobjeto a ser usado como o destino para a restrição.</span><span class="sxs-lookup"><span data-stu-id="40653-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="40653-111">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="40653-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="40653-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="40653-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="40653-113">Aplicar a restrição à tabela de destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="40653-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="40653-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="40653-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="40653-115">Aplicar a restrição à tabela de anexos de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="40653-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="40653-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="40653-116">**lpRes**</span></span>
  
> <span data-ttu-id="40653-117">Ponteiro para uma estrutura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="40653-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40653-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="40653-118">Remarks</span></span>

<span data-ttu-id="40653-119">As restrições de subobjeto não são suportadas por todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="40653-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="40653-120">Normalmente, apenas as pastas de conteúdo da pasta e de resultados de pesquisa dão suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="40653-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="40653-121">Por exemplo, as restrições de subobjeto são usadas para localizar uma mensagem que tem um tipo específico de anexo ou destinatário.</span><span class="sxs-lookup"><span data-stu-id="40653-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="40653-122">Se uma implementação não oferecer suporte a restrições de subobjeto, ela retornará MAPI_E_TOO_COMPLEX de seus métodos imApitable: [: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="40653-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="40653-123">Para uma discussão geral de como as restrições funcionam, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="40653-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40653-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="40653-124">See also</span></span>



[<span data-ttu-id="40653-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="40653-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="40653-126">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="40653-126">MAPI Structures</span></span>](mapi-structures.md)

