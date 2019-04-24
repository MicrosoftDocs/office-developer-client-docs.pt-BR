---
title: Célula TxtPinX (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina a coordenada x do centro de rotação do bloco de texto em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282296"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="aecfd-104">Célula TxtPinX (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="aecfd-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="aecfd-105">Determina a coordenada *x* do centro de rotação do bloco de texto em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="aecfd-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="aecfd-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="aecfd-106">The default formula is:</span></span> 
  
<span data-ttu-id="aecfd-107">= Largura \* 0,5</span><span class="sxs-lookup"><span data-stu-id="aecfd-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aecfd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="aecfd-108">Remarks</span></span>

<span data-ttu-id="aecfd-109">Para fazer referência à célula TxtPinX pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="aecfd-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aecfd-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="aecfd-110">Cell name:</span></span>  <br/> | <span data-ttu-id="aecfd-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="aecfd-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="aecfd-112">Para fazer referência à célula TxtPinX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="aecfd-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aecfd-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="aecfd-113">Section index:</span></span>  <br/> |<span data-ttu-id="aecfd-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aecfd-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aecfd-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="aecfd-115">Row index:</span></span>  <br/> |<span data-ttu-id="aecfd-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="aecfd-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="aecfd-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="aecfd-117">Cell index:</span></span>  <br/> |<span data-ttu-id="aecfd-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="aecfd-118">**visXFormPinX**</span></span> <br/> |
   

