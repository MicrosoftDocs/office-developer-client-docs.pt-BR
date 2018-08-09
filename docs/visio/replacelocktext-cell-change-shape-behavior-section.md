---
title: Célula ReplaceLockText (Seção Change Shape Behavior)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma. O ReplaceLockText determina se o texto exibido no mestre substitui o texto da forma que está sendo substituído.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772727"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="8e3b3-104">Célula ReplaceLockText (Seção Change Shape Behavior)</span><span class="sxs-lookup"><span data-stu-id="8e3b3-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="8e3b3-105">Indica se os valores das células especificadas em uma forma mestra substituir os valores (incluindo valores locais) de uma forma que está sendo substituído durante uma operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="8e3b3-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="8e3b3-106">O **ReplaceLockText** determina se o texto exibido no mestre substitui o texto da forma que está sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="8e3b3-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="8e3b3-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-107">**Value**</span></span>|<span data-ttu-id="8e3b3-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8e3b3-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="8e3b3-109">TRUE</span></span>  <br/> | <span data-ttu-id="8e3b3-110">O texto na forma mestra substitui o texto na forma antigo.</span><span class="sxs-lookup"><span data-stu-id="8e3b3-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="8e3b3-111">Além disso, a forma mestra substitui os valores das células nas seções a seguir durante uma operação de substituição de forma:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="8e3b3-112">Seção **Text Fields**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="8e3b3-113">Seção **Text Block Format**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="8e3b3-114">FALSO</span><span class="sxs-lookup"><span data-stu-id="8e3b3-114">FALSE</span></span>  <br/> |<span data-ttu-id="8e3b3-115">A forma de substituição contém qualquer texto, campos de texto ou outras propriedades de texto da forma antiga que foram adicionadas à forma.</span><span class="sxs-lookup"><span data-stu-id="8e3b3-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="8e3b3-116">Quando a forma de substituição contém propriedades de texto da forma antiga, a forma de substituição tem também os valores das seções de **parágrafo** e **caractere** da forma antiga, caso possuam mais de uma linha.</span><span class="sxs-lookup"><span data-stu-id="8e3b3-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="8e3b3-117">Se definido como verdadeiro (1), os valores da forma mestra substitui os valores das seguintes opções na forma sendo substituída:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="8e3b3-118">Célula TheText (Seção Events)</span><span class="sxs-lookup"><span data-stu-id="8e3b3-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="8e3b3-119">Células na [seção Character](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="8e3b3-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="8e3b3-120">Células na [seção Paragraph](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="8e3b3-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="8e3b3-121">Células na [seção Tabs](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="8e3b3-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e3b3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e3b3-122">Remarks</span></span>

<span data-ttu-id="8e3b3-123">Para fazer referência à célula **ReplaceLockText** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e3b3-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-124">Cell name:</span></span>  <br/> | <span data-ttu-id="8e3b3-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="8e3b3-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="8e3b3-126">Para obter uma referência à célula **ReplaceLockText** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e3b3-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-127">Section index:</span></span>  <br/> |<span data-ttu-id="8e3b3-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8e3b3-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-129">Row index:</span></span>  <br/> |<span data-ttu-id="8e3b3-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="8e3b3-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8e3b3-131">Cell index:</span></span>  <br/> |<span data-ttu-id="8e3b3-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="8e3b3-132">**visReplaceLockText**</span></span> <br/> |
   

