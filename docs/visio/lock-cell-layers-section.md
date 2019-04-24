---
title: Célula Lock (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Especifica se as formas pertencentes à camada estão protegidas contra seleção ou edição.
ms.openlocfilehash: d548a6f0fe0cac10d80d73c904739b2979ecf27f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359679"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="20e6c-103">Célula Lock (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="20e6c-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="20e6c-104">Especifica se as formas pertencentes à camada estão protegidas contra seleção ou edição.</span><span class="sxs-lookup"><span data-stu-id="20e6c-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="20e6c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="20e6c-105">**Value**</span></span>|<span data-ttu-id="20e6c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20e6c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20e6c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="20e6c-107">TRUE</span></span>  <br/> |<span data-ttu-id="20e6c-108">As formas estão protegidas.</span><span class="sxs-lookup"><span data-stu-id="20e6c-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="20e6c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="20e6c-109">FALSE</span></span>  <br/> |<span data-ttu-id="20e6c-110">As formas não estão protegidas.</span><span class="sxs-lookup"><span data-stu-id="20e6c-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20e6c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="20e6c-111">Remarks</span></span>

<span data-ttu-id="20e6c-112">Também é possível definir esse valor selecionando a opção **Bloquear** na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial** no grupo **Edição** clique em **Camadas** e em **Propriedades da Camada**).</span><span class="sxs-lookup"><span data-stu-id="20e6c-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="20e6c-113">Para obter uma referência para a célula Lock pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="20e6c-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20e6c-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="20e6c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="20e6c-115">Layers. Locked [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="20e6c-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="20e6c-116">Para obter uma referência para a célula Lock pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="20e6c-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20e6c-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="20e6c-117">Section index:</span></span>  <br/> |<span data-ttu-id="20e6c-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="20e6c-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="20e6c-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="20e6c-119">Row index:</span></span>  <br/> |<span data-ttu-id="20e6c-120">**visRowLayer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="20e6c-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="20e6c-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="20e6c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="20e6c-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="20e6c-122">**visLayerLock**</span></span> <br/> |
   

