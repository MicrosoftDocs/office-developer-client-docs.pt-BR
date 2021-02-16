---
title: Célula Overline (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Determina se o texto conterá uma linha acima dele.
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431642"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="943ed-103">Célula Overline (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="943ed-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="943ed-104">Determina se o texto conterá uma linha acima dele.</span><span class="sxs-lookup"><span data-stu-id="943ed-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="943ed-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="943ed-105">**Value**</span></span>|<span data-ttu-id="943ed-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="943ed-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="943ed-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="943ed-107">TRUE</span></span>  <br/> |<span data-ttu-id="943ed-108">O texto contém uma linha acima dele.</span><span class="sxs-lookup"><span data-stu-id="943ed-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="943ed-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="943ed-109">FALSE</span></span>  <br/> |<span data-ttu-id="943ed-110">O texto não contém uma linha acima dele.</span><span class="sxs-lookup"><span data-stu-id="943ed-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="943ed-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="943ed-111">Remarks</span></span>

<span data-ttu-id="943ed-112">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="943ed-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="943ed-113">Para obter uma referência para a célula Overline pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="943ed-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="943ed-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="943ed-114">Cell name:</span></span>  <br/> |<span data-ttu-id="943ed-115">Char.Overline[ *i*  ] onde i =  *<*  1>, 2.</span><span class="sxs-lookup"><span data-stu-id="943ed-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="943ed-116">3...</span><span class="sxs-lookup"><span data-stu-id="943ed-116">3...</span></span>  <br/> |
   
<span data-ttu-id="943ed-117">Para obter uma referência para a célula Overline pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="943ed-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="943ed-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="943ed-118">Section index:</span></span>  <br/> |<span data-ttu-id="943ed-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="943ed-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="943ed-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="943ed-120">Row index:</span></span>  <br/> |<span data-ttu-id="943ed-121">**visRowCharacter**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="943ed-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="943ed-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="943ed-122">Cell index:</span></span>  <br/> |<span data-ttu-id="943ed-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="943ed-123">**visCharacterOverline**</span></span> <br/> |
   

