---
title: Célula ImgWidth (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: 'Determina a largura da imagem do objeto dentro de sua borda. A fórmula padrão é:'
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772064"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a><span data-ttu-id="a9cda-104">Célula ImgWidth (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="a9cda-104">ImgWidth Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="a9cda-p102">Determina a largura da imagem do objeto dentro de sua borda. A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="a9cda-p102">Determines the width of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="a9cda-107">= A largura \* 1</span><span class="sxs-lookup"><span data-stu-id="a9cda-107">= Width \* 1</span></span>
  
<span data-ttu-id="a9cda-108">Cortar o objeto altera o fator pelo qual a largura é multiplicada.</span><span class="sxs-lookup"><span data-stu-id="a9cda-108">Cropping the object changes the factor by which Width is multiplied.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9cda-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9cda-109">Remarks</span></span>

<span data-ttu-id="a9cda-110">Para fazer referência à célula ImgWidth pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a9cda-110">To get a reference to the ImgWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9cda-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a9cda-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a9cda-112">ImgWidth</span><span class="sxs-lookup"><span data-stu-id="a9cda-112">ImgWidth</span></span>  <br/> |
   
<span data-ttu-id="a9cda-113">Para fazer referência à célula ImgWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a9cda-113">To get a reference to the ImgWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a9cda-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a9cda-114">Section index:</span></span>  <br/> |<span data-ttu-id="a9cda-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9cda-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a9cda-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a9cda-116">Row index:</span></span>  <br/> |<span data-ttu-id="a9cda-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="a9cda-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="a9cda-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a9cda-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a9cda-119">**visFrgnImgWidth**</span><span class="sxs-lookup"><span data-stu-id="a9cda-119">**visFrgnImgWidth**</span></span> <br/> |
   

