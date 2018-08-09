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
ms.openlocfilehash: d0a07d8c86bd7e9ed3eb14074dda164f82c92475
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771769"
---
# <a name="doubleuline-cell-character-section"></a><span data-ttu-id="dde8e-103">Célula DoubleULine (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="dde8e-103">DoubleULine Cell (Character Section)</span></span>

<span data-ttu-id="dde8e-104">Determina se o intervalo de texto contém um sublinhado duplo abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="dde8e-104">Determines whether the range of text has a double underline below it.</span></span>
  
|<span data-ttu-id="dde8e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dde8e-105">**Value**</span></span>|<span data-ttu-id="dde8e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dde8e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dde8e-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="dde8e-107">TRUE</span></span>  <br/> |<span data-ttu-id="dde8e-108">O texto contém sublinhado duplo abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="dde8e-108">Text has a double underline below it.</span></span>  <br/> |
|<span data-ttu-id="dde8e-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="dde8e-109">FALSE</span></span>  <br/> |<span data-ttu-id="dde8e-110">O texto não contém sublinhado duplo abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="dde8e-110">Text does not have a double underline below it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dde8e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dde8e-111">Remarks</span></span>

<span data-ttu-id="dde8e-p101">A célula DoubleULine conterá informações de formatação aplicada a um subintervalo do texto de uma forma se a seção Caractere contiver diversas linhas. Caso contrário, ela conterá informações de formatação para todo o texto da forma.</span><span class="sxs-lookup"><span data-stu-id="dde8e-p101">The DoubleULine cell contains formatting information applied to a sub-range of a shape's text if the Characters section contains multiple rows. Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="dde8e-114">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (clique na seta **Fonte** na guia **Página Inicial**).</span><span class="sxs-lookup"><span data-stu-id="dde8e-114">You can also set the value of this cell by using the **Text** dialog box (click the **Font** arrow on the **Home** tab).</span></span> 
  
<span data-ttu-id="dde8e-115">Para obter uma referência para a célula DoubleULine pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="dde8e-115">To get a reference to the DoubleULine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dde8e-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="dde8e-116">Cell name:</span></span>  <br/> |<span data-ttu-id="dde8e-117">Char.DblUnderline [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="dde8e-117">Char.DblUnderline[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="dde8e-118">Para obter uma referência para a célula DoubleULine pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="dde8e-118">To get a reference to the DoubleULine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dde8e-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="dde8e-119">Section index:</span></span>  <br/> |<span data-ttu-id="dde8e-120">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="dde8e-120">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="dde8e-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="dde8e-121">Row index:</span></span>  <br/> |<span data-ttu-id="dde8e-122">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dde8e-122">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dde8e-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="dde8e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="dde8e-124">**visCharacterDblUnderline**</span><span class="sxs-lookup"><span data-stu-id="dde8e-124">**visCharacterDblUnderline**</span></span> <br/> |
   
