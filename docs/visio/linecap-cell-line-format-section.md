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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425194"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="af055-103">Célula LineCap (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="af055-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="af055-104">Indica se as terminações da linha são arredondadas, quadradas ou estendidas.</span><span class="sxs-lookup"><span data-stu-id="af055-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="af055-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="af055-105">**Value**</span></span>|<span data-ttu-id="af055-106">**Estilo do fim de linha**</span><span class="sxs-lookup"><span data-stu-id="af055-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af055-107">0</span><span class="sxs-lookup"><span data-stu-id="af055-107">0</span></span>  <br/> |<span data-ttu-id="af055-108">Arredondado</span><span class="sxs-lookup"><span data-stu-id="af055-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="af055-109">1 </span><span class="sxs-lookup"><span data-stu-id="af055-109">1</span></span>  <br/> |<span data-ttu-id="af055-110">Quadrado</span><span class="sxs-lookup"><span data-stu-id="af055-110">Square</span></span>  <br/> |
|<span data-ttu-id="af055-111">2 </span><span class="sxs-lookup"><span data-stu-id="af055-111">2</span></span>  <br/> |<span data-ttu-id="af055-112">Estendida</span><span class="sxs-lookup"><span data-stu-id="af055-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af055-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="af055-113">Remarks</span></span>

<span data-ttu-id="af055-114">Também é possível definir o valor dessa célula na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**).</span><span class="sxs-lookup"><span data-stu-id="af055-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="af055-115">Para obter uma referência para a célula LineCap pelo nome, a partir de outra célula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="af055-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af055-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="af055-116">Cell name:</span></span>  <br/> |<span data-ttu-id="af055-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="af055-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="af055-118">Para obter uma referência para a célula LineCap a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="af055-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af055-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="af055-119">Section index:</span></span>  <br/> |<span data-ttu-id="af055-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="af055-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="af055-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="af055-121">Row index:</span></span>  <br/> |<span data-ttu-id="af055-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="af055-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="af055-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="af055-123">Cell index:</span></span>  <br/> |<span data-ttu-id="af055-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="af055-124">**visLineEndCap**</span></span> <br/> |
   

