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
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771945"
---
# <a name="frame-cell-hyperlinks-section"></a><span data-ttu-id="11673-104">Célula Frame (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="11673-104">Frame Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="11673-p102">Representa o nome de um quadro a ser direcionado quando o aplicativo estiver aberto como um documento ativo em um aplicativo contêiner. O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="11673-p102">Represents the name of a frame to target when the application is open as an Active document in a container application. The default is an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11673-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="11673-107">Remarks</span></span>

<span data-ttu-id="11673-108">Para fazer referência à célula Frame pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="11673-108">To get a reference to the Frame cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11673-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="11673-109">Cell name:</span></span>  <br/> | <span data-ttu-id="11673-110">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="11673-110">Hyperlink.</span></span>  <span data-ttu-id="11673-111">*nome* . Enquadrar onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="11673-111">*name*  .Frame            where Hyperlink.</span></span>  <span data-ttu-id="11673-112">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="11673-112">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="11673-113">Para fazer referência à célula Frame pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="11673-113">To get a reference to the Frame cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11673-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="11673-114">Section index:</span></span>  <br/> |<span data-ttu-id="11673-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="11673-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="11673-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="11673-116">Row index:</span></span>  <br/> |<span data-ttu-id="11673-117">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="11673-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="11673-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="11673-118">Cell index:</span></span>  <br/> |<span data-ttu-id="11673-119">**visHLinkFrame**</span><span class="sxs-lookup"><span data-stu-id="11673-119">**visHLinkFrame**</span></span> <br/> |
   

