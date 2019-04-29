---
title: Célula Default (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434351"
---
# <a name="default-cell-hyperlinks-section"></a><span data-ttu-id="d3abc-104">Célula Padrão (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="d3abc-104">Default Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="d3abc-p102">Determina o hiperlink padrão de uma forma ou página. Defina o valor desta célula para VERDADEIRO para atribuir um hiperlink como o padrão.</span><span class="sxs-lookup"><span data-stu-id="d3abc-p102">Determines the default hyperlink for a shape or page. Set the value of this cell to TRUE to set a hyperlink as the default.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3abc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3abc-107">Remarks</span></span>

<span data-ttu-id="d3abc-p103">Também é possível definir o hiperlink padrão selecionando uma forma, clicando em **Hiperlink**, na guia **Inserir**, selecionando um hiperlink e clicando em **Padrão**. O hiperlink padrão é exibido em negrito.</span><span class="sxs-lookup"><span data-stu-id="d3abc-p103">You can also set the default hyperlink by selecting a shape, clicking **Hyperlink** on the **Insert** tab, selecting a hyperlink, and then clicking **Default**. The default hyperlink appears in bold text.</span></span>
  
<span data-ttu-id="d3abc-110">Para obter uma referência à célula Padrão pelo nome de uma outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="d3abc-110">To get a reference to the Default cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3abc-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d3abc-111">Cell name:</span></span>  <br/> |<span data-ttu-id="d3abc-112">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="d3abc-112">Hyperlink.</span></span> <span data-ttu-id="d3abc-113">*Nome*  .Default           onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="d3abc-113">*Name*  .Default           where Hyperlink.</span></span> <span data-ttu-id="d3abc-114">*Name*  é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="d3abc-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d3abc-115">Para obter uma referência à célula Padrão por índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d3abc-115">To get a reference to the Default cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3abc-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d3abc-116">Section index:</span></span>  <br/> |<span data-ttu-id="d3abc-117">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="d3abc-117">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="d3abc-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="d3abc-118">Row index:</span></span>  <br/> |<span data-ttu-id="d3abc-119">**visRow1stHyperlink** +  *i*           onde *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d3abc-119">**visRow1stHyperlink** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d3abc-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d3abc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d3abc-121">**visHLinkDefault**</span><span class="sxs-lookup"><span data-stu-id="d3abc-121">**visHLinkDefault**</span></span> <br/> |
   

