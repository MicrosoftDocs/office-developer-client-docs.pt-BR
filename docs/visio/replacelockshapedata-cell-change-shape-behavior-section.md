---
title: Célula ReplaceLockShapeData (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. O ReplaceLockShapeData determina se os dados da forma da forma mestra substitui todos os dados da forma da forma que está sendo substituído.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772716"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="a24b9-104">Célula ReplaceLockShapeData (Seção Change Shape Behavior)</span><span class="sxs-lookup"><span data-stu-id="a24b9-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="a24b9-105">Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="a24b9-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="a24b9-106">O **ReplaceLockShapeData** determina se os dados da forma da forma mestra substitui todos os dados da forma da forma que está sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="a24b9-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="a24b9-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a24b9-107">**Value**</span></span>|<span data-ttu-id="a24b9-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a24b9-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a24b9-109">1 (VERDADEIRO)</span><span class="sxs-lookup"><span data-stu-id="a24b9-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="a24b9-110">Todas as linhas e os valores da seção **Shape Data** da forma mestra são copiados para a forma de substituição e quaisquer valores locais da forma que está sendo substituído antiga serão descartados.</span><span class="sxs-lookup"><span data-stu-id="a24b9-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="a24b9-111">0 (FALSO)</span><span class="sxs-lookup"><span data-stu-id="a24b9-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="a24b9-112">As linhas e os valores da seção **Shape Data** da forma mestra são copiados para a forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="a24b9-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="a24b9-113">Qualquer linha na seção **Dados da forma** da forma antiga com valores locais é transferida para a forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="a24b9-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a24b9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a24b9-114">Remarks</span></span>

<span data-ttu-id="a24b9-115">Para fazer referência à célula **ReplaceLockShapeData** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="a24b9-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a24b9-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a24b9-116">Cell name:</span></span>  <br/> | <span data-ttu-id="a24b9-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="a24b9-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="a24b9-118">Para obter uma referência à célula **ReplaceLockShapeData** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a24b9-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a24b9-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a24b9-119">Section index:</span></span>  <br/> |<span data-ttu-id="a24b9-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a24b9-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a24b9-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a24b9-121">Row index:</span></span>  <br/> |<span data-ttu-id="a24b9-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="a24b9-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="a24b9-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a24b9-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a24b9-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="a24b9-124">**visReplaceLockShapeData**</span></span> <br/> |
   

