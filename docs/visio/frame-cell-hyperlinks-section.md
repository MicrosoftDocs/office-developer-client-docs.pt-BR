---
title: Célula Frame (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432853"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="2827b-104">Célula Frame (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="2827b-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="2827b-p102">Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="2827b-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2827b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2827b-107">Remarks</span></span>

<span data-ttu-id="2827b-108">Para fazer referência à célula Frame pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2827b-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2827b-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2827b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2827b-110">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="2827b-110">Hyperlink.</span></span>  <span data-ttu-id="2827b-111">*nome*  . Quadro onde Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="2827b-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="2827b-112">*nome*  é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="2827b-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2827b-113">Para fazer referência à célula Frame pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2827b-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2827b-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2827b-114">Section index:</span></span>  <br/> |<span data-ttu-id="2827b-115">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="2827b-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="2827b-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="2827b-116">Row index:</span></span>  <br/> |<span data-ttu-id="2827b-117">**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2827b-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2827b-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2827b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="2827b-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="2827b-119">**visHLinkFrame**</span></span> <br/> |
   

