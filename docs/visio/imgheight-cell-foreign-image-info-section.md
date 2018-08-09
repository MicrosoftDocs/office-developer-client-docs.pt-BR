---
title: Célula ImgWidth (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 'Determina a altura da imagem do objeto dentro de sua borda. A fórmula padrão é:'
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772066"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="fe23f-104">Célula ImgHeight (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="fe23f-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="fe23f-p102">Determina a altura da imagem do objeto dentro de sua borda. A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="fe23f-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="fe23f-107">= A altura \* 1</span><span class="sxs-lookup"><span data-stu-id="fe23f-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe23f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe23f-108">Remarks</span></span>

<span data-ttu-id="fe23f-109">Para fazer referência à célula ImgHeight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="fe23f-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe23f-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fe23f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fe23f-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="fe23f-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="fe23f-112">Para fazer referência à célula ImgHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fe23f-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe23f-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fe23f-113">Section index:</span></span>  <br/> |<span data-ttu-id="fe23f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fe23f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fe23f-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="fe23f-115">Row index:</span></span>  <br/> |<span data-ttu-id="fe23f-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="fe23f-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="fe23f-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="fe23f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fe23f-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="fe23f-118">**visFrgnImgHeight**</span></span> <br/> |
   

