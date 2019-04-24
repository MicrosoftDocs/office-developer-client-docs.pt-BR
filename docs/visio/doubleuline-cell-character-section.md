---
title: Célula DoubleULine (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Determina se o intervalo de texto contém um sublinhado duplo abaixo dele.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357460"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="d64ba-103">Célula DoubleULine (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="d64ba-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="d64ba-104">Determina se o intervalo de texto contém um sublinhado duplo abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="d64ba-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="d64ba-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d64ba-105">**Value**</span></span>|<span data-ttu-id="d64ba-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d64ba-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d64ba-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d64ba-107">TRUE</span></span>  <br/> |<span data-ttu-id="d64ba-108">O texto contém sublinhado duplo abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="d64ba-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="d64ba-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d64ba-109">FALSE</span></span>  <br/> |<span data-ttu-id="d64ba-110">O texto não contém sublinhado duplo abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="d64ba-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d64ba-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d64ba-111">Remarks</span></span>

<span data-ttu-id="d64ba-p101">A célula DoubleULine conterá informações de formatação aplicada a um subintervalo do texto de uma forma se a seção Caractere contiver diversas linhas. Caso contrário, ela conterá informações de formatação para todo o texto da forma.</span><span class="sxs-lookup"><span data-stu-id="d64ba-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="d64ba-114">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (clique na seta **Fonte** na guia **Página Inicial**).</span><span class="sxs-lookup"><span data-stu-id="d64ba-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="d64ba-115">Para obter uma referência para a célula DoubleULine pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d64ba-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d64ba-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d64ba-116">Cell name:</span></span>  <br/> |<span data-ttu-id="d64ba-117">Char. DblUnderline [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d64ba-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d64ba-118">Para obter uma referência para a célula DoubleULine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d64ba-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d64ba-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d64ba-119">Section index:</span></span>  <br/> |<span data-ttu-id="d64ba-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d64ba-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d64ba-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d64ba-121">Row index:</span></span>  <br/> |<span data-ttu-id="d64ba-122">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d64ba-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d64ba-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d64ba-123">Cell index:</span></span>  <br/> |<span data-ttu-id="d64ba-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="d64ba-124">**visCharacterDblUnderline**</span></span> <br/> |
   

