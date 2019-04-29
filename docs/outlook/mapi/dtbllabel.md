---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410683"
---
# <a name="dtbllabel"></a><span data-ttu-id="e5555-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="e5555-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="e5555-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5555-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5555-105">Descreve um rótulo que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e5555-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5555-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e5555-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5555-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e5555-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e5555-108">Macro relacionada</span><span class="sxs-lookup"><span data-stu-id="e5555-108">Related macro</span></span>  <br/> |[<span data-ttu-id="e5555-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="e5555-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="e5555-110">Members</span><span class="sxs-lookup"><span data-stu-id="e5555-110">Members</span></span>

 <span data-ttu-id="e5555-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="e5555-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="e5555-112">Posição na memória do rótulo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e5555-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="e5555-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e5555-113">**ulFlags**</span></span>
  
> <span data-ttu-id="e5555-114">Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="e5555-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="e5555-115">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="e5555-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="e5555-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5555-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e5555-117">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e5555-117">The label is in Unicode format.</span></span> <span data-ttu-id="e5555-118">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e5555-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5555-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5555-119">Remarks</span></span>

<span data-ttu-id="e5555-120">Uma estrutura **DTBLLABEL** descreve um texto de controle de rótulo que é exibido com outro tipo de controle para adicionar significado a esse controle.</span><span class="sxs-lookup"><span data-stu-id="e5555-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="e5555-121">Por exemplo, a maioria dos controles de edição são posicionados ao lado de rótulos para informar ao usuário sobre o tipo de informação a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="e5555-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="e5555-122">Alguns controles, como caixas de grupo e botões de opção, mantêm seus próprios rótulos.</span><span class="sxs-lookup"><span data-stu-id="e5555-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="e5555-123">O rótulo pode incluir um acelerador do Windows, identificado como o caractere após o&amp;e comercial ().</span><span class="sxs-lookup"><span data-stu-id="e5555-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="e5555-124">Pressionar a tecla aceleradora coloca o foco no primeiro controle não rótulo, sem botão, seguindo este rótulo na tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e5555-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="e5555-125">Não há suporte para rótulos de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="e5555-125">There is no support for multiline labels.</span></span> <span data-ttu-id="e5555-126">Mostrar várias linhas requer vários rótulos.</span><span class="sxs-lookup"><span data-stu-id="e5555-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="e5555-127">Não é possível usar um rótulo como um controle de edição somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e5555-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="e5555-128">A diferença é que um controle de edição pode ser selecionado e copiado, enquanto um rótulo não pode.</span><span class="sxs-lookup"><span data-stu-id="e5555-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="e5555-129">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e5555-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e5555-130">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e5555-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5555-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5555-131">See also</span></span>



[<span data-ttu-id="e5555-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e5555-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e5555-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e5555-133">MAPI Structures</span></span>](mapi-structures.md)

