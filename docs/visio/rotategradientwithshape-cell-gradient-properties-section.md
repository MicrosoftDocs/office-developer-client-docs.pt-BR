---
title: Célula RotateGradientWithShape (Seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina se um gradiente do preenchimento gira com a forma em rotação 2D, como um valor booleano.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772734"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="a2b15-103">Célula RotateGradientWithShape (Seção Gradient Properties)</span><span class="sxs-lookup"><span data-stu-id="a2b15-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="a2b15-104">Determina se um gradiente do preenchimento gira com a forma em rotação 2D, como um valor booleano.</span><span class="sxs-lookup"><span data-stu-id="a2b15-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="a2b15-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a2b15-105">**Value**</span></span>|<span data-ttu-id="a2b15-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2b15-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a2b15-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="a2b15-107">TRUE</span></span>  <br/> |<span data-ttu-id="a2b15-108">Gradiente gira com a forma quando a forma for girada ao redor do pino rotação.</span><span class="sxs-lookup"><span data-stu-id="a2b15-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="a2b15-109">O "superior" do gradiente é paralelo com a alça de rotação.</span><span class="sxs-lookup"><span data-stu-id="a2b15-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="a2b15-110">FALSO</span><span class="sxs-lookup"><span data-stu-id="a2b15-110">FALSE</span></span>  <br/> |<span data-ttu-id="a2b15-111">Gradiente não gira com a forma quando a forma for girada ao redor do pino rotação.</span><span class="sxs-lookup"><span data-stu-id="a2b15-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="a2b15-112">O "superior" do gradiente é paralelo à tela de desenho.</span><span class="sxs-lookup"><span data-stu-id="a2b15-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2b15-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2b15-113">Remarks</span></span>

<span data-ttu-id="a2b15-114">Para fazer referência à célula **RotateGradientWithShape** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="a2b15-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2b15-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a2b15-115">Cell name:</span></span>  <br/> | <span data-ttu-id="a2b15-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="a2b15-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="a2b15-117">Para obter uma referência à célula **RotateGradientWithShape** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a2b15-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2b15-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a2b15-118">Section index:</span></span>  <br/> |<span data-ttu-id="a2b15-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2b15-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a2b15-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a2b15-120">Row index:</span></span>  <br/> |<span data-ttu-id="a2b15-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="a2b15-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="a2b15-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a2b15-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a2b15-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="a2b15-123">**visRotateGradientWithShape**</span></span> <br/> |
   

