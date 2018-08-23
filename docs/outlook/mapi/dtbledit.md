---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eefd0c62314a35c4c6c956b8d4a4d92d5746d1c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590460"
---
# <a name="dtbledit"></a><span data-ttu-id="05a45-103">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="05a45-103">DTBLEDIT</span></span>

  
  
<span data-ttu-id="05a45-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05a45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05a45-105">Descreve um controle de edição que será usado em uma caixa de diálogo construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="05a45-105">Describes an edit control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05a45-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="05a45-106">Header file:</span></span>  <br/> |<span data-ttu-id="05a45-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05a45-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="05a45-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="05a45-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="05a45-109">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="05a45-109">SizedDtblEdit</span></span>](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a><span data-ttu-id="05a45-110">Members</span><span class="sxs-lookup"><span data-stu-id="05a45-110">Members</span></span>

 <span data-ttu-id="05a45-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="05a45-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="05a45-112">Deslocamento desde o início da estrutura **DTBLEDIT** para um filtro de sequência de caracteres que descreve restrições, se houver, com os caracteres que podem ser inseridos em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="05a45-112">An offset from the start of the **DTBLEDIT** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the edit control.</span></span> <span data-ttu-id="05a45-113">O filtro não será interpretado como uma expressão regular e o mesmo filtro é aplicado a cada caractere inserido.</span><span class="sxs-lookup"><span data-stu-id="05a45-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="05a45-114">O formato do filtro é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="05a45-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="05a45-115">**Caractere**</span><span class="sxs-lookup"><span data-stu-id="05a45-115">**Character**</span></span>|<span data-ttu-id="05a45-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="05a45-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="05a45-117">Qualquer caractere é permitido (por exemplo, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="05a45-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="05a45-118">Define um conjunto de caracteres (por exemplo, `"[0123456789]".`)</span><span class="sxs-lookup"><span data-stu-id="05a45-118">Defines a set of characters (for example,  `"[0123456789]".`)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="05a45-119">Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="05a45-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="05a45-120">Indica que esses caracteres não são permitidos (por exemplo, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="05a45-120">Indicates that these characters are not allowed (for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="05a45-121">Usado para quote qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` significa-, \, [, e] caracteres são permitidos).</span><span class="sxs-lookup"><span data-stu-id="05a45-121">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="05a45-122">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="05a45-122">**ulFlags**</span></span>
  
> <span data-ttu-id="05a45-123">Bitmask dos sinalizadores usado para designar o formato do filtro caractere.</span><span class="sxs-lookup"><span data-stu-id="05a45-123">Bitmask of flags used to designate the format of the character filter.</span></span> <span data-ttu-id="05a45-124">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="05a45-124">The following flag can be set:</span></span>
    
<span data-ttu-id="05a45-125">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05a45-125">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="05a45-126">O filtro está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="05a45-126">The filter is in Unicode format.</span></span> <span data-ttu-id="05a45-127">Se o sinalizador MAPI_UNICODE não estiver definido, o filtro está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="05a45-127">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="05a45-128">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="05a45-128">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="05a45-129">Número máximo de caracteres que o usuário pode digitar na caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="05a45-129">Maximum number of characters that the user can type into the text box.</span></span>
    
 <span data-ttu-id="05a45-130">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="05a45-130">**ulPropTag**</span></span>
  
> <span data-ttu-id="05a45-131">Marca de propriedade para uma propriedade do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="05a45-131">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="05a45-132">O membro **ulPropTag** identifica a propriedade de cadeia de caracteres cujos dados são exibidos e editados no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="05a45-132">The **ulPropTag** member identifies the string property whose data is displayed and edited in the edit control.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="05a45-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="05a45-133">Remarks</span></span>

<span data-ttu-id="05a45-134">Uma estrutura **DTBLEDIT** descreve um controle de edição de uma área em uma caixa de diálogo que contém informações alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="05a45-134">A **DTBLEDIT** structure describes an edit control an area on a dialog box that contains alphanumeric information.</span></span> <span data-ttu-id="05a45-135">Quase todas as caixas de diálogo possuem o controle de edição de pelo menos um.</span><span class="sxs-lookup"><span data-stu-id="05a45-135">Almost all dialog boxes have at least one edit control.</span></span> <span data-ttu-id="05a45-136">Controles de edição podem ser modificável por um usuário ou somente leitura.</span><span class="sxs-lookup"><span data-stu-id="05a45-136">Edit controls can be modifiable by a user or read-only.</span></span> 
  
<span data-ttu-id="05a45-137">Controles de edição também podem ser único linha ou multiline.</span><span class="sxs-lookup"><span data-stu-id="05a45-137">Edit controls can also be single line or multiline.</span></span> <span data-ttu-id="05a45-138">Controles de edição de várias linhas geralmente têm uma barra de rolagem associada a eles.</span><span class="sxs-lookup"><span data-stu-id="05a45-138">Multiline edit controls typically have a scroll bar associated with them.</span></span> 
  
<span data-ttu-id="05a45-139">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="05a45-139">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="05a45-140">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="05a45-140">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05a45-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="05a45-141">See also</span></span>



[<span data-ttu-id="05a45-142">DTCTL</span><span class="sxs-lookup"><span data-stu-id="05a45-142">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="05a45-143">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="05a45-143">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="05a45-144">Propriedade canônica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="05a45-144">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="05a45-145">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="05a45-145">MAPI Structures</span></span>](mapi-structures.md)

