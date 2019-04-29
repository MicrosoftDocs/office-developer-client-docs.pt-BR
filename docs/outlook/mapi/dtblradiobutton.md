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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434596"
---
# <a name="dtblradiobutton"></a><span data-ttu-id="b62b8-103">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="b62b8-103">DTBLRADIOBUTTON</span></span>

  
  
<span data-ttu-id="b62b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b62b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b62b8-105">Descreve um botão de opção que fará parte de um grupo de botões de opção.</span><span class="sxs-lookup"><span data-stu-id="b62b8-105">Describes one radio button that will be part of a radio button group.</span></span> <span data-ttu-id="b62b8-106">O grupo de botões de opção será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="b62b8-106">The radio button group will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b62b8-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b62b8-107">Header file:</span></span>  <br/> |<span data-ttu-id="b62b8-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b62b8-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="b62b8-109">Members</span><span class="sxs-lookup"><span data-stu-id="b62b8-109">Members</span></span>

 <span data-ttu-id="b62b8-110">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="b62b8-110">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="b62b8-111">Posição na memória do rótulo de cadeia de caracteres do botão de opção.</span><span class="sxs-lookup"><span data-stu-id="b62b8-111">Position in memory of the character string label for the radio button.</span></span>
    
 <span data-ttu-id="b62b8-112">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b62b8-112">**ulFlags**</span></span>
  
> <span data-ttu-id="b62b8-113">Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="b62b8-113">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="b62b8-114">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="b62b8-114">The following flag can be set:</span></span> 
    
<span data-ttu-id="b62b8-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b62b8-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b62b8-116">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b62b8-116">The label is in Unicode format.</span></span> <span data-ttu-id="b62b8-117">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b62b8-117">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="b62b8-118">**ulcButtons**</span><span class="sxs-lookup"><span data-stu-id="b62b8-118">**ulcButtons**</span></span>
  
> <span data-ttu-id="b62b8-119">Contagem de botões no grupo de botões de opção.</span><span class="sxs-lookup"><span data-stu-id="b62b8-119">Count of buttons in the radio button group.</span></span> <span data-ttu-id="b62b8-120">As estruturas **DTBLRADIOBUTTON** para os outros botões no grupo devem estar contidas em linhas sucessivas da tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="b62b8-120">The **DTBLRADIOBUTTON** structures for the other buttons in the group must be contained in successive rows of the display table.</span></span> <span data-ttu-id="b62b8-121">Cada uma dessas linhas deve conter o mesmo valor para o membro **ulcButtons** .</span><span class="sxs-lookup"><span data-stu-id="b62b8-121">Each of these rows should contain the same value for the **ulcButtons** member.</span></span> 
    
 <span data-ttu-id="b62b8-122">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="b62b8-122">**ulPropTag**</span></span>
  
> <span data-ttu-id="b62b8-123">Marca de propriedade de uma propriedade do tipo PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="b62b8-123">Property tag for a property of type PT_LONG.</span></span> <span data-ttu-id="b62b8-124">A seleção inicial no grupo de botões de opção é baseada no valor inicial dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b62b8-124">The initial selection in the radio button group is based on the initial value of this property.</span></span> <span data-ttu-id="b62b8-125">Cada botão no grupo deve ter **ulPropTag** definido para a mesma propriedade.</span><span class="sxs-lookup"><span data-stu-id="b62b8-125">Each button in the group must have **ulPropTag** set to the same property.</span></span> 
    
 <span data-ttu-id="b62b8-126">**lReturnValue**</span><span class="sxs-lookup"><span data-stu-id="b62b8-126">**lReturnValue**</span></span>
  
> <span data-ttu-id="b62b8-127">Número exclusivo que identifica o botão selecionado.</span><span class="sxs-lookup"><span data-stu-id="b62b8-127">Unique number that identifies the selected button.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b62b8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b62b8-128">Remarks</span></span>

<span data-ttu-id="b62b8-129">Uma estrutura **DTBLRADIOBUTTON** descreve um botão de opção um controle de botão que é associado a um grupo de botões.</span><span class="sxs-lookup"><span data-stu-id="b62b8-129">A **DTBLRADIOBUTTON** structure describes a radio button a button control that is associated with a group of buttons.</span></span> <span data-ttu-id="b62b8-130">Somente um botão no grupo pode ser verificado; definir um botão faz com que os outros botões do grupo sejam desdefinidos.</span><span class="sxs-lookup"><span data-stu-id="b62b8-130">Only one button in the group can be checked; setting one button causes the other buttons in the group to be unset.</span></span> 
  
<span data-ttu-id="b62b8-131">A contagem de botões é o número de botões de opção no grupo.</span><span class="sxs-lookup"><span data-stu-id="b62b8-131">The button count is the number of radio buttons in the group.</span></span> <span data-ttu-id="b62b8-132">As estruturas dos outros botões de opção no grupo devem estar nas linhas subsequentes na tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="b62b8-132">The structures for the other radio buttons in the group must be in subsequent rows in the display table.</span></span> <span data-ttu-id="b62b8-133">Cada uma dessas estruturas deve ter o mesmo valor para a contagem de botão.</span><span class="sxs-lookup"><span data-stu-id="b62b8-133">Each of these structures should have the same value for its button count.</span></span>
  
<span data-ttu-id="b62b8-134">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b62b8-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b62b8-135">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b62b8-135">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b62b8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b62b8-136">See also</span></span>



[<span data-ttu-id="b62b8-137">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="b62b8-137">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="b62b8-138">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b62b8-138">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="b62b8-139">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="b62b8-139">SizedDtblButton</span></span>](sizeddtblbutton.md)


[<span data-ttu-id="b62b8-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b62b8-140">MAPI Structures</span></span>](mapi-structures.md)

