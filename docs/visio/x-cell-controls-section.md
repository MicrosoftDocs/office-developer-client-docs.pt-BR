---
title: Célula X (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Representa o x-coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773302"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="f72c4-103">Célula X (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="f72c4-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="f72c4-104">Representa o *x* -coordenada que indica a localização da alça de controle de uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="f72c4-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f72c4-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="f72c4-105">Remarks</span></span>

<span data-ttu-id="f72c4-106">Para obter uma referência à célula X pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="f72c4-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f72c4-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f72c4-107">Cell name:</span></span>  <br/> | <span data-ttu-id="f72c4-108">Controles.</span><span class="sxs-lookup"><span data-stu-id="f72c4-108">Controls.</span></span>  <span data-ttu-id="f72c4-109">*nome* . X, onde controla.</span><span class="sxs-lookup"><span data-stu-id="f72c4-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="f72c4-110">*nome* é o nome da linha controles.</span><span class="sxs-lookup"><span data-stu-id="f72c4-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f72c4-111">Para obter uma referência à célula X pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f72c4-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f72c4-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f72c4-112">Section index:</span></span>  <br/> |<span data-ttu-id="f72c4-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f72c4-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f72c4-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f72c4-114">Row index:</span></span>  <br/> |<span data-ttu-id="f72c4-115">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f72c4-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f72c4-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f72c4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f72c4-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="f72c4-117">**visCtlX**</span></span> <br/> |
   

