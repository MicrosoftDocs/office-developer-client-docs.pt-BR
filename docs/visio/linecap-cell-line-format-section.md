---
title: Célula LineCap (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indica se as terminações da linha são arredondadas, quadradas ou estendidas.
ms.openlocfilehash: 44de4bff87fd3d121dfce9eec934ec39bc61065a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359315"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="f97de-103">Célula LineCap (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="f97de-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="f97de-104">Indica se as terminações da linha são arredondadas, quadradas ou estendidas.</span><span class="sxs-lookup"><span data-stu-id="f97de-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="f97de-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f97de-105">**Value**</span></span>|<span data-ttu-id="f97de-106">**Estilo do fim de linha**</span><span class="sxs-lookup"><span data-stu-id="f97de-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f97de-107">,0</span><span class="sxs-lookup"><span data-stu-id="f97de-107">0</span></span>  <br/> |<span data-ttu-id="f97de-108">Arredondado</span><span class="sxs-lookup"><span data-stu-id="f97de-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="f97de-109">1</span><span class="sxs-lookup"><span data-stu-id="f97de-109">1</span></span>  <br/> |<span data-ttu-id="f97de-110">Quadrado</span><span class="sxs-lookup"><span data-stu-id="f97de-110">Square</span></span>  <br/> |
|<span data-ttu-id="f97de-111">duas</span><span class="sxs-lookup"><span data-stu-id="f97de-111">2</span></span>  <br/> |<span data-ttu-id="f97de-112">Estendida</span><span class="sxs-lookup"><span data-stu-id="f97de-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f97de-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f97de-113">Remarks</span></span>

<span data-ttu-id="f97de-114">Também é possível definir o valor dessa célula na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**).</span><span class="sxs-lookup"><span data-stu-id="f97de-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="f97de-115">Para obter uma referência para a célula LineCap pelo nome, a partir de outra célula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f97de-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f97de-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f97de-116">Cell name:</span></span>  <br/> |<span data-ttu-id="f97de-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="f97de-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="f97de-118">Para obter uma referência para a célula LineCap a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f97de-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f97de-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f97de-119">Section index:</span></span>  <br/> |<span data-ttu-id="f97de-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f97de-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f97de-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f97de-121">Row index:</span></span>  <br/> |<span data-ttu-id="f97de-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="f97de-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="f97de-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f97de-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f97de-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="f97de-124">**visLineEndCap**</span></span> <br/> |
   

