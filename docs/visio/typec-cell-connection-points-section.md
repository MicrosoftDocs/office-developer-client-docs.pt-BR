---
title: Célula Type / C (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Determina o tipo de ponto de conexão.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415233"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="26bef-103">Célula Type / C (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="26bef-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="26bef-104">Determina o tipo de ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="26bef-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="26bef-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26bef-105">**Value**</span></span>|<span data-ttu-id="26bef-106">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26bef-106">**Type**</span></span>|<span data-ttu-id="26bef-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="26bef-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26bef-108">,0</span><span class="sxs-lookup"><span data-stu-id="26bef-108">0</span></span>  <br/> |<span data-ttu-id="26bef-109">Cilindro</span><span class="sxs-lookup"><span data-stu-id="26bef-109">Inward</span></span>  <br/> |<span data-ttu-id="26bef-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="26bef-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="26bef-111">1</span><span class="sxs-lookup"><span data-stu-id="26bef-111">1</span></span>  <br/> |<span data-ttu-id="26bef-112">Para fora</span><span class="sxs-lookup"><span data-stu-id="26bef-112">Outward</span></span>  <br/> |<span data-ttu-id="26bef-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="26bef-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="26bef-114">duas</span><span class="sxs-lookup"><span data-stu-id="26bef-114">2</span></span>  <br/> |<span data-ttu-id="26bef-115">Para &amp; fora</span><span class="sxs-lookup"><span data-stu-id="26bef-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="26bef-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="26bef-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26bef-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="26bef-117">Remarks</span></span>

<span data-ttu-id="26bef-p101">Também é possível definir o tipo de ponto de conexão escolhendo a ferramenta **Conector**, selecionando uma forma e clicando com o botão direito do mouse em um ponto de conexão. Para fazer isso, você precisa executar no modo do [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md).</span><span class="sxs-lookup"><span data-stu-id="26bef-p101">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point. To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="26bef-120">Para obter uma referência para a célula Type / C pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="26bef-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26bef-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="26bef-121">Cell name:</span></span>  <br/> |<span data-ttu-id="26bef-122">Connections. Type [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="26bef-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="26bef-123">Para obter uma referência para a célula Type / C pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="26bef-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26bef-124">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="26bef-124">Section index:</span></span>  <br/> |<span data-ttu-id="26bef-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="26bef-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="26bef-126">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="26bef-126">Row index:</span></span>  <br/> |<span data-ttu-id="26bef-127">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="26bef-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="26bef-128">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="26bef-128">Cell index:</span></span>  <br/> |<span data-ttu-id="26bef-129">**visCnnctType** (linhas não estendidas) **visCnnctC** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="26bef-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="26bef-130">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="26bef-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

