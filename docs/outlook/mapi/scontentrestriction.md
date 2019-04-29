---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423661"
---
# <a name="scontentrestriction"></a><span data-ttu-id="9a85c-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="9a85c-103">SContentRestriction</span></span>
 
<span data-ttu-id="9a85c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a85c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a85c-105">Descreve uma restrição de conteúdo, que é usada para limitar um modo de exibição de tabela apenas às linhas que incluem uma coluna com conteúdo correspondente a uma cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a85c-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a85c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9a85c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a85c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9a85c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="9a85c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9a85c-108">Members</span></span>

<span data-ttu-id="9a85c-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="9a85c-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="9a85c-110">Configurações de opção que definem o nível de precisão que a restrição de conteúdo deve impor quando você verifica se há uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="9a85c-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="9a85c-111">Os **16 bits inferiores** do membro **ulFuzzyLevel** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8 e devem ser definidos como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9a85c-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="9a85c-112">FL_FULLSTRING: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida na propriedade identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="9a85c-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="9a85c-113">FL_PREFIX: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve aparecer no início da propriedade identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="9a85c-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="9a85c-114">As duas cadeias de caracteres devem ser comparadas apenas com o comprimento da cadeia de caracteres de pesquisa indicada por **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="9a85c-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="9a85c-115">FL_SUBSTRING: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida em qualquer lugar na propriedade identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="9a85c-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="9a85c-116">Os **16 bits superiores** do membro **ulFuzzyLevel** se aplicam apenas às propriedades do tipo PT_STRING8 e podem ser definidos com os seguintes valores em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="9a85c-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="9a85c-117">FL_IGNORECASE: a comparação deve ser feita sem considerar o uso de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9a85c-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="9a85c-118">FL_IGNORENONSPACE: a comparação deve ignorar caracteres de espaçamento não definidos por Unicode, como marcas diacríticos.</span><span class="sxs-lookup"><span data-stu-id="9a85c-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="9a85c-119">FL_LOOSE: a comparação deve fornecer uma correspondência sempre que possível, ignorando os caracteres de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9a85c-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="9a85c-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="9a85c-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="9a85c-121">Marca de propriedade que identifica a propriedade de cadeia de caracteres a ser verificada quanto à sequência de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a85c-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="9a85c-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="9a85c-122">**lpProp**</span></span>
  
> <span data-ttu-id="9a85c-123">Ponteiro para uma estrutura de valor de propriedade que contém o valor da cadeia de caracteres a ser usado como a sequência de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9a85c-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a85c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a85c-124">Remarks</span></span>

<span data-ttu-id="9a85c-125">Há duas marcas de propriedade em uma estrutura **SContentRestriction** : uma no membro **ulPropTag** e a outra no membro **ulPropTag** da estrutura **SPropValue** apontada por **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="9a85c-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="9a85c-126">Em ambas as marcas, MAPI requer apenas o campo tipo de propriedade e ignora o campo identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9a85c-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="9a85c-127">No enTanto, os dois tipos de propriedade devem coincidir, ou o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para imApitable [:: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="9a85c-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="9a85c-128">Os valores FL_FULLSTRING, FL_PREFIX e FL_SUBSTRING são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="9a85c-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="9a85c-129">Apenas uma delas pode ser definida, e uma delas deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="9a85c-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="9a85c-130">Seus significados são fixos e o provedor deve implementá-los exatamente como definido.</span><span class="sxs-lookup"><span data-stu-id="9a85c-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="9a85c-131">O provedor deve retornar MAPI_E_TOO_COMPLEX se não puder suportar esses valores.</span><span class="sxs-lookup"><span data-stu-id="9a85c-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="9a85c-132">Os valores FL_IGNORECASE, FL_IGNORENONSPACE e FL_LOOSE são independentes.</span><span class="sxs-lookup"><span data-stu-id="9a85c-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="9a85c-133">Qualquer lugar de zero para todos os três podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="9a85c-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="9a85c-134">Suas definições são fornecidas apenas como uma orientação e o provedor é livre para implementar seu significado específico de cada sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9a85c-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="9a85c-135">O provedor não deve retornar nenhuma indicação de erro se não tiver nenhuma implementação de um sinalizador especificado.</span><span class="sxs-lookup"><span data-stu-id="9a85c-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="9a85c-136">O resultado de uma restrição de conteúdo imposta a uma propriedade é indefinido quando a propriedade não existe.</span><span class="sxs-lookup"><span data-stu-id="9a85c-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="9a85c-137">Quando um cliente requer um comportamento bem definido para tal restrição e não tem certeza se a propriedade existe por exemplo, ela não é uma coluna obrigatória de uma tabela que deve criar uma restrição **e** para ingressar na restrição de conteúdo com uma restrição existir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="9a85c-138">Use uma estrutura [SExistRestriction](sexistrestriction.md) para definir a restrição existir e uma estrutura [SAndRestriction](sandrestriction.md) para definir a restrição **e** .</span><span class="sxs-lookup"><span data-stu-id="9a85c-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="9a85c-139">Para obter mais informações sobre a estrutura e as restrições do **SContentRestriction** em geral, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="9a85c-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a85c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a85c-140">See also</span></span>

- [<span data-ttu-id="9a85c-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9a85c-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="9a85c-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9a85c-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="9a85c-143">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9a85c-143">MAPI Structures</span></span>](mapi-structures.md)

