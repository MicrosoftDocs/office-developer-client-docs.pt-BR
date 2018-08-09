---
title: Célula Case (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Determina a utilização de maiúsculas e minúsculas no texto de uma forma. Todas as letras maiúsculas (1) e maiúsculas iniciais (2) não alteram a aparência do texto digitado completamente em letras maiúsculas. O texto deve ser digitado em letras minúsculas para que essas opções possam ter efeito.
ms.openlocfilehash: 9acd786b6fa38aec42990f1fd942174367f1135e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771439"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="90069-105">Célula Case (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="90069-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="90069-p102">Determina a utilização de maiúsculas e minúsculas no texto de uma forma. Todas as letras maiúsculas (1) e maiúsculas iniciais (2) não alteram a aparência do texto digitado completamente em letras maiúsculas. O texto deve ser digitado em letras minúsculas para que essas opções possam ter efeito.</span><span class="sxs-lookup"><span data-stu-id="90069-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="90069-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="90069-109">**Value**</span></span>|<span data-ttu-id="90069-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="90069-110">**Description**</span></span>|<span data-ttu-id="90069-111">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="90069-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="90069-112">0</span><span class="sxs-lookup"><span data-stu-id="90069-112">0</span></span>  <br/> | <span data-ttu-id="90069-113">Maiúsculas e minúsculas normais</span><span class="sxs-lookup"><span data-stu-id="90069-113">Normal case</span></span>  <br/> |<span data-ttu-id="90069-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="90069-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="90069-115">1</span><span class="sxs-lookup"><span data-stu-id="90069-115">1</span></span>  <br/> | <span data-ttu-id="90069-116">Tudo em letras maiúsculas</span><span class="sxs-lookup"><span data-stu-id="90069-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="90069-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="90069-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="90069-118">2</span><span class="sxs-lookup"><span data-stu-id="90069-118">2</span></span>  <br/> | <span data-ttu-id="90069-119">Somente as iniciais maiúsculas</span><span class="sxs-lookup"><span data-stu-id="90069-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="90069-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="90069-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90069-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="90069-121">Remarks</span></span>

<span data-ttu-id="90069-122">Para fazer referência à célula Case pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="90069-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="90069-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="90069-123">Cell name:</span></span>  <br/> | <span data-ttu-id="90069-124">Char.Case [ *i* ] onde *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="90069-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="90069-125">Para fazer referência à célula Case pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="90069-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="90069-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="90069-126">Section index:</span></span>  <br/> |<span data-ttu-id="90069-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="90069-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="90069-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="90069-128">Row index:</span></span>  <br/> |<span data-ttu-id="90069-129">**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="90069-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="90069-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="90069-130">Cell index:</span></span>  <br/> |<span data-ttu-id="90069-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="90069-131">**visCharacterCase**</span></span> <br/> |
   

