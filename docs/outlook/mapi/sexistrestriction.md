---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339274"
---
# <a name="sexistrestriction"></a><span data-ttu-id="19d2d-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="19d2d-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="19d2d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19d2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19d2d-105">Descreve uma restrição exist que é usada para testar se uma propriedade específica existe como uma coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="19d2d-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19d2d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="19d2d-106">Header file:</span></span>  <br/> |<span data-ttu-id="19d2d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="19d2d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="19d2d-108">Members</span><span class="sxs-lookup"><span data-stu-id="19d2d-108">Members</span></span>

 <span data-ttu-id="19d2d-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="19d2d-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="19d2d-110">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="19d2d-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="19d2d-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="19d2d-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="19d2d-112">Marca de propriedade identificando a coluna a ser testada para existência em cada linha.</span><span class="sxs-lookup"><span data-stu-id="19d2d-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="19d2d-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="19d2d-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="19d2d-114">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="19d2d-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19d2d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="19d2d-115">Remarks</span></span>

<span data-ttu-id="19d2d-116">A restrição exist é usada para garantir resultados significativos para outros tipos de restrições que envolvem Propriedades, como restrições de propriedade e de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="19d2d-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="19d2d-117">Quando uma restrição que envolve uma propriedade é passada para [IMAPITable:: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md) e a propriedade não existir, os resultados da restrição são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="19d2d-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="19d2d-118">Ao criar uma restrição **e** que ingresse na restrição de propriedade com uma restrição exist, um chamador pode ter resultados precisos garantidos.</span><span class="sxs-lookup"><span data-stu-id="19d2d-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="19d2d-119">As restrições existem não podem ser usadas com propriedades de subobjeto que tenham o tipo PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="19d2d-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="19d2d-120">Para obter mais informações sobre a estrutura **SExistRestriction** , consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="19d2d-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19d2d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="19d2d-121">See also</span></span>



[<span data-ttu-id="19d2d-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="19d2d-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="19d2d-123">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="19d2d-123">MAPI Structures</span></span>](mapi-structures.md)

