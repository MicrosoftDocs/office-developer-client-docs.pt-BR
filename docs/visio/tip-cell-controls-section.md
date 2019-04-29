---
title: Célula Tip (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Representa uma sequência de texto descritiva exibida como uma dica de ferramenta quando o usuário posiciona o ponteiro do mouse sobre a alça de controle de uma forma. O aplicativo inclui automaticamente a dica entre aspas na célula, mas as aspas não são exibidas na dica de ferramenta.
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424858"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="24d36-104">Célula Tip (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="24d36-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="24d36-p102">Representa uma sequência de texto descritiva exibida como uma dica de ferramenta quando o usuário posiciona o ponteiro do mouse sobre a alça de controle de uma forma. O aplicativo inclui automaticamente a dica entre aspas na célula, mas as aspas não são exibidas na dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="24d36-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24d36-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="24d36-107">Remarks</span></span>

<span data-ttu-id="24d36-108">Para fazer referência à célula Tip pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="24d36-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24d36-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="24d36-109">Cell name:</span></span>  <br/> | <span data-ttu-id="24d36-110">Menores.</span><span class="sxs-lookup"><span data-stu-id="24d36-110">Controls.</span></span>  <span data-ttu-id="24d36-111">*nome* . Controles Tipwhere.</span><span class="sxs-lookup"><span data-stu-id="24d36-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="24d36-112">*Name* é o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="24d36-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="24d36-113">Para fazer referência à célula Tip pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="24d36-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="24d36-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="24d36-114">Section index:</span></span>  <br/> |<span data-ttu-id="24d36-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="24d36-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="24d36-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="24d36-116">Row index:</span></span>  <br/> |<span data-ttu-id="24d36-117">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="24d36-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="24d36-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="24d36-118">Cell index:</span></span>  <br/> |<span data-ttu-id="24d36-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="24d36-119">**visCtlTip**</span></span> <br/> |
   

