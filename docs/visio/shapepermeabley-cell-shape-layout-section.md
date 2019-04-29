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
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="ea685-103">Célula ShapePermeableY (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="ea685-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ea685-104">Determina se um conector pode fazer o roteamento verticalmente por uma forma.</span><span class="sxs-lookup"><span data-stu-id="ea685-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="ea685-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ea685-105">**Value**</span></span>|<span data-ttu-id="ea685-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ea685-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea685-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="ea685-107">TRUE</span></span>  <br/> |<span data-ttu-id="ea685-108">Permitir que os conectores façam o roteamento verticalmente por uma forma.</span><span class="sxs-lookup"><span data-stu-id="ea685-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="ea685-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ea685-109">FALSE</span></span>  <br/> |<span data-ttu-id="ea685-110">Não permitir que os conectores façam o roteamento verticalmente por uma forma.</span><span class="sxs-lookup"><span data-stu-id="ea685-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea685-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea685-111">Remarks</span></span>

<span data-ttu-id="ea685-112">Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="ea685-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="ea685-113">Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="ea685-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="ea685-114">Para obter uma referência para a célula ShapePermeableY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ea685-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea685-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ea685-115">Cell name:</span></span>  <br/> |<span data-ttu-id="ea685-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="ea685-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="ea685-117">Para obter uma referência para a célula ShapePermeableY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ea685-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ea685-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ea685-118">Section index:</span></span>  <br/> |<span data-ttu-id="ea685-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ea685-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ea685-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ea685-120">Row index:</span></span>  <br/> |<span data-ttu-id="ea685-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ea685-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="ea685-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="ea685-122">Cell index:</span></span>  <br/> |<span data-ttu-id="ea685-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="ea685-123">**visSLOPermY**</span></span> <br/> |
   

