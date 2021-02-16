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
# <a name="dtbllabel"></a><span data-ttu-id="e9c91-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="e9c91-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="e9c91-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9c91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9c91-105">Descreve um rótulo que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9c91-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9c91-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e9c91-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9c91-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9c91-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e9c91-108">Macro relacionada</span><span class="sxs-lookup"><span data-stu-id="e9c91-108">Related macro</span></span>  <br/> |[<span data-ttu-id="e9c91-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="e9c91-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="e9c91-110">Members</span><span class="sxs-lookup"><span data-stu-id="e9c91-110">Members</span></span>

 <span data-ttu-id="e9c91-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="e9c91-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="e9c91-112">Posição na memória do rótulo de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e9c91-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="e9c91-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e9c91-113">**ulFlags**</span></span>
  
> <span data-ttu-id="e9c91-114">Bitmask de sinalizadores usados para designar o formato do rótulo apontado pelo **membro ulbLpszLabelName.**</span><span class="sxs-lookup"><span data-stu-id="e9c91-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="e9c91-115">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="e9c91-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="e9c91-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e9c91-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e9c91-117">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e9c91-117">The label is in Unicode format.</span></span> <span data-ttu-id="e9c91-118">Se o MAPI_UNICODE sinalizador não estiver definido, o rótulo está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e9c91-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9c91-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9c91-119">Remarks</span></span>

<span data-ttu-id="e9c91-120">Uma **estrutura DTBLLABEL** descreve um texto de controle de rótulo que é exibido com outro tipo de controle para adicionar significado a esse controle.</span><span class="sxs-lookup"><span data-stu-id="e9c91-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="e9c91-121">Por exemplo, a maioria dos controles de edição é posicionada ao lado dos rótulos para informar o usuário sobre o tipo de informação a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="e9c91-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="e9c91-122">Alguns controles, como caixas de grupo e botões de rádio, têm seus próprios rótulos.</span><span class="sxs-lookup"><span data-stu-id="e9c91-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="e9c91-123">O rótulo pode incluir um acelerador do Windows, identificado como o caractere após o esand ( &amp; ).</span><span class="sxs-lookup"><span data-stu-id="e9c91-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="e9c91-124">Pressionar a tecla aceleradora coloca o foco no primeiro controle sem rótulo e sem rótulo após esse rótulo na tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9c91-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="e9c91-125">Não há suporte para rótulos de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="e9c91-125">There is no support for multiline labels.</span></span> <span data-ttu-id="e9c91-126">Mostrar várias linhas requer vários rótulos.</span><span class="sxs-lookup"><span data-stu-id="e9c91-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="e9c91-127">Não é possível usar um rótulo como um controle de edição somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e9c91-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="e9c91-128">A diferença é que um controle de edição pode ser selecionado e copiado, enquanto um rótulo não.</span><span class="sxs-lookup"><span data-stu-id="e9c91-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="e9c91-129">Para uma visão geral das tabelas de exibição, consulte [Tabelas de Exibição.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="e9c91-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e9c91-130">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="e9c91-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9c91-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9c91-131">See also</span></span>



[<span data-ttu-id="e9c91-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e9c91-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e9c91-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e9c91-133">MAPI Structures</span></span>](mapi-structures.md)

