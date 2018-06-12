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
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772208"
---
# <a name="lineweight-cell-line-format-section"></a><span data-ttu-id="81c0a-104">Célula LineWeight (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="81c0a-104">LineWeight Cell (Line Format Section)</span></span>

<span data-ttu-id="81c0a-p102">Determina a espessura da linha de uma forma. Defina a espessura inserindo um número com uma unidade de medida válida.</span><span class="sxs-lookup"><span data-stu-id="81c0a-p102">Determines the line weight of a shape. Set the line weight by entering a number with a valid unit of measure.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81c0a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="81c0a-107">Remarks</span></span>

<span data-ttu-id="81c0a-108">Você também pode definir o valor da célula LineWeight na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e, em seguida, clique em **Mais linhas**).</span><span class="sxs-lookup"><span data-stu-id="81c0a-108">You can also set the value of LineWeight in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="81c0a-109">Se a unidade de medida não for inserida, a unidade de medida de texto especificado na caixa de diálogo **Opções do Visio** é usada (clique na guia **arquivo** e, em seguida, clique em **Opções**).</span><span class="sxs-lookup"><span data-stu-id="81c0a-109">If the unit of measure is not entered, the unit of measure for text specified in the **Visio Options** dialog box is used (click the **File** tab, and then click **Options**).</span></span> <span data-ttu-id="81c0a-110">Espessura da linha é independente da escala do desenho.</span><span class="sxs-lookup"><span data-stu-id="81c0a-110">Line weight is independent of the scale of the drawing.</span></span> <span data-ttu-id="81c0a-111">Se o desenho estiver em escala, a espessura da linha permanece o mesmo.</span><span class="sxs-lookup"><span data-stu-id="81c0a-111">If the drawing is scaled, the line weight remains the same.</span></span> 
  
<span data-ttu-id="81c0a-112">Para obter uma referência à célula LineWeight pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="81c0a-112">To get a reference to the LineWeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81c0a-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="81c0a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="81c0a-114">LineWeight</span><span class="sxs-lookup"><span data-stu-id="81c0a-114">LineWeight</span></span>  <br/> |
   
<span data-ttu-id="81c0a-115">Para obter uma referência à célula LineWeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="81c0a-115">To get a reference to the LineWeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="81c0a-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="81c0a-116">Section index:</span></span>  <br/> |<span data-ttu-id="81c0a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81c0a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="81c0a-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="81c0a-118">Row index:</span></span>  <br/> |<span data-ttu-id="81c0a-119">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="81c0a-119">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="81c0a-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="81c0a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="81c0a-121">**visLineWeight**</span><span class="sxs-lookup"><span data-stu-id="81c0a-121">**visLineWeight**</span></span> <br/> |
   

