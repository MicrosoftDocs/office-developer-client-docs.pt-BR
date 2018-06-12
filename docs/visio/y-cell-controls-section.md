---
title: Célula Y (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Representa o y-coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773322"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="b3add-103">Célula Y (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="b3add-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="b3add-104">Representa o *y* -coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="b3add-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3add-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b3add-105">Remarks</span></span>

<span data-ttu-id="b3add-106">Para obter uma referência à célula Y pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b3add-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3add-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b3add-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b3add-108">Controles.</span><span class="sxs-lookup"><span data-stu-id="b3add-108">Controls.</span></span>  <span data-ttu-id="b3add-109">*nome* . Controles de Ywhere.</span><span class="sxs-lookup"><span data-stu-id="b3add-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="b3add-110">*nome* é o nome da linha controles.</span><span class="sxs-lookup"><span data-stu-id="b3add-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="b3add-111">Para obter uma referência à célula Y pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b3add-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3add-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b3add-112">Section index:</span></span>  <br/> |<span data-ttu-id="b3add-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="b3add-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="b3add-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b3add-114">Row index:</span></span>  <br/> |<span data-ttu-id="b3add-115">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b3add-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b3add-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b3add-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b3add-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="b3add-117">**visCtlY**</span></span> <br/> |
   

