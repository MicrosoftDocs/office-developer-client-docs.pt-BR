---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: dee12ba9da83d2167afe13d00270a900bf0d73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766481"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="21d54-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="21d54-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="21d54-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="21d54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="21d54-105">Descreve um botão de opção que farão parte de um grupo de botão de opção.</span><span class="sxs-lookup"><span data-stu-id="21d54-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="21d54-106">O grupo de botão de opção será usado em uma caixa de diálogo que é construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="21d54-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21d54-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="21d54-107">Header file:</span></span>  <br/> |<span data-ttu-id="21d54-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21d54-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a><span data-ttu-id="21d54-109">Membros</span><span class="sxs-lookup"><span data-stu-id="21d54-109">Members</span></span>

 <span data-ttu-id="21d54-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="21d54-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="21d54-111">Posição na memória do rótulo de cadeia de caracteres de caractere para o botão de opção.</span><span class="sxs-lookup"><span data-stu-id="21d54-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="21d54-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="21d54-112">**ulFlags**</span></span>
  
> <span data-ttu-id="21d54-113">Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="21d54-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="21d54-114">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="21d54-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="21d54-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="21d54-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="21d54-116">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="21d54-116">The label is in Unicode format.</span></span> <span data-ttu-id="21d54-117">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="21d54-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="21d54-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="21d54-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="21d54-119">Contagem de botões do grupo de botão de rádio.</span><span class="sxs-lookup"><span data-stu-id="21d54-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="21d54-120">As estruturas de **DTBLRADIOBUTTON** para os outros botões no grupo devem estar contidas em sucessivas linhas da tabela exibição.</span><span class="sxs-lookup"><span data-stu-id="21d54-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="21d54-121">Cada um nessas linhas deve conter o mesmo valor para o membro **ulcButtons** .</span><span class="sxs-lookup"><span data-stu-id="21d54-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="21d54-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="21d54-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="21d54-123">Marca de propriedade para uma propriedade do tipo PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="21d54-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="21d54-124">A seleção inicial no grupo de botões de rádio baseia-se no valor inicial dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="21d54-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="21d54-125">Cada botão do grupo deve ter **ulPropTag** definido para a mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="21d54-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="21d54-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="21d54-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="21d54-127">Número exclusivo que identifica o botão selecionado.</span><span class="sxs-lookup"><span data-stu-id="21d54-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21d54-128">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="21d54-128">Remarks</span></span>

<span data-ttu-id="21d54-129">Uma estrutura **DTBLRADIOBUTTON** descreve um botão de opção de um controle de botão que está associado um grupo de botões.</span><span class="sxs-lookup"><span data-stu-id="21d54-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="21d54-130">Somente um botão do grupo pode ser verificado; a definição de um botão faz com que os outros botões no grupo a ser desfeito.</span><span class="sxs-lookup"><span data-stu-id="21d54-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="21d54-131">A contagem de botão é o número de botões de opção no grupo.</span><span class="sxs-lookup"><span data-stu-id="21d54-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="21d54-132">As estruturas para os outros botões de opção no grupo devem estar no subsequentes linhas da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="21d54-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="21d54-133">Cada uma dessas estruturas deve ter o mesmo valor para sua contagem de botão.</span><span class="sxs-lookup"><span data-stu-id="21d54-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="21d54-134">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="21d54-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="21d54-135">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="21d54-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21d54-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="21d54-136">See also</span></span>



[<span data-ttu-id="21d54-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="21d54-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="21d54-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="21d54-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="21d54-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="21d54-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="21d54-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="21d54-140">MAPI Structures</span></span>](mapi-structures.md)

