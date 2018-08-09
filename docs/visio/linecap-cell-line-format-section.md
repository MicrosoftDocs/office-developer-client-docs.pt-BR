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
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772195"
---
# <a name="linecap-cell-line-format-section"></a><span data-ttu-id="a3242-103">Célula LineCap (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="a3242-103">LineCap Cell (Line Format Section)</span></span>

<span data-ttu-id="a3242-104">Indica se as terminações da linha são arredondadas, quadradas ou estendidas.</span><span class="sxs-lookup"><span data-stu-id="a3242-104">Indicates whether a line has rounded, square, or extended line caps.</span></span>
  
|<span data-ttu-id="a3242-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a3242-105">**Value**</span></span>|<span data-ttu-id="a3242-106">**Estilo do fim de linha**</span><span class="sxs-lookup"><span data-stu-id="a3242-106">**Line end style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3242-107">0</span><span class="sxs-lookup"><span data-stu-id="a3242-107">0</span></span>  <br/> |<span data-ttu-id="a3242-108">Arredondado</span><span class="sxs-lookup"><span data-stu-id="a3242-108">Rounded</span></span>  <br/> |
|<span data-ttu-id="a3242-109">1</span><span class="sxs-lookup"><span data-stu-id="a3242-109">1</span></span>  <br/> |<span data-ttu-id="a3242-110">Quadrado</span><span class="sxs-lookup"><span data-stu-id="a3242-110">Square</span></span>  <br/> |
|<span data-ttu-id="a3242-111">2</span><span class="sxs-lookup"><span data-stu-id="a3242-111">2</span></span>  <br/> |<span data-ttu-id="a3242-112">Estendido</span><span class="sxs-lookup"><span data-stu-id="a3242-112">Extended</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3242-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3242-113">Remarks</span></span>

<span data-ttu-id="a3242-114">Também é possível definir o valor dessa célula na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**).</span><span class="sxs-lookup"><span data-stu-id="a3242-114">You can also set the value of this cell in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span>
  
<span data-ttu-id="a3242-115">Para obter uma referência para a célula LineCap pelo nome, a partir de outra célula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a3242-115">To get a reference to the LineCap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3242-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a3242-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a3242-117">LineCap</span><span class="sxs-lookup"><span data-stu-id="a3242-117">LineCap</span></span>  <br/> |
   
<span data-ttu-id="a3242-118">Para obter uma referência para a célula LineCap a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a3242-118">To get a reference to the LineCap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3242-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a3242-119">Section index:</span></span>  <br/> |<span data-ttu-id="a3242-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a3242-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a3242-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a3242-121">Row index:</span></span>  <br/> |<span data-ttu-id="a3242-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="a3242-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="a3242-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a3242-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a3242-124">**visLineEndCap**</span><span class="sxs-lookup"><span data-stu-id="a3242-124">**visLineEndCap**</span></span> <br/> |
   

