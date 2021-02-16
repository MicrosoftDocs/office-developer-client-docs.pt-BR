---
title: Célula ClippingPath (Seção Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contém uma referência à geometria do caminho pelo o que uma imagem está limitada.
ms.openlocfilehash: cfbbb3ca7294f751f088df7c3284bf6461270af7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425509"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="711d3-103">Célula ClippingPath (Seção Foreign Image Info)</span><span class="sxs-lookup"><span data-stu-id="711d3-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="711d3-104">Contém uma referência à geometria do caminho pelo o que uma imagem está limitada.</span><span class="sxs-lookup"><span data-stu-id="711d3-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="711d3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="711d3-105">Remarks</span></span>

<span data-ttu-id="711d3-106">Se a **célula ClippingPath** aponta para um caminho válido, a imagem é cortada para que a imagem seja renderizada dentro do caminho.</span><span class="sxs-lookup"><span data-stu-id="711d3-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="711d3-107">Se a **célula ClippingPath** estiver vazia ou contiver uma entrada inválida, a imagem será renderizada com um clipe retangular, usando os valores de escala e deslocamento.</span><span class="sxs-lookup"><span data-stu-id="711d3-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="711d3-108">Somente caminhos definidos [por uma seção Geometry](geometry-section.md) no ShapeSheet da imagem são entradas válidas para a **célula ClippingPath.**</span><span class="sxs-lookup"><span data-stu-id="711d3-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="711d3-109">Referências entre planilhas não podem ser usadas para definir um caminho de recorte de imagem.</span><span class="sxs-lookup"><span data-stu-id="711d3-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="711d3-110">Para fazer referência à célula **ClippingPath** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="711d3-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="711d3-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="711d3-111">Cell name:</span></span>  <br/> | <span data-ttu-id="711d3-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="711d3-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="711d3-113">Para fazer referência à célula **ClippingPath** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="711d3-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="711d3-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="711d3-114">Section index:</span></span>  <br/> |<span data-ttu-id="711d3-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="711d3-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="711d3-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="711d3-116">Row index:</span></span>  <br/> |<span data-ttu-id="711d3-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="711d3-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="711d3-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="711d3-118">Cell index:</span></span>  <br/> |<span data-ttu-id="711d3-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="711d3-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="711d3-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="711d3-120">Example</span></span>

<span data-ttu-id="711d3-121">Você pode alterar a forma delimitativa de uma imagem para uma oval fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="711d3-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="711d3-122">Insira a imagem na tela de desenho.</span><span class="sxs-lookup"><span data-stu-id="711d3-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="711d3-123">Clique com o botão direito do mouse na imagem e selecione **Mostrar ShapeSheet**.</span><span class="sxs-lookup"><span data-stu-id="711d3-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="711d3-124">Clique com o botão direito do mouse em qualquer lugar no ShapeSheet e selecione **Inserir Seção.**</span><span class="sxs-lookup"><span data-stu-id="711d3-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="711d3-125">Na caixa **de diálogo Inserir Seção,** selecione **Geometria e** clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="711d3-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="711d3-126">Na nova seção Geometry (por exemplo, "Geometry2"), exclua apenas uma linha.</span><span class="sxs-lookup"><span data-stu-id="711d3-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="711d3-127">Clique com o botão direito do mouse na linha restante e clique em **Alterar Tipo de Linha.**</span><span class="sxs-lookup"><span data-stu-id="711d3-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="711d3-128">Na caixa **de diálogo Alterar Tipo** de Linha, selecione **Elipse** e clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="711d3-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="711d3-129">Na seção **Imagem Externa,** de definida a fórmula para a célula **ClippingPath** e aceite  `="Geometry2.Path"` a fórmula.</span><span class="sxs-lookup"><span data-stu-id="711d3-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

