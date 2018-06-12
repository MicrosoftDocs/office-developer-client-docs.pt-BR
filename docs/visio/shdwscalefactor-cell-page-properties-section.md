---
title: Célula ShdwScaleFactor (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Especifica a porcentagem de aumento ou redução da sombra de uma forma.
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772950"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a><span data-ttu-id="ec532-103">Célula ShdwScaleFactor (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="ec532-103">ShdwScaleFactor Cell (Page Properties Section)</span></span>

<span data-ttu-id="ec532-104">Especifica a porcentagem de aumento ou redução da sombra de uma forma.</span><span class="sxs-lookup"><span data-stu-id="ec532-104">Specifies the percentage to enlarge or reduce a shape's shadow.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ec532-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec532-105">Remarks</span></span>

<span data-ttu-id="ec532-106">Cada sombra possui um local de pino sombreado, que é um ponto na sombra que corresponde ao pino da forma.</span><span class="sxs-lookup"><span data-stu-id="ec532-106">Each shadow has a shadowed pin location, which is a point on the shadow that corresponds to the shape's pin.</span></span> <span data-ttu-id="ec532-107">Por exemplo, se o pino de uma forma estiver no centro da forma, o local do pino sombreado seria o ponto no centro da sombra.</span><span class="sxs-lookup"><span data-stu-id="ec532-107">For example, if a shape's pin is in the center of the shape, then the shadowed pin location would be the point in the center of the shadow.</span></span> <span data-ttu-id="ec532-108">Quando a aplicação da escala em sombras simples, a ampliação é centralizada no local do pino sombreado; Quando a aplicação da escala em sombras oblíquas, ampliação é aplicada na direção oblíqua.</span><span class="sxs-lookup"><span data-stu-id="ec532-108">When applying scale to simple shadows, magnification is centered at the shadowed pin location; when applying scale to oblique shadows, magnification is applied in the oblique direction.</span></span> 
  
 <span data-ttu-id="ec532-109">Esta porcentagem é utilizada quando o tipo de sombra para uma forma é definido como padrão da página (célula ShapeShdwType igual a * * visFSTPageDefault * *).</span><span class="sxs-lookup"><span data-stu-id="ec532-109">This percentage is used when the shadow type for a shape is set to Page Default (ShapeShdwType cell equals ** visFSTPageDefault ** ).</span></span> 
  
<span data-ttu-id="ec532-110">Para configurar este comportamento para uma forma individual, use a célula ShapeShdwScaleFactor na seção Fill Format.</span><span class="sxs-lookup"><span data-stu-id="ec532-110">To set this behavior for an individual shape, use the ShapeShdwScaleFactor cell in the Fill Format section.</span></span>
  
<span data-ttu-id="ec532-111">Esse valor corresponde ao valor na caixa **ampliação** da guia **sombras** na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="ec532-111">This value corresponds to the value in the **Magnification** box on the **Shadows** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="ec532-112">Para obter uma referência para a célula ShdwScaleFactor pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="ec532-112">To get a reference to the ShdwScaleFactor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec532-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ec532-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ec532-114">ShdwScaleFactor</span><span class="sxs-lookup"><span data-stu-id="ec532-114">ShdwScaleFactor</span></span>  <br/> |
   
<span data-ttu-id="ec532-115">Para obter uma referência para a célula ShdwScaleFactor pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ec532-115">To get a reference to the ShdwScaleFactor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ec532-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ec532-116">Section index:</span></span>  <br/> |<span data-ttu-id="ec532-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ec532-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ec532-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ec532-118">Row index:</span></span>  <br/> |<span data-ttu-id="ec532-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ec532-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="ec532-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ec532-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ec532-121">**visPageShdwScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="ec532-121">**visPageShdwScaleFactor**</span></span> <br/> |
   

