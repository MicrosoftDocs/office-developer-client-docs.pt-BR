---
title: Célula PageWidth (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Determina a largura da página impressa em unidades de desenho.
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772471"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="16dbb-103">Célula PageWidth (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="16dbb-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="16dbb-104">Determina a largura da página impressa em unidades de desenho.</span><span class="sxs-lookup"><span data-stu-id="16dbb-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16dbb-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="16dbb-105">Remarks</span></span>

<span data-ttu-id="16dbb-106">Você também pode definir a largura da página na guia **Tamanho da página** da caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ) ou redimensionar manualmente a página com o mouse.</span><span class="sxs-lookup"><span data-stu-id="16dbb-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="16dbb-107">Para fazer isso, arraste a borda da página, mantendo pressionada a tecla CTRL.</span><span class="sxs-lookup"><span data-stu-id="16dbb-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="16dbb-108">Para obter uma referência para a célula PageWidth pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="16dbb-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16dbb-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="16dbb-109">Cell name:</span></span>  <br/> |<span data-ttu-id="16dbb-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="16dbb-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="16dbb-111">Para obter uma referência para a célula PageWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="16dbb-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16dbb-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="16dbb-112">Section index:</span></span>  <br/> |<span data-ttu-id="16dbb-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="16dbb-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="16dbb-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="16dbb-114">Row index:</span></span>  <br/> |<span data-ttu-id="16dbb-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="16dbb-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="16dbb-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="16dbb-116">Cell index:</span></span>  <br/> |<span data-ttu-id="16dbb-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="16dbb-117">**visPageWidth**</span></span> <br/> |
   

