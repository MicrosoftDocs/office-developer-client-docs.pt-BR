---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406084"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="fcf7a-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="fcf7a-103">SPropertyRestriction</span></span>

<span data-ttu-id="fcf7a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcf7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcf7a-105">Descreve uma restrição de propriedade que é usada para corresponder a uma constante com o valor de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fcf7a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fcf7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="fcf7a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fcf7a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="fcf7a-108">Members</span><span class="sxs-lookup"><span data-stu-id="fcf7a-108">Members</span></span>

<span data-ttu-id="fcf7a-109">**re ltda**</span><span class="sxs-lookup"><span data-stu-id="fcf7a-109">**relop**</span></span>
  
> <span data-ttu-id="fcf7a-110">Operador relacional que será usado na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="fcf7a-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="fcf7a-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="fcf7a-112">RELOP_GE: a comparação é feita com base em um primeiro valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="fcf7a-113">RELOP_GT: a comparação é feita com base em um primeiro valor maior.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="fcf7a-114">RELOP_LE: a comparação é feita com base em um primeiro valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="fcf7a-115">RELOP_LT: a comparação é feita com base em um primeiro valor menor.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="fcf7a-116">RELOP_NE: a comparação é feita com base em valores de valores de valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="fcf7a-117">RELOP_RE: a comparação é feita com base nos valores LIKE (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="fcf7a-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="fcf7a-118">RELOP_EQ: a comparação é feita com base em valores iguais.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="fcf7a-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="fcf7a-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="fcf7a-120">Marca de propriedade que identifica a propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="fcf7a-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="fcf7a-121">**lpProp**</span></span>
  
> <span data-ttu-id="fcf7a-122">Ponteiro para uma [estrutura SPropValue](spropvalue.md) que contém o valor constante que será usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fcf7a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcf7a-123">Remarks</span></span>

<span data-ttu-id="fcf7a-124">Há duas marcas de propriedade em uma **estrutura SPropertyRestriction.**</span><span class="sxs-lookup"><span data-stu-id="fcf7a-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="fcf7a-125">Um está no **membro ulPropTag** e o outro está no membro **ulPropTag** da estrutura **SPropValue** apontado por **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="fcf7a-126">MAPI requires both the property identifier field and the property type field.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="fcf7a-127">**UlPropTag** em **SPropertyRestriction** é a propriedade a ser matched, e o ponteiro **lpProp** do **SPropertyRestriction** para o tipo de **ulPropTag** do **SPropValue** indica como o valor de membros da união **lpProp** são interpretados.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="fcf7a-128">Os dois tipos de propriedade devem corresponder ou o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="fcf7a-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="fcf7a-129">A ordem de comparação _é (valor da propriedade) (operador relacional) (valor constante)._</span><span class="sxs-lookup"><span data-stu-id="fcf7a-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="fcf7a-130">Quando uma restrição de propriedade é passada para **IMAPITable::Restrict** ou **IMAPITable::FindRow** e a propriedade de destino não existe, os resultados da restrição são indefinido.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="fcf7a-131">Ao criar uma **restrição AND** que une a restrição de propriedade com uma restrição **EXIST,** um chamador pode ter resultados precisos garantidos.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="fcf7a-132">Use uma [estrutura SExistRestriction](sexistrestriction.md) para definir a restrição **EXIST** e uma [estrutura SAndRestriction](sandrestriction.md) para definir a **restrição AND.**</span><span class="sxs-lookup"><span data-stu-id="fcf7a-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="fcf7a-133">As marcas de propriedade de valores múltiplos poderão ser usadas nas restrições de propriedade se o provedor de serviços que implementa a tabela as suportar.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="fcf7a-134">Se tiver suporte, as marcas de propriedade de vários valores podem ser usadas em qualquer lugar que as marcas de propriedade de valor único possam ser usadas.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="fcf7a-135">Marcas de propriedade de valores múltiplos podem ser usadas nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="fcf7a-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="fcf7a-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="fcf7a-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="fcf7a-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="fcf7a-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="fcf7a-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="fcf7a-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="fcf7a-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="fcf7a-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="fcf7a-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="fcf7a-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="fcf7a-141">Um caso notável quando as duas marcas de propriedade não corresponderem é se estiver restringindo uma propriedade de vários valores.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="fcf7a-142">Nesse caso, o seguinte deve ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-142">In this case the following must be true.</span></span> <span data-ttu-id="fcf7a-143">> Se o tipo de propriedade **da ulPropTag** de **SPropertyRestriction** contiver o sinalizador de bit do tipo de propriedade de vários valores MV_FLAG (0x1000), o tipo de propriedade **do ulPropTag** de **SPropValue** deverá corresponder ao primeiro menos o sinalizador de bit MV_FLAG, ou seja, seu inverso.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="fcf7a-144">> Por exemplo, para restringir o uso de uma propriedade de cadeia de caracteres personalizada de vários valores, como uma categoria com uma marca de propriedade para a propriedade 0x8012101f, ou seja, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), a **SPropertyRestriction** correspondente aparecerá da seguinte forma.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="fcf7a-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> observe que, se o tipo de propriedade **do ulPropTag** de **SPropValue** contiver o sinalizador MV_FLAG bit, o provável retorno será MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="fcf7a-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="fcf7a-146">Para obter mais informações sobre a **estrutura SPropertyRestriction,** consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="fcf7a-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fcf7a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcf7a-147">See also</span></span>

- [<span data-ttu-id="fcf7a-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="fcf7a-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="fcf7a-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="fcf7a-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="fcf7a-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fcf7a-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="fcf7a-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fcf7a-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="fcf7a-152">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="fcf7a-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="fcf7a-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="fcf7a-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="fcf7a-154">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="fcf7a-154">MAPI Structures</span></span>](mapi-structures.md)

