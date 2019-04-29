---
title: DTBLCOMBOBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCOMBOBOX
api_type:
- COM
ms.assetid: 73b68614-6aca-4669-b879-5631c5d6483c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5256efbff734d4555ac263dd330e3349c789cd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406973"
---
# <a name="dtblcombobox"></a><span data-ttu-id="c6d2c-103">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="c6d2c-103">DTBLCOMBOBOX</span></span>

  
  
<span data-ttu-id="c6d2c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6d2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6d2c-105">Descreve um controle de caixa de combinação que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-105">Describes a combo box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6d2c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c6d2c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6d2c-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c6d2c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c6d2c-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="c6d2c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="c6d2c-109">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="c6d2c-109">SizedDtblComboBox</span></span>](sizeddtblcombobox.md) <br/> |
   
```cpp
typedef struct _DTBLCOMBOBOX
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPRPropertyName;
  ULONG ulPRTableName;
} DTBLCOMBOBOX, FAR *LPDTBLCOMBOBOX;

```

## <a name="members"></a><span data-ttu-id="c6d2c-110">Members</span><span class="sxs-lookup"><span data-stu-id="c6d2c-110">Members</span></span>

 <span data-ttu-id="c6d2c-111">**ulbLpszCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-111">**ulbLpszCharsAllowed**</span></span>
  
> <span data-ttu-id="c6d2c-112">Um offset do início da estrutura **DTBLCOMBOBOX** para um filtro de cadeia de caracteres que descreve as restrições, se houver, para os caracteres que podem ser inseridos no controle de edição da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-112">An offset from the start of the **DTBLCOMBOBOX** structure to a character string filter that describes restrictions, if any, to the characters that can be entered into the combo box's edit control.</span></span> <span data-ttu-id="c6d2c-113">O filtro não é interpretado como uma expressão regular e o mesmo filtro é aplicado a todos os caracteres inseridos.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-113">The filter is not interpreted as a regular expression and the same filter is applied to every character entered.</span></span> <span data-ttu-id="c6d2c-114">O formato do filtro é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c6d2c-114">The format of the filter is as follows:</span></span> 
    
|<span data-ttu-id="c6d2c-115">**Caractere**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-115">**Character**</span></span>|<span data-ttu-id="c6d2c-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-116">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> |<span data-ttu-id="c6d2c-117">Qualquer caractere é permitido (por exemplo, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-117">Any character is allowed (for example,  `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="c6d2c-118">Define um conjunto de caracteres (por exemplo, `"[0123456789]"`).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-118">Defines a set of characters (for example,  `"[0123456789]"`).</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="c6d2c-119">Indica um intervalo de caracteres (por exemplo, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-119">Indicates a range of characters (for example,  `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="c6d2c-120">Indica que esses caracteres não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-120">Indicates that these characters are not allowed.</span></span> <span data-ttu-id="c6d2c-121">(por exemplo, `"[~0-9]"`).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-121">(for example,  `"[~0-9]"`).</span></span>  <br/> |
| `\` <br/> |<span data-ttu-id="c6d2c-122">Usado para citar qualquer um dos símbolos anteriores (por exemplo, `"[\-\\\[\]]"` os caracteres significa \, -, [e] são permitidos).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-122">Used to quote any of the previous symbols (for example,  `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
 <span data-ttu-id="c6d2c-123">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-123">**ulFlags**</span></span>
  
> <span data-ttu-id="c6d2c-124">Bitmask dos sinalizadores usados para designar o formato do filtro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-124">Bitmask of flags used to designate the format of the character string filter.</span></span> <span data-ttu-id="c6d2c-125">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="c6d2c-125">The following flag can be set:</span></span>
    
<span data-ttu-id="c6d2c-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6d2c-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c6d2c-127">O filtro está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-127">The filter is in Unicode format.</span></span> <span data-ttu-id="c6d2c-128">Se o sinalizador MAPI_UNICODE não estiver definido, o filtro estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-128">If the MAPI_UNICODE flag is not set, the filter is in ANSI format.</span></span>
    
 <span data-ttu-id="c6d2c-129">**ulNumCharsAllowed**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-129">**ulNumCharsAllowed**</span></span>
  
> <span data-ttu-id="c6d2c-130">Número máximo de caracteres que podem ser inseridos na caixa de texto da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-130">Maximum number of characters that can be entered in the combo box's text box.</span></span>
    
 <span data-ttu-id="c6d2c-131">**ulPRPropertyName**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-131">**ulPRPropertyName**</span></span>
  
> <span data-ttu-id="c6d2c-132">Marca de propriedade de uma propriedade do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-132">Property tag for a property of type PT_TSTRING.</span></span> 
    
 <span data-ttu-id="c6d2c-133">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-133">**ulPRTableName**</span></span>
  
> <span data-ttu-id="c6d2c-134">Marca de propriedade de uma propriedade do tipo PT_OBJECT na qual \*\*\*\* uma interface IMAPITable pode ser aberta usando uma chamada **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="c6d2c-134">Property tag for a property of type PT_OBJECT on which an **IMAPITable** interface can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="c6d2c-135">A tabela deve ter uma coluna com uma propriedade que é do mesmo tipo que a propriedade identificada pelo membro **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="c6d2c-135">The table must have one column with a property that is the same type as the property identified by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="c6d2c-136">As linhas da tabela são usadas para preencher a lista.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-136">The rows of the table are used to populate the list.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c6d2c-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6d2c-137">Remarks</span></span>

<span data-ttu-id="c6d2c-138">Uma estrutura **DTBLCOMBOBOX** descreve uma caixa de combinação de um controle que consiste em uma lista e um campo de seleção.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-138">A **DTBLCOMBOBOX** structure describes a combo box a control that consists of a list and a selection field.</span></span> <span data-ttu-id="c6d2c-139">A lista apresenta as informações que um usuário pode selecionar e o campo de seleção exibe a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-139">The list presents the information from which a user can select, and the selection field displays the current selection.</span></span> <span data-ttu-id="c6d2c-140">O campo de seleção é um controle de edição que também pode ser usado para inserir texto que ainda não está na lista.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-140">The selection field is an edit control that can also be used to enter text not already in the list.</span></span> 
  
<span data-ttu-id="c6d2c-141">Os dois membros da marca de propriedade trabalham juntos para coordenar a exibição da lista com o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-141">The two property tag members work together to coordinate the list display with the edit control.</span></span> <span data-ttu-id="c6d2c-142">Quando o MAPI exibe primeiro a caixa de combinação, ele \*\*\*\* chama o método OpenProperty da implementação do **IMAPIProp** associada à tabela de exibição para recuperar a tabela representada pelo membro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="c6d2c-142">When MAPI first displays the combo box, it calls the **OpenProperty** method of the **IMAPIProp** implementation that is associated with the display table to retrieve the table represented by the **ulPRTableName** member.</span></span> <span data-ttu-id="c6d2c-143">Esta tabela tem uma coluna que contém valores para a propriedade representada pelo membro **ulPRPropertyName** .</span><span class="sxs-lookup"><span data-stu-id="c6d2c-143">This table has one column a column that contains values for the property represented by the **ulPRPropertyName** member.</span></span> <span data-ttu-id="c6d2c-144">Portanto, essa coluna deve ser do mesmo tipo que a propriedade **ulPRPropertyName** e ambas as colunas devem ser cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-144">Therefore, this column must be of the same type as the **ulPRPropertyName** property and both columns must be character strings.</span></span> 
  
<span data-ttu-id="c6d2c-145">Os valores da coluna são exibidos na seção lista da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-145">The values for the column are displayed in the list section of the combo box.</span></span> <span data-ttu-id="c6d2c-146">Portanto, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não é uma marca de propriedade válida para **ulPRPropertyName**.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-146">Therefore, **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) is not a valid property tag for **ulPRPropertyName**.</span></span> <span data-ttu-id="c6d2c-147">Quando um usuário seleciona uma das linhas ou insere novos dados na caixa de texto, a propriedade **ulPRPropertyName** é definida como o valor selecionado ou inserido.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-147">When a user either selects one of the rows or enters new data into the text box, the **ulPRPropertyName** property is set to the selected or entered value.</span></span> 
  
<span data-ttu-id="c6d2c-148">Para exibir um valor inicial para o controle de edição, MAPI chama [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar os valores de propriedade da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-148">To display an initial value for the edit control, MAPI calls [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve the property values for the display table.</span></span> <span data-ttu-id="c6d2c-149">Se uma das propriedades recuperadas corresponder à propriedade representada pelo membro **ulPRPropertyName** , seu valor se tornará o valor inicial.</span><span class="sxs-lookup"><span data-stu-id="c6d2c-149">If one of the retrieved properties matches the property represented by the **ulPRPropertyName** member, its value becomes the initial value.</span></span> 
  
<span data-ttu-id="c6d2c-150">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-150">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c6d2c-151">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c6d2c-151">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6d2c-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6d2c-152">See also</span></span>



[<span data-ttu-id="c6d2c-153">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c6d2c-153">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="c6d2c-154">Propriedade canônica PidTagControlType</span><span class="sxs-lookup"><span data-stu-id="c6d2c-154">PidTagControlType Canonical Property</span></span>](pidtagcontroltype-canonical-property.md)


[<span data-ttu-id="c6d2c-155">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6d2c-155">MAPI Structures</span></span>](mapi-structures.md)

