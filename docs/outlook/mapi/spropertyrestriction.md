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
ms.openlocfilehash: 7d588380ccc84f51fe58bb0f092d5287b12b4270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586533"
---
# <a name="spropertyrestriction"></a><span data-ttu-id="68b44-103">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="68b44-103">SPropertyRestriction</span></span>

<span data-ttu-id="68b44-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68b44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68b44-105">Descreve uma restrição de propriedade que será usada para corresponder a uma constante com o valor de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="68b44-105">Describes a property restriction that is used to match a constant with the value of a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68b44-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="68b44-106">Header file:</span></span>  <br/> |<span data-ttu-id="68b44-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68b44-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a><span data-ttu-id="68b44-108">Members</span><span class="sxs-lookup"><span data-stu-id="68b44-108">Members</span></span>

<span data-ttu-id="68b44-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="68b44-109">**relop**</span></span>
  
> <span data-ttu-id="68b44-110">Operador relacional que será usado na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="68b44-110">Relational operator that will be used in the search.</span></span> <span data-ttu-id="68b44-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="68b44-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="68b44-112">RELOP_GE: A comparação é feita com base no primeiro um valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="68b44-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
        
  - <span data-ttu-id="68b44-113">RELOP_GT: A comparação é feita com base em um valor maior de primeiro.</span><span class="sxs-lookup"><span data-stu-id="68b44-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
        
  - <span data-ttu-id="68b44-114">RELOP_LE: A comparação é feita com base no primeiro um valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="68b44-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
        
  - <span data-ttu-id="68b44-115">RELOP_LT: A comparação é feita com base em um valor menor de primeiro.</span><span class="sxs-lookup"><span data-stu-id="68b44-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
        
  - <span data-ttu-id="68b44-116">RELOP_NE: A comparação é feita com base nos valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="68b44-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
        
  - <span data-ttu-id="68b44-117">RELOP_RE: A comparação é feita com base em como valores (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="68b44-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
        
  - <span data-ttu-id="68b44-118">RELOP_EQ: A comparação é feita com base nos valores iguais.</span><span class="sxs-lookup"><span data-stu-id="68b44-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="68b44-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="68b44-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="68b44-120">Marca de propriedade que identifica a propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="68b44-120">Property tag identifying the property to be compared.</span></span> 
    
<span data-ttu-id="68b44-121">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="68b44-121">**lpProp**</span></span>
  
> <span data-ttu-id="68b44-122">Ponteiro para uma estrutura [SPropValue](spropvalue.md) que contém o valor da constante que será usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="68b44-122">Pointer to an [SPropValue](spropvalue.md) structure that contains the constant value that will be used in the comparison.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="68b44-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="68b44-123">Remarks</span></span>

<span data-ttu-id="68b44-124">Há duas marcas de propriedade em uma estrutura **SPropertyRestriction** .</span><span class="sxs-lookup"><span data-stu-id="68b44-124">There are two property tags in an **SPropertyRestriction** structure.</span></span> <span data-ttu-id="68b44-125">Uma é no membro **ulPropTag** e o outro for no membro **ulPropTag** da estrutura **SPropValue** apontado pela **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="68b44-125">One is in the **ulPropTag** member and the other is in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="68b44-126">MAPI requer o campo do identificador de propriedade e um campo de tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="68b44-126">MAPI requires both the property identifier field and the property type field.</span></span> <span data-ttu-id="68b44-127">O **ulPropTag** em **SPropertyRestriction** é a propriedade a ser correspondido e o ponteiro de **lpProp** de **SPropertyRestriction** o tipo do **ulPropTag**do **SPropValue** indica como o valor de membros do União **lpProp** são interpretadas.</span><span class="sxs-lookup"><span data-stu-id="68b44-127">The **ulPropTag** in **SPropertyRestriction** is the property to be matched, and the **lpProp** pointer of the **SPropertyRestriction** to the **ulPropTag**'s type of the **SPropValue** indicates how the members value of the **lpProp** union are interpreted.</span></span> <span data-ttu-id="68b44-128">Os tipos de dois propriedade devem corresponder, senão o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="68b44-128">The two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="68b44-129">A ordem de comparação é _(valor da propriedade) (operador relacional) (valor de constante)_.</span><span class="sxs-lookup"><span data-stu-id="68b44-129">The comparison order is  _(property value) (relational operator) (constant value)_.</span></span>
  
<span data-ttu-id="68b44-130">Quando uma restrição de propriedade é passada para **IMAPITable:: Restrict** ou **IMAPITable:: FindRow** e a propriedade de destino não existir, os resultados da restrição são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="68b44-130">When a property restriction is passed to **IMAPITable::Restrict** or **IMAPITable::FindRow** and the target property does not exist, the results of the restriction are undefined.</span></span> <span data-ttu-id="68b44-131">Criando uma restrição **AND** que une a restrição de propriedade com uma restrição **EXISTEM** , um chamador pode ser garantido resultados exatos.</span><span class="sxs-lookup"><span data-stu-id="68b44-131">By creating an **AND** restriction that joins the property restriction with an **EXIST** restriction, a caller can be guaranteed accurate results.</span></span> <span data-ttu-id="68b44-132">Use uma estrutura de [SExistRestriction](sexistrestriction.md) para definir a restrição **existe** e uma estrutura de [SAndRestriction](sandrestriction.md) para definir a restrição **AND** .</span><span class="sxs-lookup"><span data-stu-id="68b44-132">Use an [SExistRestriction](sexistrestriction.md) structure to define the **EXIST** restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="68b44-133">Marcas de valores múltiplos de propriedade podem ser usadas em restrições de propriedade, se o provedor de serviço implementando a tabela oferece suporte a eles.</span><span class="sxs-lookup"><span data-stu-id="68b44-133">Multi-valued property tags can be used in property restrictions if the service provider implementing the table supports them.</span></span> <span data-ttu-id="68b44-134">Se houver suporte, marcas de propriedade de valores múltiplos podem ser marcas de propriedade de valor único podem ser usadas em qualquer lugar usadas.</span><span class="sxs-lookup"><span data-stu-id="68b44-134">If supported, multi-valued property tags can be used anywhere single-valued property tags can be used.</span></span> 
  
<span data-ttu-id="68b44-135">Marcas de propriedade de valores múltiplos podem ser usadas nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="68b44-135">Multi-valued property tags can be used in the following methods:</span></span>
  
- [<span data-ttu-id="68b44-136">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="68b44-136">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="68b44-137">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="68b44-137">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
    
- [<span data-ttu-id="68b44-138">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="68b44-138">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
- [<span data-ttu-id="68b44-139">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="68b44-139">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="68b44-140">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="68b44-140">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
> [!IMPORTANT]
> <span data-ttu-id="68b44-141">Uma ocorrência notável quando as marcas de duas propriedade não coincidem com é se restringindo em uma propriedade de valor múltiplos.</span><span class="sxs-lookup"><span data-stu-id="68b44-141">A notable case when the two property tags won't match is if restricting on a multi-value property.</span></span> <span data-ttu-id="68b44-142">Nesse caso, a seguir deve ser verdadeira.</span><span class="sxs-lookup"><span data-stu-id="68b44-142">In this case the following must be true.</span></span> <span data-ttu-id="68b44-143">> Se o tipo de propriedade do **ulPropTag** de **SPropertyRestriction** contém o sinalizador de bit de tipo de propriedade de valores múltiplos MV_FLAG (0x1000), o tipo de propriedade do **ulPropTag** de **SPropValue** deve corresponder ao primeiro menos o MV_ Sinalizador de bit de sinalizador, ou seja, seu inverso.</span><span class="sxs-lookup"><span data-stu-id="68b44-143">> If the property type of the **ulPropTag** of **SPropertyRestriction** contains the multi-value property type bit flag MV_FLAG (0x1000), the property type of the **ulPropTag** of **SPropValue** should match the former minus the MV_FLAG bit flag, that is, its inverse.</span></span> <span data-ttu-id="68b44-144">> Por exemplo, para restringir usando uma propriedade de cadeia de caracteres de valores múltiplos personalizada, como uma categoria com uma marca de propriedade para a propriedade 0x8012101f, ou seja, PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), o correspondente **SPropertyRestriction** apareceria como segue.</span><span class="sxs-lookup"><span data-stu-id="68b44-144">> For example, to restrict using a multi-value custom string property such as a category with a property tag for the property 0x8012101f, that is, PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), the corresponding **SPropertyRestriction** would appear as follows.</span></span><span data-ttu-id="68b44-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Observe que, se o tipo de propriedade do **ulPropTag** de **SPropValue** contiver o sinalizador de bit MV_FLAG, o retorno provavelmente é MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="68b44-145"> >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Note that if the property type of the **ulPropTag** of **SPropValue** contains the MV_FLAG bit flag, the likely return is MAPI_E_TOO_COMPLEX.</span></span> 
  
<span data-ttu-id="68b44-146">Para obter mais informações sobre a estrutura **SPropertyRestriction** , consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="68b44-146">For more information about the **SPropertyRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68b44-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="68b44-147">See also</span></span>

- [<span data-ttu-id="68b44-148">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="68b44-148">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="68b44-149">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="68b44-149">SAndRestriction</span></span>](sandrestriction.md)
- [<span data-ttu-id="68b44-150">SPropValue</span><span class="sxs-lookup"><span data-stu-id="68b44-150">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="68b44-151">SRestriction</span><span class="sxs-lookup"><span data-stu-id="68b44-151">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="68b44-152">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="68b44-152">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
- [<span data-ttu-id="68b44-153">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="68b44-153">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
- [<span data-ttu-id="68b44-154">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="68b44-154">MAPI Structures</span></span>](mapi-structures.md)

