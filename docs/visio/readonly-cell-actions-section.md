---
title: Célula ReadOnly (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Controla se a ação em um menu de marca de ação ou atalho é somente leitura ou não.
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434232"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="02775-103">Célula ReadOnly (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="02775-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="02775-104">Controla se a ação em um menu de atalho ou de marca de ação é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="02775-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="02775-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="02775-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="02775-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="02775-106">**Value**</span></span>|<span data-ttu-id="02775-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02775-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02775-108">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="02775-108">TRUE</span></span>  <br/> |<span data-ttu-id="02775-109">A ação é exibida no menu, mas é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="02775-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="02775-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="02775-110">FALSE</span></span>  <br/> |<span data-ttu-id="02775-111">A ação é exibida no menu e pode ser selecionada (padrão).</span><span class="sxs-lookup"><span data-stu-id="02775-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02775-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="02775-112">Remarks</span></span>

<span data-ttu-id="02775-113">Quando uma ação é somente leitura, ela é exibida no menu de atalho ou de marca de ação, mas você não pode selecioná-la.</span><span class="sxs-lookup"><span data-stu-id="02775-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="02775-114">Ela não fica esmaecida, é exibida em fundo colorido, como um rótulo.</span><span class="sxs-lookup"><span data-stu-id="02775-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="02775-115">Para que o item de menu seja exibido esmaecido, use a célula Disabled.</span><span class="sxs-lookup"><span data-stu-id="02775-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="02775-116">Para obter uma referência para a célula ReadOnly pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="02775-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02775-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="02775-117">Cell name:</span></span>  <br/> |<span data-ttu-id="02775-118">Ações.</span><span class="sxs-lookup"><span data-stu-id="02775-118">Actions.</span></span> <span data-ttu-id="02775-119">*nome*  . Ações readOnlywhere.</span><span class="sxs-lookup"><span data-stu-id="02775-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="02775-120">*nome*  é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="02775-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="02775-121">Para obter uma referência para a célula ReadOnly pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="02775-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02775-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="02775-122">Section index:</span></span>  <br/> |<span data-ttu-id="02775-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="02775-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="02775-124">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="02775-124">Row index:</span></span>  <br/> |<span data-ttu-id="02775-125">**visRowAction**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="02775-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="02775-126">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="02775-126">Cell index:</span></span>  <br/> |<span data-ttu-id="02775-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="02775-127">**visActionReadOnly**</span></span> <br/> |
   

