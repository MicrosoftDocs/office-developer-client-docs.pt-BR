---
title: Célula Spacing (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm955
localization_priority: Normal
ms.assetid: 46feb136-01ac-1303-66ab-d772c0ec41a0
description: Controla a quantidade de espaço entre dois ou mais caracteres. O espaço pode ser adicionado ou subtraído em incrementos de ponto de 1/20.
ms.openlocfilehash: 927b6203b81af453411cdd13b6f8c8342507a61b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334899"
---
# <a name="spacing-cell-character-section"></a><span data-ttu-id="9710d-104">Célula Spacing (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="9710d-104">Spacing Cell (Character Section)</span></span>

<span data-ttu-id="9710d-105">Controla a quantidade de espaço entre dois ou mais caracteres.</span><span class="sxs-lookup"><span data-stu-id="9710d-105">Controls the amount of space between two or more characters.</span></span> <span data-ttu-id="9710d-106">O espaço pode ser adicionado ou subtraído em incrementos de ponto de 1/20.</span><span class="sxs-lookup"><span data-stu-id="9710d-106">Space can be added or subtracted in 1/20th point increments.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9710d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9710d-107">Remarks</span></span>

<span data-ttu-id="9710d-108">Você também pode definir o valor da célula usando a caixa de diálogo **Texto** (na guia **Página Inicial**, clique na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="9710d-108">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="9710d-109">Para obter uma referência para a célula Spacing pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9710d-109">To get a reference to the Spacing cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9710d-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9710d-110">Cell name:</span></span>  <br/> |<span data-ttu-id="9710d-111">Char. Letterspace [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9710d-111">Char.Letterspace[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9710d-112">Para obter uma referência para a célula Spacing pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9710d-112">To get a reference to the Spacing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9710d-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9710d-113">Section index:</span></span>  <br/> |<span data-ttu-id="9710d-114">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="9710d-114">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="9710d-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9710d-115">Row index:</span></span>  <br/> |<span data-ttu-id="9710d-116">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9710d-116">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9710d-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9710d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="9710d-118">**visCharacterLetterspace**</span><span class="sxs-lookup"><span data-stu-id="9710d-118">**visCharacterLetterspace**</span></span> <br/> |
   

