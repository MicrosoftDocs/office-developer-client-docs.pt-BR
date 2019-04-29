---
title: Célula LineWeight (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Determina a espessura da linha de uma forma. Defina a espessura inserindo um número com uma unidade de medida válida.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412244"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="c6ce3-104">Célula LineWeight (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="c6ce3-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="c6ce3-105">Determina a espessura da linha de uma forma.</span><span class="sxs-lookup"><span data-stu-id="c6ce3-105">Determines the line weight of a shape.</span></span> <span data-ttu-id="c6ce3-106">Defina a espessura inserindo um número com uma unidade de medida válida.</span><span class="sxs-lookup"><span data-stu-id="c6ce3-106">Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6ce3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6ce3-107">Remarks</span></span>

<span data-ttu-id="c6ce3-108">Você também pode definir o valor da célula LineWeight na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Espessura** e clique em **Mais Linhas**).</span><span class="sxs-lookup"><span data-stu-id="c6ce3-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="c6ce3-109">Se a unidade de medida não for inserida, a unidade de medida do texto especificado na caixa de diálogo **Opções do Visio** será usada (clique na guia **arquivo** e em **Opções**).</span><span class="sxs-lookup"><span data-stu-id="c6ce3-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="c6ce3-110">A espessura da linha não depende da escala do desenho.</span><span class="sxs-lookup"><span data-stu-id="c6ce3-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="c6ce3-111">Se o desenho estiver dimensionado, a espessura será a mesma.</span><span class="sxs-lookup"><span data-stu-id="c6ce3-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="c6ce3-112">Para fazer referência à célula IsDropSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c6ce3-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6ce3-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c6ce3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c6ce3-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="c6ce3-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="c6ce3-115">Para fazer referência à célula LineWeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c6ce3-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c6ce3-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c6ce3-116">Section index:</span></span>  <br/> |<span data-ttu-id="c6ce3-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6ce3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c6ce3-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c6ce3-118">Row index:</span></span>  <br/> |<span data-ttu-id="c6ce3-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="c6ce3-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="c6ce3-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="c6ce3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c6ce3-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="c6ce3-121">**visLineWeight**</span></span> <br/> |
   

