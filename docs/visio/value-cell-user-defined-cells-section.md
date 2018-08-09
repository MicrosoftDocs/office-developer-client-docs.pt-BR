---
title: Célula Value (Seção User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Especifica um valor para a célula definida pelo usuário correspondente.
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773246"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="b4773-103">Célula Value (Seção User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="b4773-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="b4773-104">Especifica um valor para a célula definida pelo usuário correspondente.</span><span class="sxs-lookup"><span data-stu-id="b4773-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4773-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4773-105">Remarks</span></span>

<span data-ttu-id="b4773-106">Para fazer referência a esse valor em outra célula, especifique o nome definido pelo usuário inserido no rótulo da linha User.Row.</span><span class="sxs-lookup"><span data-stu-id="b4773-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="b4773-107">Para fazer referência à célula Value pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b4773-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4773-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b4773-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b4773-109">Usuário.</span><span class="sxs-lookup"><span data-stu-id="b4773-109">User.</span></span>  <span data-ttu-id="b4773-110">*Nome* . Valor where usuário.</span><span class="sxs-lookup"><span data-stu-id="b4773-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="b4773-111">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="b4773-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b4773-112">Para obter uma referência para a célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b4773-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b4773-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b4773-113">Section index:</span></span>  <br/> |<span data-ttu-id="b4773-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="b4773-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="b4773-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b4773-115">Row index:</span></span>  <br/> |<span data-ttu-id="b4773-116">**visRowUser** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b4773-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b4773-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b4773-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b4773-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="b4773-118">**visUserValue**</span></span> <br/> |
   

