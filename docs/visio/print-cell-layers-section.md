---
title: Célula Print (Seção Layers)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Especifica se as formas pertencentes à camada podem ser impressas.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435212"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="f7015-103">Célula Print (Seção Layers)</span><span class="sxs-lookup"><span data-stu-id="f7015-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="f7015-104">Especifica se as formas pertencentes à camada podem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="f7015-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="f7015-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f7015-105">**Value**</span></span>|<span data-ttu-id="f7015-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f7015-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7015-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="f7015-107">TRUE</span></span>  <br/> |<span data-ttu-id="f7015-108">As formas podem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="f7015-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="f7015-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f7015-109">FALSE</span></span>  <br/> |<span data-ttu-id="f7015-110">As formas não podem ser impressas.</span><span class="sxs-lookup"><span data-stu-id="f7015-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7015-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7015-111">Remarks</span></span>

<span data-ttu-id="f7015-112">Também é possível definir esse valor usando a opção **Imprimir** na caixa de diálogo **Propriedades da Camada** (na guia **Página Inicial** no grupo **Edição** clique em **Camadas** e em **Propriedades da Camada**).</span><span class="sxs-lookup"><span data-stu-id="f7015-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="f7015-113">Para obter uma referência para a célula Print pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f7015-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7015-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f7015-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f7015-115">Layers.Print[ *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f7015-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f7015-116">Para obter uma referência para a célula Print pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f7015-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7015-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f7015-117">Section index:</span></span>  <br/> |<span data-ttu-id="f7015-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="f7015-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="f7015-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f7015-119">Row index:</span></span>  <br/> |<span data-ttu-id="f7015-120">**visRowLayer**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f7015-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f7015-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="f7015-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f7015-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="f7015-122">**visDocPreviewScope**</span></span> <br/> |
   

