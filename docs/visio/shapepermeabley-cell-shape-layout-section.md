---
title: Célula ShapePermeableY (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Determina se um conector pode fazer o roteamento verticalmente por uma forma.
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417515"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="37837-103">Célula ShapePermeableY (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="37837-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="37837-104">Determina se um conector pode fazer o roteamento verticalmente por uma forma.</span><span class="sxs-lookup"><span data-stu-id="37837-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="37837-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="37837-105">**Value**</span></span>|<span data-ttu-id="37837-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37837-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37837-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="37837-107">TRUE</span></span>  <br/> |<span data-ttu-id="37837-108">Permitir que os conectores façam o roteamento verticalmente por uma forma.</span><span class="sxs-lookup"><span data-stu-id="37837-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="37837-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="37837-109">FALSE</span></span>  <br/> |<span data-ttu-id="37837-110">Não permitir que os conectores façam o roteamento verticalmente por uma forma.</span><span class="sxs-lookup"><span data-stu-id="37837-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37837-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="37837-111">Remarks</span></span>

<span data-ttu-id="37837-112">Você também pode definir o valor dessa célula  na guia Posicionamento na caixa [](run-in-developer-mode-display-the-developer-tab.md) de diálogo Comportamento (com uma forma selecionada,  na guia Desenvolvedor, no grupo **Design** da Forma, clique em Comportamento e na guia Posicionamento).  </span><span class="sxs-lookup"><span data-stu-id="37837-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="37837-113">Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="37837-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="37837-114">Para obter uma referência para a célula ShapePermeableY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="37837-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37837-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="37837-115">Cell name:</span></span>  <br/> |<span data-ttu-id="37837-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="37837-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="37837-117">Para obter uma referência para a célula ShapePermeableY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="37837-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37837-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="37837-118">Section index:</span></span>  <br/> |<span data-ttu-id="37837-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37837-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="37837-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="37837-120">Row index:</span></span>  <br/> |<span data-ttu-id="37837-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="37837-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="37837-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="37837-122">Cell index:</span></span>  <br/> |<span data-ttu-id="37837-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="37837-123">**visSLOPermY**</span></span> <br/> |
   

