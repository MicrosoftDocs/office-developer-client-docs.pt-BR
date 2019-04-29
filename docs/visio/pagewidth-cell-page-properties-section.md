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
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434267"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="10490-103">Célula PageWidth (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="10490-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="10490-104">Determina a largura da página impressa em unidades de desenho.</span><span class="sxs-lookup"><span data-stu-id="10490-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="10490-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="10490-105">Remarks</span></span>

<span data-ttu-id="10490-106">Você também pode definir a largura da página na **guia Tamanho da página** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ) ou redimensionando manualmente a página com o mouse.</span><span class="sxs-lookup"><span data-stu-id="10490-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="10490-107">Para fazer isso, mantenha pressionada a tecla CTRL e arraste a borda da página.</span><span class="sxs-lookup"><span data-stu-id="10490-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="10490-108">Para obter uma referência para a célula PageWidth pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="10490-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10490-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="10490-109">Cell name:</span></span>  <br/> |<span data-ttu-id="10490-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="10490-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="10490-111">Para obter uma referência para a célula PageWidth pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="10490-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10490-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="10490-112">Section index:</span></span>  <br/> |<span data-ttu-id="10490-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10490-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="10490-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="10490-114">Row index:</span></span>  <br/> |<span data-ttu-id="10490-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="10490-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="10490-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="10490-116">Cell index:</span></span>  <br/> |<span data-ttu-id="10490-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="10490-117">**visPageWidth**</span></span> <br/> |
   

