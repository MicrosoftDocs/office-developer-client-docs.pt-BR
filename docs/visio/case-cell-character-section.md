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
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337230"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="d0b4d-105">Célula Case (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="d0b4d-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="d0b4d-p102">Determina a utilização de maiúsculas e minúsculas no texto de uma forma. Todas as letras maiúsculas (1) e maiúsculas iniciais (2) não alteram a aparência do texto digitado completamente em letras maiúsculas. O texto deve ser digitado em letras minúsculas para que essas opções possam ter efeito.</span><span class="sxs-lookup"><span data-stu-id="d0b4d-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="d0b4d-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-109">**Value**</span></span>|<span data-ttu-id="d0b4d-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-110">**Description**</span></span>|<span data-ttu-id="d0b4d-111">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="d0b4d-112">,0</span><span class="sxs-lookup"><span data-stu-id="d0b4d-112">0</span></span>  <br/> | <span data-ttu-id="d0b4d-113">Maiúsculas e minúsculas normais</span><span class="sxs-lookup"><span data-stu-id="d0b4d-113">Normal case</span></span>  <br/> |<span data-ttu-id="d0b4d-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="d0b4d-115">1</span><span class="sxs-lookup"><span data-stu-id="d0b4d-115">1</span></span>  <br/> | <span data-ttu-id="d0b4d-116">Tudo em letras maiúsculas</span><span class="sxs-lookup"><span data-stu-id="d0b4d-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="d0b4d-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="d0b4d-118">duas</span><span class="sxs-lookup"><span data-stu-id="d0b4d-118">2</span></span>  <br/> | <span data-ttu-id="d0b4d-119">Somente as iniciais maiúsculas</span><span class="sxs-lookup"><span data-stu-id="d0b4d-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="d0b4d-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0b4d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0b4d-121">Remarks</span></span>

<span data-ttu-id="d0b4d-122">Para fazer referência à célula Case pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d0b4d-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0b4d-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d0b4d-123">Cell name:</span></span>  <br/> | <span data-ttu-id="d0b4d-124">Char. case [ *i* ] onde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="d0b4d-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="d0b4d-125">Para fazer referência à célula Case pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d0b4d-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0b4d-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d0b4d-126">Section index:</span></span>  <br/> |<span data-ttu-id="d0b4d-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="d0b4d-128">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d0b4d-128">Row index:</span></span>  <br/> |<span data-ttu-id="d0b4d-129">**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="d0b4d-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="d0b4d-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d0b4d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="d0b4d-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="d0b4d-131">**visCharacterCase**</span></span> <br/> |
   

