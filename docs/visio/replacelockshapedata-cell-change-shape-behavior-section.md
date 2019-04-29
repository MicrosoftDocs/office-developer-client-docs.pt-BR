---
title: Célula ReplaceLockShapeData (seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma. O ReplaceLockShapeData determina se os dados da forma da forma mestre substituirão todos os dados da forma da forma que está sendo substituída.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408870"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="7231b-104">Célula ReplaceLockShapeData (seção Change Shape Behavior)</span><span class="sxs-lookup"><span data-stu-id="7231b-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="7231b-105">Indica se os valores das células especificadas em uma forma mestre substituirão os valores (incluindo valores locais) de uma forma que está sendo substituída durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="7231b-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="7231b-106">O **ReplaceLockShapeData** determina se os dados da forma da forma mestre substituirão todos os dados da forma da forma que está sendo substituída.</span><span class="sxs-lookup"><span data-stu-id="7231b-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="7231b-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7231b-107">**Value**</span></span>|<span data-ttu-id="7231b-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7231b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7231b-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="7231b-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="7231b-110">Todas as linhas e valores da seção de **dados da forma** da forma mestre são copiados para a forma de substituição e quaisquer valores locais da forma antiga que está sendo substituído são descartados.</span><span class="sxs-lookup"><span data-stu-id="7231b-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="7231b-111">0 (FALSO)</span><span class="sxs-lookup"><span data-stu-id="7231b-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="7231b-112">As linhas e os valores da seção de **dados da forma** da forma mestre são copiados para a forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="7231b-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="7231b-113">Qualquer linha na seção **Shape data** da forma antiga com valores locais é transferida para a forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="7231b-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7231b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7231b-114">Remarks</span></span>

<span data-ttu-id="7231b-115">Para obter uma referência para a célula **ReplaceLockShapeData** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="7231b-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7231b-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7231b-116">Cell name:</span></span>  <br/> | <span data-ttu-id="7231b-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="7231b-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="7231b-118">Para obter uma referência para a célula **ReplaceLockShapeData** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7231b-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7231b-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7231b-119">Section index:</span></span>  <br/> |<span data-ttu-id="7231b-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7231b-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7231b-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="7231b-121">Row index:</span></span>  <br/> |<span data-ttu-id="7231b-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="7231b-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="7231b-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7231b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7231b-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="7231b-124">**visReplaceLockShapeData**</span></span> <br/> |
   

