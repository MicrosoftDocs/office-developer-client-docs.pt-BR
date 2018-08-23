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
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571945"
---
# <a name="sexistrestriction"></a><span data-ttu-id="34fcf-103">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="34fcf-103">SExistRestriction</span></span>

  
  
<span data-ttu-id="34fcf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34fcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34fcf-105">Descreve uma restrição existem que é usada para testar se uma determinada propriedade existe como uma coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="34fcf-105">Describes an exist restriction which is used to test whether a particular property exists as a column in the table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34fcf-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="34fcf-106">Header file:</span></span>  <br/> |<span data-ttu-id="34fcf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34fcf-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a><span data-ttu-id="34fcf-108">Members</span><span class="sxs-lookup"><span data-stu-id="34fcf-108">Members</span></span>

 <span data-ttu-id="34fcf-109">**ulReserved1**</span><span class="sxs-lookup"><span data-stu-id="34fcf-109">**ulReserved1**</span></span>
  
> <span data-ttu-id="34fcf-110">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="34fcf-110">Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="34fcf-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="34fcf-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="34fcf-112">Marca de propriedade que identifica a coluna a ser testado existência em cada linha.</span><span class="sxs-lookup"><span data-stu-id="34fcf-112">Property tag identifying the column to be tested for existence in each row.</span></span>
    
 <span data-ttu-id="34fcf-113">**ulReserved2**</span><span class="sxs-lookup"><span data-stu-id="34fcf-113">**ulReserved2**</span></span>
  
> <span data-ttu-id="34fcf-114">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="34fcf-114">Reserved; must be zero.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34fcf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="34fcf-115">Remarks</span></span>

<span data-ttu-id="34fcf-116">A restrição da lista é usada para garantir resultados significativos para outros tipos de restrições que envolvem propriedades, como restrições de propriedade e conteúdo.</span><span class="sxs-lookup"><span data-stu-id="34fcf-116">The exist restriction is used to guarantee meaningful results for other types of restrictions that involve properties, such as property and content restrictions.</span></span> <span data-ttu-id="34fcf-117">Quando uma restrição que envolva uma propriedade é passada para [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) e a propriedade não existir, os resultados da restrição são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="34fcf-117">When a restriction that involves a property is passed to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) and the property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="34fcf-118">Criando uma restrição **e** que une a restrição de propriedade com uma restrição existem, um chamador pode ser garantido resultados exatos.</span><span class="sxs-lookup"><span data-stu-id="34fcf-118">By creating an **AND** restriction that joins the property restriction with an exist restriction, a caller can be guaranteed accurate results.</span></span> 
  
<span data-ttu-id="34fcf-119">Existem restrições não podem ser usadas com propriedades do objeto sub-recurso que têm tipo PT_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="34fcf-119">Exist restrictions cannot be used with sub-object properties that have type PT_OBJECT.</span></span> 
  
<span data-ttu-id="34fcf-120">Para obter mais informações sobre a estrutura **SExistRestriction** , consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="34fcf-120">For more information about the **SExistRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34fcf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="34fcf-121">See also</span></span>



[<span data-ttu-id="34fcf-122">SRestriction</span><span class="sxs-lookup"><span data-stu-id="34fcf-122">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="34fcf-123">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="34fcf-123">MAPI Structures</span></span>](mapi-structures.md)

