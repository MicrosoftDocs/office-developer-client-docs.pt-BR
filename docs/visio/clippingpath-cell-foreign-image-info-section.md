---
title: Célula ClippingPath (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contém uma referência para a geometria do caminho que uma imagem limitada por.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771500"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="f4f98-103">Célula ClippingPath (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="f4f98-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="f4f98-104">Contém uma referência para a geometria do caminho que uma imagem limitada por.</span><span class="sxs-lookup"><span data-stu-id="f4f98-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4f98-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4f98-105">Remarks</span></span>

<span data-ttu-id="f4f98-106">Se a célula **ClippingPath** aponta para um caminho válido, a imagem é cortada para que a imagem é processada dentro do caminho.</span><span class="sxs-lookup"><span data-stu-id="f4f98-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="f4f98-107">Se a célula **ClippingPath** está vazia ou contém uma entrada inválida, em seguida, a imagem será processada com um clipe retangular, usando os valores de deslocamento e escala.</span><span class="sxs-lookup"><span data-stu-id="f4f98-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f4f98-108">Somente os caminhos definidos por uma seção [Geometry](geometry-section.md) na ShapeSheet da imagem são entradas válidas para a célula **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="f4f98-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="f4f98-109">Referências entre planilhas não podem ser usadas para definir um caminho de recorte de imagem.</span><span class="sxs-lookup"><span data-stu-id="f4f98-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="f4f98-110">Para fazer referência à célula **ClippingPath** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="f4f98-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4f98-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f4f98-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f4f98-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="f4f98-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="f4f98-113">Para obter uma referência à célula **ClippingPath** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f4f98-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4f98-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f4f98-114">Section index:</span></span>  <br/> |<span data-ttu-id="f4f98-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f4f98-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f4f98-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f4f98-116">Row index:</span></span>  <br/> |<span data-ttu-id="f4f98-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="f4f98-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="f4f98-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f4f98-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f4f98-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="f4f98-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="f4f98-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f4f98-120">Example</span></span>

<span data-ttu-id="f4f98-121">Você pode alterar a forma de contorno de uma imagem para uma elipse fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f4f98-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="f4f98-122">Insira a imagem para a tela de desenho.</span><span class="sxs-lookup"><span data-stu-id="f4f98-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="f4f98-123">A imagem do mouse em e selecione **Mostrar ShapeSheet**.</span><span class="sxs-lookup"><span data-stu-id="f4f98-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="f4f98-124">Com o botão direito em qualquer lugar na ShapeSheet e selecione **Inserir seção**.</span><span class="sxs-lookup"><span data-stu-id="f4f98-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="f4f98-125">Na caixa de diálogo **Inserir seção** , selecione a **geometria** e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="f4f98-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="f4f98-126">Na seção Geometry novo (por exemplo, "Geometry2"), exclua apenas uma fila.</span><span class="sxs-lookup"><span data-stu-id="f4f98-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="f4f98-127">Com o botão direito na linha restante e clique em **Alterar tipo de linha**.</span><span class="sxs-lookup"><span data-stu-id="f4f98-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="f4f98-128">Na caixa de diálogo **Alterar tipo de linha** , selecione **Elipse** e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="f4f98-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="f4f98-129">Na seção **Foreign Image** , defina a fórmula para a célula **ClippingPath** para `="Geometry2.Path"` e aceite a fórmula.</span><span class="sxs-lookup"><span data-stu-id="f4f98-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

