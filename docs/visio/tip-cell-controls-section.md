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
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773156"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="4c2db-104">Célula Tip (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="4c2db-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="4c2db-p102">Representa uma sequência de texto descritiva exibida como uma dica de ferramenta quando o usuário posiciona o ponteiro do mouse sobre a alça de controle de uma forma. O aplicativo inclui automaticamente a dica entre aspas na célula, mas as aspas não são exibidas na dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="4c2db-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c2db-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c2db-107">Remarks</span></span>

<span data-ttu-id="4c2db-108">Para obter uma referência à célula Tip pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="4c2db-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c2db-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4c2db-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4c2db-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="4c2db-110">Controls.</span></span>  <span data-ttu-id="4c2db-111">*nome* . Controles de Tipwhere.</span><span class="sxs-lookup"><span data-stu-id="4c2db-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="4c2db-112">*nome* é o nome da linha controles.</span><span class="sxs-lookup"><span data-stu-id="4c2db-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="4c2db-113">Para obter uma referência à célula Tip pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4c2db-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c2db-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4c2db-114">Section index:</span></span>  <br/> |<span data-ttu-id="4c2db-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="4c2db-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="4c2db-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4c2db-116">Row index:</span></span>  <br/> |<span data-ttu-id="4c2db-117">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4c2db-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4c2db-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4c2db-118">Cell index:</span></span>  <br/> |<span data-ttu-id="4c2db-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="4c2db-119">**visCtlTip**</span></span> <br/> |
   

