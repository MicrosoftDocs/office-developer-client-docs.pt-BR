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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418936"
---
# <a name="sexistrestriction"></a><span data-ttu-id="5843e-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="5843e-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="5843e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5843e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5843e-105">Descreve uma restrição exist que é usada para testar se uma propriedade específica existe como uma coluna na tabela.</span><span class="sxs-lookup"><span data-stu-id="5843e-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5843e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5843e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5843e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5843e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="5843e-108">Members</span><span class="sxs-lookup"><span data-stu-id="5843e-108">Members</span></span>

 <span data-ttu-id="5843e-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="5843e-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="5843e-110">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5843e-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="5843e-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="5843e-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="5843e-112">Marca de propriedade identificando a coluna a ser testada para existência em cada linha.</span><span class="sxs-lookup"><span data-stu-id="5843e-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="5843e-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="5843e-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="5843e-114">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5843e-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5843e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5843e-115">Remarks</span></span>

<span data-ttu-id="5843e-116">A restrição exist é usada para garantir resultados significativos para outros tipos de restrições que envolvem Propriedades, como restrições de propriedade e de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5843e-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="5843e-117">Quando uma restrição que envolve uma propriedade é passada para [IMAPITable:: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md) e a propriedade não existir, os resultados da restrição são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="5843e-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="5843e-118">Ao criar uma restrição **e** que ingresse na restrição de propriedade com uma restrição exist, um chamador pode ter resultados precisos garantidos.</span><span class="sxs-lookup"><span data-stu-id="5843e-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="5843e-119">As restrições existem não podem ser usadas com propriedades de subobjeto que tenham o tipo PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="5843e-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="5843e-120">Para obter mais informações sobre a estrutura **SExistRestriction** , consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="5843e-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5843e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5843e-121">See also</span></span>



[<span data-ttu-id="5843e-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="5843e-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="5843e-123">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="5843e-123">MAPI Structures</span></span>](mapi-structures.md)

