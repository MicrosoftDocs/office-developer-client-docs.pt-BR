---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351412"
---
# <a name="scommentrestriction"></a><span data-ttu-id="3f537-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="3f537-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="3f537-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f537-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f537-105">Descreve uma restrição de comentário, que é usada para anotar uma restrição.</span><span class="sxs-lookup"><span data-stu-id="3f537-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f537-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3f537-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f537-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3f537-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="3f537-108">Members</span><span class="sxs-lookup"><span data-stu-id="3f537-108">Members</span></span>

 <span data-ttu-id="3f537-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="3f537-109">**cValues**</span></span>
  
> <span data-ttu-id="3f537-110">Contagem de valores de propriedade na matriz apontada pelo membro **lpProp** .</span><span class="sxs-lookup"><span data-stu-id="3f537-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="3f537-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="3f537-111">**lpRes**</span></span>
  
> <span data-ttu-id="3f537-112">Ponteiro para uma estrutura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="3f537-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="3f537-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="3f537-113">**lpProp**</span></span>
  
> <span data-ttu-id="3f537-114">Ponteiro para uma matriz de estruturas [SPropValue](spropvalue.md) , cada uma contendo a marca de propriedade e o valor de uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="3f537-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3f537-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f537-115">Remarks</span></span>

<span data-ttu-id="3f537-116">A estrutura **SCommentRestriction** associa um objeto junto a um conjunto de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="3f537-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="3f537-117">As restrições de comentário são diferentes de outras restrições porque elas não são avaliadas.</span><span class="sxs-lookup"><span data-stu-id="3f537-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="3f537-118">Ou seja, eles são ignorados pelo método imApitable [:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="3f537-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="3f537-119">Não há efeito nas linhas retornadas pelo método imApitable [:: QueryRows](imapitable-queryrows.md) após uma chamada IMAPITable **:: Restrict** foi feita.</span><span class="sxs-lookup"><span data-stu-id="3f537-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="3f537-120">A estrutura **SCommentRestriction** pode ser usada para manter as informações específicas do aplicativo com uma restrição quando salva no disco.</span><span class="sxs-lookup"><span data-stu-id="3f537-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="3f537-121">Por exemplo, um cliente que salva o nome de uma propriedade nomeada usada em uma restrição de propriedade pode fazê-lo em uma estrutura **SCommentRestriction** .</span><span class="sxs-lookup"><span data-stu-id="3f537-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="3f537-122">Não é possível salvar um nome de propriedade em uma restrição de propriedade porque a estrutura [SPropertyRestriction](spropertyrestriction.md) associada contém apenas a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3f537-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="3f537-123">Para obter mais informações sobre a estrutura e as restrições do **SCommentRestriction** em geral, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="3f537-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f537-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f537-124">See also</span></span>



[<span data-ttu-id="3f537-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3f537-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3f537-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="3f537-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="3f537-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="3f537-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="3f537-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="3f537-128">MAPI Structures</span></span>](mapi-structures.md)

