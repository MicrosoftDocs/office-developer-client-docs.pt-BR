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
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344930"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="4e4ff-104">Célula ImgWidth (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="4e4ff-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="4e4ff-105">Determina a altura da imagem do objeto dentro de sua borda.</span><span class="sxs-lookup"><span data-stu-id="4e4ff-105">Determines the height of the object's image within its border.</span></span> <span data-ttu-id="4e4ff-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-106">The default formula is:</span></span>
  
<span data-ttu-id="4e4ff-107">= Altura \* 1</span><span class="sxs-lookup"><span data-stu-id="4e4ff-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e4ff-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e4ff-108">Remarks</span></span>

<span data-ttu-id="4e4ff-109">Para fazer referência à célula ImgHeight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e4ff-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-110">Cell name:</span></span>  <br/> | <span data-ttu-id="4e4ff-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="4e4ff-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="4e4ff-112">Para fazer referência à célula ImgHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e4ff-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-113">Section index:</span></span>  <br/> |<span data-ttu-id="4e4ff-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4e4ff-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4e4ff-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-115">Row index:</span></span>  <br/> |<span data-ttu-id="4e4ff-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="4e4ff-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="4e4ff-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4e4ff-117">Cell index:</span></span>  <br/> |<span data-ttu-id="4e4ff-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="4e4ff-118">**visFrgnImgHeight**</span></span> <br/> |
   

