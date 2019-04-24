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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357852"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="7273f-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="7273f-103">SPropertyRestriction</span></span>

<span data-ttu-id="7273f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7273f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7273f-105">Descreve uma restrição de propriedade que é usada para corresponder a uma constante com o valor de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="7273f-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7273f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7273f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7273f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7273f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="7273f-108">Members</span><span class="sxs-lookup"><span data-stu-id="7273f-108">Members</span></span>

<span data-ttu-id="7273f-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="7273f-109">**relop**</span></span>
  
> <span data-ttu-id="7273f-110">Operador relacional que será usado na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7273f-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="7273f-111">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7273f-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="7273f-112">RELOP_GE: a comparação é feita com base em um valor maior ou igual a um primeiro.</span><span class="sxs-lookup"><span data-stu-id="7273f-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="7273f-113">RELOP_GT: a comparação é feita com base em um primeiro valor maior.</span><span class="sxs-lookup"><span data-stu-id="7273f-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="7273f-114">RELOP_LE: a comparação é feita com base em um valor menor ou igual a.</span><span class="sxs-lookup"><span data-stu-id="7273f-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="7273f-115">RELOP_LT: a comparação é feita com base em um primeiro valor menor.</span><span class="sxs-lookup"><span data-stu-id="7273f-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="7273f-116">RELOP_NE: a comparação é feita com base em valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="7273f-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="7273f-117">RELOP_RE: a comparação é feita com base nos valores LIKE (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="7273f-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="7273f-118">RELOP_EQ: a comparação é feita com base em valores iguais.</span><span class="sxs-lookup"><span data-stu-id="7273f-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="7273f-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7273f-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="7273f-120">Marca de propriedade identificando a propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="7273f-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="7273f-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="7273f-121">**lpProp**</span></span>
  
> <span data-ttu-id="7273f-122">Ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém o valor da constante que será usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="7273f-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7273f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7273f-123">Remarks</span></span>

<span data-ttu-id="7273f-124">Há duas marcas de propriedade em uma estrutura **SPropertyRestriction** .</span><span class="sxs-lookup"><span data-stu-id="7273f-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="7273f-125">Um está no membro **ulPropTag** e o outro está no membro **UlPropTag** da estrutura **SPropValue** indicada por **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="7273f-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="7273f-126">O MAPI requer o campo de identificador de propriedade e o campo de tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7273f-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="7273f-127">O **ulPropTag** no **SPropertyRestriction** é a propriedade a ser correspondida e o ponteiro **lpProp** do **SPropertyRestriction** para o tipo de **ulPropTag**do **SPropValue** indica como o valor de Members do **lpProp** Union são interpretadas.</span><span class="sxs-lookup"><span data-stu-id="7273f-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="7273f-128">Os dois tipos de propriedade devem coincidir, ou o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para imApitable [:: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="7273f-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="7273f-129">A ordem de comparação é _(valor da propriedade) (operador relacional) (valor constante)_.</span><span class="sxs-lookup"><span data-stu-id="7273f-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="7273f-130">Quando uma restrição de propriedade é passada para imApitable **:: Restrict** ou IMAPITable **:: FindRow** e a propriedade target não existir, os resultados da restrição são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="7273f-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="7273f-131">Ao criar uma restrição **e** que ingresse na restrição de propriedade com uma restrição **exist** , um chamador pode ter resultados precisos garantidos.</span><span class="sxs-lookup"><span data-stu-id="7273f-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="7273f-132">Use uma estrutura [SExistRestriction](sexistrestriction.md) para definir a restrição **existir** e uma estrutura [SAndRestriction](sandrestriction.md) para definir a restrição **e** .</span><span class="sxs-lookup"><span data-stu-id="7273f-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="7273f-133">Marcas de propriedade com valores múltiplos podem ser usadas em restrições de propriedade se o provedor de serviços que está implementando a tabela oferecer suporte a elas.</span><span class="sxs-lookup"><span data-stu-id="7273f-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="7273f-134">Se houver suporte, as marcas de propriedade de vários valores poderão ser usadas em qualquer lugar de propriedades de valor único.</span><span class="sxs-lookup"><span data-stu-id="7273f-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="7273f-135">Marcas de propriedade com valores múltiplos podem ser usadas nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="7273f-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="7273f-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="7273f-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="7273f-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7273f-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="7273f-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7273f-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="7273f-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="7273f-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="7273f-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7273f-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="7273f-141">Um caso notável quando as duas marcas de propriedade não coincidem é se a restrição de uma propriedade de vários valores.</span><span class="sxs-lookup"><span data-stu-id="7273f-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="7273f-142">Nesse caso, o seguinte deve ser verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7273f-142">In this case the following must be true.</span></span> <span data-ttu-id="7273f-143">> se o tipo de Propriedade do **ulPropTag** de **SPropertyRestriction** contiver o sinalizador de bit de tipo de propriedade de vários valores MV_FLAG (0x1000), o tipo de Propriedade do **ulPropTag** de **SPropValue** deverá corresponder ao antigo menos o MV_ Sinalizador de bit FLAG, ou seja, o inverso.</span><span class="sxs-lookup"><span data-stu-id="7273f-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="7273f-144">> por exemplo, para restringir o uso de uma propriedade de cadeia de caracteres personalizada de vários valores, como uma categoria com uma marca de propriedade para a propriedade 0x8012101f, ou seja, PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), o **SPropertyRestriction** correspondente apareceria como maneira.</span><span class="sxs-lookup"><span data-stu-id="7273f-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="7273f-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> Observe que, se o tipo de Propriedade do *\*ulPropTag** de *\*SPropValue** contiver o sinalizador de bit MV_FLAG, o provável retorno é MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="7273f-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property\`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid\`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";\`> Note that if the property type of the *\*ulPropTag** of *\*SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="7273f-146">Para obter mais informações sobre a estrutura **SPropertyRestriction** , consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7273f-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7273f-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="7273f-147">See also</span></span>

- [<span data-ttu-id="7273f-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="7273f-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="7273f-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="7273f-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="7273f-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7273f-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="7273f-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7273f-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="7273f-152">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="7273f-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="7273f-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="7273f-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="7273f-154">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="7273f-154">MAPI Structures</span></span>](mapi-structures.md)

