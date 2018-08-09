---
title: Célula LinePattern (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Determina o padrão de linha de uma forma. O valor inserido na célula LinePattern é um número que serve de índice para uma coleção de padrões de linha.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772200"
---
# <a name="linepattern-cell-line-format-section"></a><span data-ttu-id="e4d02-104">Célula LinePattern (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="e4d02-104">LinePattern Cell (Line Format Section)</span></span>

<span data-ttu-id="e4d02-p102">Determina o padrão de linha de uma forma. O valor inserido na célula LinePattern é um número que serve de índice para uma coleção de padrões de linha.</span><span class="sxs-lookup"><span data-stu-id="e4d02-p102">Determines the line pattern of the shape. The value entered in the LinePattern cell is a number that is an index into a collection of line patterns.</span></span>
  
|<span data-ttu-id="e4d02-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e4d02-107">**Value**</span></span>|<span data-ttu-id="e4d02-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e4d02-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4d02-109">0</span><span class="sxs-lookup"><span data-stu-id="e4d02-109">0</span></span>  <br/> |<span data-ttu-id="e4d02-110">Sem padrão de linha</span><span class="sxs-lookup"><span data-stu-id="e4d02-110">No line pattern</span></span>  <br/> |
|<span data-ttu-id="e4d02-111">1</span><span class="sxs-lookup"><span data-stu-id="e4d02-111">1</span></span>  <br/> |<span data-ttu-id="e4d02-112">Sólido</span><span class="sxs-lookup"><span data-stu-id="e4d02-112">Solid</span></span>  <br/> |
|<span data-ttu-id="e4d02-113">2 - 23</span><span class="sxs-lookup"><span data-stu-id="e4d02-113">2 - 23</span></span>  <br/> |<span data-ttu-id="e4d02-114">Padrões de linha variados</span><span class="sxs-lookup"><span data-stu-id="e4d02-114">Assorted line patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4d02-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4d02-115">Remarks</span></span>

<span data-ttu-id="e4d02-116">É possível visualizar a coleção de padrões de linha na caixa de diálogo **Linha** (na guia **Página Inicial** no grupo **Forma**, clique em **Linha**, aponte para **Traços** e clique em **Mais Linhas**).</span><span class="sxs-lookup"><span data-stu-id="e4d02-116">You can view the line pattern collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Dashes**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="e4d02-117">Para especificar um padrão de linha personalizado, utilize a função USE desta célula.</span><span class="sxs-lookup"><span data-stu-id="e4d02-117">To specify a custom line pattern, use the USE function in this cell.</span></span>
  
<span data-ttu-id="e4d02-118">Para obter uma referência para a célula LinePattern pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e4d02-118">To get a reference to the LinePattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4d02-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e4d02-119">Cell name:</span></span>  <br/> |<span data-ttu-id="e4d02-120">LinePattern</span><span class="sxs-lookup"><span data-stu-id="e4d02-120">LinePattern</span></span>  <br/> |
   
<span data-ttu-id="e4d02-121">Para obter uma referência para a célula LinePattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e4d02-121">To get a reference to the LinePattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4d02-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e4d02-122">Section index:</span></span>  <br/> |<span data-ttu-id="e4d02-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e4d02-123">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e4d02-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e4d02-124">Row index:</span></span>  <br/> |<span data-ttu-id="e4d02-125">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="e4d02-125">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="e4d02-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e4d02-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e4d02-127">**visLinePattern**</span><span class="sxs-lookup"><span data-stu-id="e4d02-127">**visLinePattern**</span></span> <br/> |
   

