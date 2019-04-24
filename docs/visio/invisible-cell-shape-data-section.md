---
title: Célula Invisible (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Especifica se o item de dados de forma ficará visível na janela Dados da Forma.
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357264"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="2a48e-103">Célula Invisible (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="2a48e-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="2a48e-104">Especifica se o item de dados da forma será visível na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="2a48e-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="2a48e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2a48e-105">**Value**</span></span>|<span data-ttu-id="2a48e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2a48e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2a48e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2a48e-107">TRUE</span></span>  <br/> | <span data-ttu-id="2a48e-108">O item de dados da forma não é visível.</span><span class="sxs-lookup"><span data-stu-id="2a48e-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="2a48e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2a48e-109">FALSE</span></span>  <br/> | <span data-ttu-id="2a48e-110">O item de dados da forma é visível.</span><span class="sxs-lookup"><span data-stu-id="2a48e-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a48e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a48e-111">Remarks</span></span>

<span data-ttu-id="2a48e-112">O valor desta célula corresponde à caixa de seleção **Oculto** da caixa de diálogo **Definir Dados da Forma** (Clique com o botão direito do mouse na forma, aponte para **Dados** e clique em **Definir Dados da Forma**).</span><span class="sxs-lookup"><span data-stu-id="2a48e-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="2a48e-113">Para obter uma referência para a célula Invisible pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2a48e-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a48e-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2a48e-114">Cell name:</span></span>  <br/> | <span data-ttu-id="2a48e-115">Hélice.  *nome* . Invisível onde prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="2a48e-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2a48e-116">Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2a48e-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a48e-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2a48e-117">Section index:</span></span>  <br/> |<span data-ttu-id="2a48e-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="2a48e-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="2a48e-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2a48e-119">Row index:</span></span>  <br/> |<span data-ttu-id="2a48e-120">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2a48e-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2a48e-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2a48e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="2a48e-122">**visCustPropsInvis**</span><span class="sxs-lookup"><span data-stu-id="2a48e-122">**visCustPropsInvis**</span></span> <br/> |
   

