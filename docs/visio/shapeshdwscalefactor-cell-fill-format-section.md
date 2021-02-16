---
title: Célula ShapeShdwScaleFactor (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033175
localization_priority: Normal
ms.assetid: 94ec06c5-8d2f-dd27-1eed-1abaf93daba8
description: Especifica a porcentagem pela qual a sombra de uma forma pode ser aumentada ou reduzida.
ms.openlocfilehash: 5862b61ca1f5df25ca97bf8742b9e20bf45091a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436262"
---
# <a name="shapeshdwscalefactor-cell-fill-format-section"></a><span data-ttu-id="ca6aa-103">Célula ShapeShdwScaleFactor (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="ca6aa-103">ShapeShdwScaleFactor Cell (Fill Format Section)</span></span>

<span data-ttu-id="ca6aa-104">Especifica a porcentagem pela qual a sombra de uma forma pode ser aumentada ou reduzida.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-104">Specifies the percentage by which the shadow of a shape can be enlarged or reduced.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca6aa-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca6aa-105">Remarks</span></span>

<span data-ttu-id="ca6aa-106">Cada sombra possui um local de pino sombreado, que representa um ponto na sombra que corresponde ao pino da forma.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="ca6aa-107">Por exemplo, se o pino de uma forma estiver no centro dela, então o local do pino sombreado será o ponto no centro da sombra.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="ca6aa-108">Ao aplicar escala a sombras simples, a ampliação é centralizada no local do pino sombreado; ao aplicar escala a sombras oblíquas, a ampliação é aplicada na direção oblíqua.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
<span data-ttu-id="ca6aa-109">Para definir esse valor para todas as formas de uma página, use a célula ShdwScaleFactor na seção Page Properties.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-109">To set this value for all the shapes on a page, use the ShdwScaleFactor cell in the Page Properties section.</span></span>
  
<span data-ttu-id="ca6aa-110">Esse valor corresponde ao valor existente na configuração **Ampliação** na caixa de diálogo **Sombra** (na guia **Página Inicial**, do grupo **Forma**, clique em **Sombra** e em **Opções de sombra**).</span><span class="sxs-lookup"><span data-stu-id="ca6aa-110">This value corresponds to the value of the **Magnification** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="ca6aa-111">Para obter uma referência para a célula ShapeShdwScaleFactor pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ca6aa-111">To get a reference to the ShapeShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca6aa-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ca6aa-112">Cell name:</span></span>  <br/> |<span data-ttu-id="ca6aa-113">ShapeShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="ca6aa-113">ShapeShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="ca6aa-114">Para obter uma referência para a célula ShapeShdwScaleFactor pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ca6aa-114">To get a reference to the ShapeShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca6aa-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ca6aa-115">Section index:</span></span>  <br/> |<span data-ttu-id="ca6aa-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca6aa-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ca6aa-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ca6aa-117">Row index:</span></span>  <br/> |<span data-ttu-id="ca6aa-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="ca6aa-118">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="ca6aa-119">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="ca6aa-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ca6aa-120">**visFillShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="ca6aa-120">**visFillShdwScaleFactor**</span></span> <br/> |
   

