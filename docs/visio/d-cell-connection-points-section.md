---
title: Célula D (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771642"
---
# <a name="d-cell-connection-points-section"></a><span data-ttu-id="6d399-103">Célula D (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="6d399-103">D Cell (Connection Points Section)</span></span>

<span data-ttu-id="6d399-104">Uma célula de rascunho que pode ser utilizada para inserir ou testar fórmulas.</span><span class="sxs-lookup"><span data-stu-id="6d399-104">A scratch cell that you can use for entering or testing formulas.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6d399-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d399-105">Remarks</span></span>

<span data-ttu-id="6d399-106">Para acessar a célula D, do mouse em uma linha e clique em **Alterar tipo de linha** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6d399-106">To access the D cell, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  
<span data-ttu-id="6d399-107">Para obter uma referência à célula D pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="6d399-107">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d399-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6d399-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6d399-109">Connections.D [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6d399-109">Connections.D[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6d399-110">Para obter uma referência à célula D pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6d399-110">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d399-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6d399-111">Section index:</span></span>  <br/> |<span data-ttu-id="6d399-112">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="6d399-112">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="6d399-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6d399-113">Row index:</span></span>  <br/> |<span data-ttu-id="6d399-114">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d399-114">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6d399-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6d399-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6d399-116">**visCnnctD**</span><span class="sxs-lookup"><span data-stu-id="6d399-116">**visCnnctD**</span></span> <br/> |
   

