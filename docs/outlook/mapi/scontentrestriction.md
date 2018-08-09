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
ms.openlocfilehash: 34177aee48adad7eecb40836a247705fc22d2a32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770332"
---
# <a name="scontentrestriction"></a><span data-ttu-id="05d6d-103">SContentRestriction</span><span class="sxs-lookup"><span data-stu-id="05d6d-103">SContentRestriction</span></span>
 
<span data-ttu-id="05d6d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05d6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05d6d-105">Descreve uma restrição de conteúdo, que é usada para limitar a um modo de exibição tabela apenas as linhas que incluem uma coluna com a correspondência de uma cadeia de caracteres de pesquisa de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="05d6d-105">Describes a content restriction, which is used to limit a table view to only those rows that include a column with contents matching a search string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05d6d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="05d6d-106">Header file:</span></span>  <br/> |<span data-ttu-id="05d6d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05d6d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a><span data-ttu-id="05d6d-108">Members</span><span class="sxs-lookup"><span data-stu-id="05d6d-108">Members</span></span>

<span data-ttu-id="05d6d-109">**ulFuzzyLevel**</span><span class="sxs-lookup"><span data-stu-id="05d6d-109">**ulFuzzyLevel**</span></span>
  
> <span data-ttu-id="05d6d-110">Configurações de opção definindo o nível de precisão a restrição de conteúdo imponha quando você verificar por uma correspondência.</span><span class="sxs-lookup"><span data-stu-id="05d6d-110">Option settings defining the level of preciseness that the content restriction should enforce when you verify for a match.</span></span>
    
   <span data-ttu-id="05d6d-111">Os **16 bits inferiores** do membro **ulFuzzyLevel** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8 e deve ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="05d6d-111">The **lower 16 bits** of the **ulFuzzyLevel** member apply to properties of type PT_BINARY and PT_STRING8 and must be set to one of the following values:</span></span> 
    
   - <span data-ttu-id="05d6d-112">FL_FULLSTRING: Para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida na propriedade identificada pela **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="05d6d-112">FL_FULLSTRING: To match, the **lpProp** search string must be contained in the property identified by **ulPropTag**.</span></span>
        
   - <span data-ttu-id="05d6d-113">FL_PREFIX: Para corresponder, a cadeia de caracteres de pesquisa **lpProp** deverá aparecer no início da propriedade identificado pela **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="05d6d-113">FL_PREFIX : To match, the **lpProp** search string must appear at the start of the property identified by **ulPropTag**.</span></span> <span data-ttu-id="05d6d-114">As duas cadeias de caracteres devem ser comparadas somente até o comprimento da cadeia de caracteres de pesquisa indicado pelo **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="05d6d-114">The two strings should be compared only up to the length of the search string indicated by **lpProp**.</span></span> 
        
   - <span data-ttu-id="05d6d-115">FL_SUBSTRING: Para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida em qualquer lugar na propriedade identificada pela **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="05d6d-115">FL_SUBSTRING: To match, the **lpProp** search string must be contained anywhere in the property identified by **ulPropTag**.</span></span> 
        
   <span data-ttu-id="05d6d-116">Os **16 bits superiores** do membro **ulFuzzyLevel** aplicam-se apenas às propriedades do tipo PT_STRING8 e pode ser definida para os seguintes valores em qualquer combinação:</span><span class="sxs-lookup"><span data-stu-id="05d6d-116">The **upper 16 bits** of the **ulFuzzyLevel** member apply only to properties of type PT_STRING8 and can be set to the following values in any combination:</span></span> 
        
   - <span data-ttu-id="05d6d-117">FL_IGNORECASE: Comparação deve ser feita sem considerar caso.</span><span class="sxs-lookup"><span data-stu-id="05d6d-117">FL_IGNORECASE: The comparison should be made without considering case.</span></span> 
        
   - <span data-ttu-id="05d6d-118">FL_IGNORENONSPACE: Comparação deve ignorar caracteres de sem espaçamento definido pelo Unicode como sinais diacríticos.</span><span class="sxs-lookup"><span data-stu-id="05d6d-118">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined non-spacing characters such as diacritical marks.</span></span> 
        
   - <span data-ttu-id="05d6d-119">FL_LOOSE: Comparação deve fornecer uma correspondência sempre que possível, ignorando caso e caracteres sem espaçamento.</span><span class="sxs-lookup"><span data-stu-id="05d6d-119">FL_LOOSE: The comparison should give you a match whenever possible, ignoring case and non-spacing characters.</span></span> 
    
<span data-ttu-id="05d6d-120">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="05d6d-120">**ulPropTag**</span></span>
  
> <span data-ttu-id="05d6d-121">Marca de propriedade que identifica a propriedade de cadeia de caracteres a ser verificado para ocorrência da cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="05d6d-121">Property tag identifying the string property to be checked for occurrence of the search string.</span></span> 
    
<span data-ttu-id="05d6d-122">**lpProp**</span><span class="sxs-lookup"><span data-stu-id="05d6d-122">**lpProp**</span></span>
  
> <span data-ttu-id="05d6d-123">Ponteiro para uma estrutura de valor de propriedade que contém o valor de cadeia de caracteres a ser usado como a cadeia de caracteres de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="05d6d-123">Pointer to a property value structure that contains the string value to use as the search string.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05d6d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="05d6d-124">Remarks</span></span>

<span data-ttu-id="05d6d-125">Há duas marcas de propriedade em uma estrutura de **SContentRestriction** : um membro do **ulPropTag** e o outro no membro **ulPropTag** da estrutura **SPropValue** apontado pela **lpProp**.</span><span class="sxs-lookup"><span data-stu-id="05d6d-125">There are two property tags in an **SContentRestriction** structure: one in the **ulPropTag** member and the other in the **ulPropTag** member of the **SPropValue** structure pointed to by **lpProp**.</span></span> <span data-ttu-id="05d6d-126">Em ambas as marcas, MAPI exige apenas o campo de tipo de propriedade e ignora o campo do identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="05d6d-126">In both tags, MAPI requires only the property type field and ignores the property identifier field.</span></span> <span data-ttu-id="05d6d-127">No entanto, os tipos de dois propriedade devem corresponder, caso contrário, o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md).</span><span class="sxs-lookup"><span data-stu-id="05d6d-127">However, the two property types must match, or else the error value MAPI_E_TOO_COMPLEX is returned when the restriction is used in a call to [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md).</span></span> 
  
<span data-ttu-id="05d6d-128">Os valores FL_FULLSTRING, FL_PREFIX e FL_SUBSTRING são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="05d6d-128">The values FL_FULLSTRING, FL_PREFIX, and FL_SUBSTRING are mutually exclusive.</span></span> <span data-ttu-id="05d6d-129">Apenas um deles pode ser definido e um deles deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="05d6d-129">Only one of them can be set, and one of them must be set.</span></span> <span data-ttu-id="05d6d-130">Seus significados corrigidos e o provedor deve implementá-los exatamente conforme definido.</span><span class="sxs-lookup"><span data-stu-id="05d6d-130">Their meanings are fixed, and the provider must implement them exactly as defined.</span></span> <span data-ttu-id="05d6d-131">O provedor deve retornar MAPI_E_TOO_COMPLEX se não for possível dar suporte a esses valores.</span><span class="sxs-lookup"><span data-stu-id="05d6d-131">The provider should return MAPI_E_TOO_COMPLEX if it is unable to support these values.</span></span> 
  
<span data-ttu-id="05d6d-132">Os valores FL_IGNORECASE, FL_IGNORENONSPACE e FL_LOOSE são independentes.</span><span class="sxs-lookup"><span data-stu-id="05d6d-132">The values FL_IGNORECASE, FL_IGNORENONSPACE, and FL_LOOSE are independent.</span></span> <span data-ttu-id="05d6d-133">Em qualquer lugar do zero para todos os três deles pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="05d6d-133">Anywhere from zero to all three of them can be set.</span></span> <span data-ttu-id="05d6d-134">Suas definições são fornecidas como uma diretriz apenas e o provedor é livre para implementar seu próprio significado específico de cada sinalizador.</span><span class="sxs-lookup"><span data-stu-id="05d6d-134">Their definitions are provided as a guideline only, and the provider is free to implement its own specific meaning of each flag.</span></span> <span data-ttu-id="05d6d-135">O provedor não deve retornar qualquer indicação de erro, se ele tiver nenhuma implementação de um sinalizador especificado.</span><span class="sxs-lookup"><span data-stu-id="05d6d-135">The provider should not return any error indication if it has no implementation of a specified flag.</span></span> 
  
<span data-ttu-id="05d6d-136">O resultado de uma restrição imposta em relação a uma propriedade de conteúdo é indefinido quando a propriedade não existe.</span><span class="sxs-lookup"><span data-stu-id="05d6d-136">The result of a content restriction imposed against a property is undefined when the property does not exist.</span></span> <span data-ttu-id="05d6d-137">Quando um cliente exige comportamento bem definido para uma restrição tal e não é certeza se a propriedade existe por exemplo, não é uma coluna obrigatória de uma tabela, ele deve criar uma restrição de **e** para ingressar a restrição de conteúdo com uma restrição existe.</span><span class="sxs-lookup"><span data-stu-id="05d6d-137">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists for example, it is not a required column of a table it should create an **AND** restriction to join the content restriction with an exist restriction.</span></span> <span data-ttu-id="05d6d-138">Use uma estrutura de [SExistRestriction](sexistrestriction.md) para definir a restrição existe e uma estrutura de [SAndRestriction](sandrestriction.md) para definir a restrição **AND** .</span><span class="sxs-lookup"><span data-stu-id="05d6d-138">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="05d6d-139">Para obter mais informações sobre a estrutura de **SContentRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="05d6d-139">For more information about the **SContentRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05d6d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="05d6d-140">See also</span></span>

- [<span data-ttu-id="05d6d-141">SPropValue</span><span class="sxs-lookup"><span data-stu-id="05d6d-141">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="05d6d-142">SRestriction</span><span class="sxs-lookup"><span data-stu-id="05d6d-142">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="05d6d-143">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="05d6d-143">MAPI Structures</span></span>](mapi-structures.md)

