---
title: Célula RotateGradientWithShape (seção Gradient Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina se um gradiente de preenchimento gira com uma forma em rotação 2D, como um Boolean.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412216"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="c03b1-103">Célula RotateGradientWithShape (seção Gradient Properties)</span><span class="sxs-lookup"><span data-stu-id="c03b1-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="c03b1-104">Determina se um gradiente de preenchimento gira com uma forma em rotação 2D, como um Boolean.</span><span class="sxs-lookup"><span data-stu-id="c03b1-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="c03b1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c03b1-105">**Value**</span></span>|<span data-ttu-id="c03b1-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c03b1-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c03b1-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c03b1-107">TRUE</span></span>  <br/> |<span data-ttu-id="c03b1-108">O gradiente gira com a forma quando a forma é girada ao redor do pino de rotação.</span><span class="sxs-lookup"><span data-stu-id="c03b1-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="c03b1-109">O "topo" do gradiente é paralelo à alça de rotação.</span><span class="sxs-lookup"><span data-stu-id="c03b1-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="c03b1-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="c03b1-110">FALSE</span></span>  <br/> |<span data-ttu-id="c03b1-111">O gradiente não gira com a forma quando a forma é girada ao redor do pino de rotação.</span><span class="sxs-lookup"><span data-stu-id="c03b1-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="c03b1-112">O "topo" do gradiente é paralelo à tela de desenho.</span><span class="sxs-lookup"><span data-stu-id="c03b1-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c03b1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c03b1-113">Remarks</span></span>

<span data-ttu-id="c03b1-114">Para obter uma referência para a célula **RotateGradientWithShape** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c03b1-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c03b1-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c03b1-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c03b1-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="c03b1-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="c03b1-117">Para obter uma referência para a célula **RotateGradientWithShape** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c03b1-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c03b1-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c03b1-118">Section index:</span></span>  <br/> |<span data-ttu-id="c03b1-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c03b1-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c03b1-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c03b1-120">Row index:</span></span>  <br/> |<span data-ttu-id="c03b1-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="c03b1-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="c03b1-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c03b1-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c03b1-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="c03b1-123">**visRotateGradientWithShape**</span></span> <br/> |
   

