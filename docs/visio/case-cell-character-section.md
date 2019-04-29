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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434344"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="cae63-105">Célula Case (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="cae63-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="cae63-p102">Determina a utilização de maiúsculas e minúsculas no texto de uma forma. Todas as letras maiúsculas (1) e maiúsculas iniciais (2) não alteram a aparência do texto digitado completamente em letras maiúsculas. O texto deve ser digitado em letras minúsculas para que essas opções possam ter efeito.</span><span class="sxs-lookup"><span data-stu-id="cae63-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="cae63-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cae63-109">**Value**</span></span>|<span data-ttu-id="cae63-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cae63-110">**Description**</span></span>|<span data-ttu-id="cae63-111">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="cae63-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="cae63-112">,0</span><span class="sxs-lookup"><span data-stu-id="cae63-112">0</span></span>  <br/> | <span data-ttu-id="cae63-113">Maiúsculas e minúsculas normais</span><span class="sxs-lookup"><span data-stu-id="cae63-113">Normal case</span></span>  <br/> |<span data-ttu-id="cae63-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="cae63-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="cae63-115">1</span><span class="sxs-lookup"><span data-stu-id="cae63-115">1</span></span>  <br/> | <span data-ttu-id="cae63-116">Tudo em letras maiúsculas</span><span class="sxs-lookup"><span data-stu-id="cae63-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="cae63-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="cae63-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="cae63-118">duas</span><span class="sxs-lookup"><span data-stu-id="cae63-118">2</span></span>  <br/> | <span data-ttu-id="cae63-119">Somente as iniciais maiúsculas</span><span class="sxs-lookup"><span data-stu-id="cae63-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="cae63-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="cae63-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cae63-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae63-121">Remarks</span></span>

<span data-ttu-id="cae63-122">Para fazer referência à célula Case pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cae63-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cae63-123">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cae63-123">Cell name:</span></span>  <br/> | <span data-ttu-id="cae63-124">Char. case [ *i* ] onde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="cae63-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="cae63-125">Para fazer referência à célula Case pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cae63-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cae63-126">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cae63-126">Section index:</span></span>  <br/> |<span data-ttu-id="cae63-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="cae63-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="cae63-128">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cae63-128">Row index:</span></span>  <br/> |<span data-ttu-id="cae63-129">**visRowCharacter** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="cae63-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="cae63-130">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cae63-130">Cell index:</span></span>  <br/> |<span data-ttu-id="cae63-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="cae63-131">**visCharacterCase**</span></span> <br/> |
   

