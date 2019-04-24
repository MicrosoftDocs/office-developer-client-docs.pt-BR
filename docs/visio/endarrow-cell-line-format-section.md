---
title: Célula EndArrow (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu último vértice.
ms.openlocfilehash: 54ef11125a8774914a60897850fb75cd4ab949a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328900"
---
# <a name="endarrow-cell-line-format-section"></a><span data-ttu-id="bfd1c-103">Célula EndArrow (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="bfd1c-103">EndArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="bfd1c-104">Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu último vértice.</span><span class="sxs-lookup"><span data-stu-id="bfd1c-104">Indicates whether a line has an arrowhead or other line end format at its last vertex.</span></span>
  
|<span data-ttu-id="bfd1c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bfd1c-105">**Value**</span></span>|<span data-ttu-id="bfd1c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bfd1c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfd1c-107">,0</span><span class="sxs-lookup"><span data-stu-id="bfd1c-107">0</span></span>  <br/> |<span data-ttu-id="bfd1c-108">Sem ponta de seta.</span><span class="sxs-lookup"><span data-stu-id="bfd1c-108">No arrowhead.</span></span>  <br/> |
|<span data-ttu-id="bfd1c-109">1 - 45</span><span class="sxs-lookup"><span data-stu-id="bfd1c-109">1 - 45</span></span>  <br/> |<span data-ttu-id="bfd1c-110">Estilos de ponta de seta variados correspondentes a entradas indexadas na caixa de diálogo **Linha**.</span><span class="sxs-lookup"><span data-stu-id="bfd1c-110">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfd1c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfd1c-111">Remarks</span></span>

<span data-ttu-id="bfd1c-112">Também é possível definir esse valor na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Setas** e em **Mais Setas**).</span><span class="sxs-lookup"><span data-stu-id="bfd1c-112">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Arrows**, and then click **More Arrows**).</span></span> <span data-ttu-id="bfd1c-113">O tamanho da ponta de seta é definido na célula EndArrowSize.</span><span class="sxs-lookup"><span data-stu-id="bfd1c-113">The size of the arrowhead is set in the EndArrowSize cell.</span></span>
  
<span data-ttu-id="bfd1c-114">Você pode especificar um fim de linha personalizado utilizando a função USE nesta célula.</span><span class="sxs-lookup"><span data-stu-id="bfd1c-114">You can specify a custom line end using the USE function in this cell.</span></span> 
  
<span data-ttu-id="bfd1c-115">Para obter uma referência para a célula EndArrow pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="bfd1c-115">To get a reference to the EndArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfd1c-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bfd1c-116">Cell name:</span></span>  <br/> |<span data-ttu-id="bfd1c-117">EndArrow</span><span class="sxs-lookup"><span data-stu-id="bfd1c-117">EndArrow</span></span>  <br/> |
   
<span data-ttu-id="bfd1c-118">Para obter uma referência para a célula EndArrow pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bfd1c-118">To get a reference to the EndArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfd1c-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bfd1c-119">Section index:</span></span>  <br/> |<span data-ttu-id="bfd1c-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bfd1c-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bfd1c-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="bfd1c-121">Row index:</span></span>  <br/> |<span data-ttu-id="bfd1c-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="bfd1c-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="bfd1c-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="bfd1c-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bfd1c-124">**visLineEndArrow**</span><span class="sxs-lookup"><span data-stu-id="bfd1c-124">**visLineEndArrow**</span></span> <br/> |
   

