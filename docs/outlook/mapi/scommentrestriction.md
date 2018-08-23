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
ms.openlocfilehash: 84fb79b1922669db9c8e5d518a833a6866f11cea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589179"
---
# <a name="scommentrestriction"></a><span data-ttu-id="dbc84-103">SCommentRestriction</span><span class="sxs-lookup"><span data-stu-id="dbc84-103">SCommentRestriction</span></span>

  
  
<span data-ttu-id="dbc84-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbc84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbc84-105">Descreve uma restrição de comentário, que é usada para anotar uma restrição.</span><span class="sxs-lookup"><span data-stu-id="dbc84-105">Describes a comment restriction, which is used to annotate a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbc84-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dbc84-106">Header file:</span></span>  <br/> |<span data-ttu-id="dbc84-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dbc84-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a><span data-ttu-id="dbc84-108">Members</span><span class="sxs-lookup"><span data-stu-id="dbc84-108">Members</span></span>

 <span data-ttu-id="dbc84-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="dbc84-109">**cValues**</span></span>
  
> <span data-ttu-id="dbc84-110">Contagem de valores de propriedade na matriz apontado pelo membro **lpProp** .</span><span class="sxs-lookup"><span data-stu-id="dbc84-110">Count of property values in the array pointed to by the **lpProp** member.</span></span> 
    
 <span data-ttu-id="dbc84-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="dbc84-111">**lpRes**</span></span>
  
> <span data-ttu-id="dbc84-112">Ponteiro para uma estrutura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="dbc84-112">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
 <span data-ttu-id="dbc84-113">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="dbc84-113">**lpProp**</span></span>
  
> <span data-ttu-id="dbc84-114">Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) , cada um contendo a marca de propriedade e o valor de uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="dbc84-114">Pointer to an array of [SPropValue](spropvalue.md) structures, each containing the property tag and value for a named property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dbc84-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbc84-115">Remarks</span></span>

<span data-ttu-id="dbc84-116">A estrutura **SCommentRestriction** associa um objeto junto com um conjunto de propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="dbc84-116">The **SCommentRestriction** structure associates an object together with a set of named properties.</span></span> <span data-ttu-id="dbc84-117">Restrições de comentário são Diferentemente de outras restrições, pois eles não são avaliados.</span><span class="sxs-lookup"><span data-stu-id="dbc84-117">Comment restrictions are unlike other restrictions because they are not evaluated.</span></span> <span data-ttu-id="dbc84-118">Ou seja, eles são ignorados pelo método [IMAPITable:: Restrict](imapitable-restrict.md) .</span><span class="sxs-lookup"><span data-stu-id="dbc84-118">That is, they are ignored by the [IMAPITable::Restrict](imapitable-restrict.md) method.</span></span> <span data-ttu-id="dbc84-119">Não há nenhum efeito sobre as linhas retornadas pelo método [IMAPITable:: QueryRows](imapitable-queryrows.md) após ter sido feita uma chamada **IMAPITable:: Restrict** .</span><span class="sxs-lookup"><span data-stu-id="dbc84-119">There is no effect on the rows returned by the [IMAPITable::QueryRows](imapitable-queryrows.md) method after an **IMAPITable::Restrict** call has been made.</span></span> 
  
<span data-ttu-id="dbc84-120">A estrutura de **SCommentRestriction** pode ser usada para manter informações específicas do aplicativo com uma restrição quando ele for salvo no disco.</span><span class="sxs-lookup"><span data-stu-id="dbc84-120">The **SCommentRestriction** structure can be used to keep application-specific information with a restriction when it is saved on disk.</span></span> <span data-ttu-id="dbc84-121">Por exemplo, um cliente a salvando o nome de uma propriedade nomeada usado em uma restrição de propriedade poderá fazer isso em uma estrutura **SCommentRestriction** .</span><span class="sxs-lookup"><span data-stu-id="dbc84-121">For example, a client saving the name of a named property used in a property restriction can do so in an **SCommentRestriction** structure.</span></span> <span data-ttu-id="dbc84-122">Salvar um nome de propriedade não é possível em uma restrição de propriedade, porque a estrutura de [SPropertyRestriction](spropertyrestriction.md) associada contém apenas a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="dbc84-122">Saving a property name is not possible in a property restriction because the associated [SPropertyRestriction](spropertyrestriction.md) structure holds only the property tag.</span></span> 
  
<span data-ttu-id="dbc84-123">Para obter mais informações sobre a estrutura de **SCommentRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="dbc84-123">For more information about the **SCommentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbc84-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc84-124">See also</span></span>



[<span data-ttu-id="dbc84-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="dbc84-125">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="dbc84-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="dbc84-126">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="dbc84-127">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="dbc84-127">SPropertyRestriction</span></span>](spropertyrestriction.md)


[<span data-ttu-id="dbc84-128">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="dbc84-128">MAPI Structures</span></span>](mapi-structures.md)

