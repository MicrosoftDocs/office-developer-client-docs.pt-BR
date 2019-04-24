---
title: Célula ClippingPath (seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contém uma referência à geometria do caminho para o qual uma imagem está limitada.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341857"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="a6687-103">Célula ClippingPath (seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="a6687-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="a6687-104">Contém uma referência à geometria do caminho para o qual uma imagem está limitada.</span><span class="sxs-lookup"><span data-stu-id="a6687-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6687-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6687-105">Remarks</span></span>

<span data-ttu-id="a6687-106">Se a célula **ClippingPath** apontar para um caminho válido, a imagem será recortada para que a imagem seja renderizada dentro do caminho.</span><span class="sxs-lookup"><span data-stu-id="a6687-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="a6687-107">Se a célula **ClippingPath** estiver vazia ou contiver uma entrada inválida, a imagem será renderizada com um clipe retangular, usando os valores de Scale e offset.</span><span class="sxs-lookup"><span data-stu-id="a6687-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a6687-108">Somente caminhos definidos por uma seção [Geometry](geometry-section.md) no ShapeSheet da imagem são entradas válidas para a célula **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="a6687-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="a6687-109">Referências de folha cruzada não podem ser usadas para definir um caminho de recorte de imagem.</span><span class="sxs-lookup"><span data-stu-id="a6687-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="a6687-110">Para obter uma referência para a célula **ClippingPath** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="a6687-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6687-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a6687-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a6687-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="a6687-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="a6687-113">Para obter uma referência para a célula **ClippingPath** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a6687-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6687-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a6687-114">Section index:</span></span>  <br/> |<span data-ttu-id="a6687-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a6687-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a6687-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a6687-116">Row index:</span></span>  <br/> |<span data-ttu-id="a6687-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="a6687-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="a6687-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a6687-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a6687-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="a6687-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="a6687-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a6687-120">Example</span></span>

<span data-ttu-id="a6687-121">Você pode alterar a forma de limite de uma imagem para uma elipse fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a6687-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="a6687-122">Insira a imagem na tela de desenho.</span><span class="sxs-lookup"><span data-stu-id="a6687-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="a6687-123">Clique com o botão direito do mouse na imagem e selecione **Mostrar ShapeSheet**.</span><span class="sxs-lookup"><span data-stu-id="a6687-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="a6687-124">Clique com o botão direito do mouse em qualquer lugar na ShapeSheet e selecione **Inserir seção**.</span><span class="sxs-lookup"><span data-stu-id="a6687-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="a6687-125">Na caixa de diálogo **Inserir seção** , selecione **geometria** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6687-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="a6687-126">Na nova seção Geometry (por exemplo, "Geometry2"), exclua todas exceto uma linha.</span><span class="sxs-lookup"><span data-stu-id="a6687-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="a6687-127">Clique com o botão direito do mouse na linha restante e clique em **alterar tipo de linha**.</span><span class="sxs-lookup"><span data-stu-id="a6687-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="a6687-128">Na caixa de diálogo **alterar tipo de linha** , selecione **elipse** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6687-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="a6687-129">Na seção **imagem estrangeira** , defina a fórmula da célula **ClippingPath** como `="Geometry2.Path"` e aceite a fórmula.</span><span class="sxs-lookup"><span data-stu-id="a6687-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

