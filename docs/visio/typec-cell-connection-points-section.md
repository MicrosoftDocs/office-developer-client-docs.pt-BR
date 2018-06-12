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
description: Especifica o tipo de ponto de conexão.
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773200"
---
# <a name="type--c-cell-connection-points-section"></a><span data-ttu-id="97010-103">Célula Type / C (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="97010-103">Type / C Cell (Connection Points Section)</span></span>

<span data-ttu-id="97010-104">Especifica o tipo de ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="97010-104">Determines the connection point type.</span></span>
  
|<span data-ttu-id="97010-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="97010-105">**Value**</span></span>|<span data-ttu-id="97010-106">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="97010-106">**Type**</span></span>|<span data-ttu-id="97010-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="97010-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="97010-108">0</span><span class="sxs-lookup"><span data-stu-id="97010-108">0</span></span>  <br/> |<span data-ttu-id="97010-109">Para dentro</span><span class="sxs-lookup"><span data-stu-id="97010-109">Inward</span></span>  <br/> |<span data-ttu-id="97010-110">**visCnnctTypeInward**</span><span class="sxs-lookup"><span data-stu-id="97010-110">**visCnnctTypeInward**</span></span> <br/> |
|<span data-ttu-id="97010-111">1</span><span class="sxs-lookup"><span data-stu-id="97010-111">1</span></span>  <br/> |<span data-ttu-id="97010-112">Para fora</span><span class="sxs-lookup"><span data-stu-id="97010-112">Outward</span></span>  <br/> |<span data-ttu-id="97010-113">**visCnnctTypeOutward**</span><span class="sxs-lookup"><span data-stu-id="97010-113">**visCnnctTypeOutward**</span></span> <br/> |
|<span data-ttu-id="97010-114">2</span><span class="sxs-lookup"><span data-stu-id="97010-114">2</span></span>  <br/> |<span data-ttu-id="97010-115">DID &amp; para fora</span><span class="sxs-lookup"><span data-stu-id="97010-115">Inward &amp; Outward</span></span>  <br/> |<span data-ttu-id="97010-116">**visCnnctTypeInwardOutward**</span><span class="sxs-lookup"><span data-stu-id="97010-116">**visCnnctTypeInwardOutward**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97010-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="97010-117">Remarks</span></span>

<span data-ttu-id="97010-118">Você também pode definir o tipo de ponto de conexão escolhendo a ferramenta de **conector** , selecionando uma forma e clicando em um ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="97010-118">You can also set the connection point type by choosing the **Connector** tool, selecting a shape, and then right-clicking a connection point.</span></span> <span data-ttu-id="97010-119">Para fazer isso, você precisará executar no modo do [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="97010-119">To do this, you need to run in [developer](run-in-developer-mode-display-the-developer-tab.md) mode.</span></span> 
  
<span data-ttu-id="97010-120">Para obter uma referência para o tipo / C célula pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="97010-120">To get a reference to the Type / C cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97010-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="97010-121">Cell name:</span></span>  <br/> |<span data-ttu-id="97010-122">Connections.Type [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="97010-122">Connections.Type[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="97010-123">Para obter uma referência para o tipo / célula C pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="97010-123">To get a reference to the Type / C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97010-124">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="97010-124">Section index:</span></span>  <br/> |<span data-ttu-id="97010-125">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="97010-125">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="97010-126">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="97010-126">Row index:</span></span>  <br/> |<span data-ttu-id="97010-127">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97010-127">**visRowConnectionPts** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="97010-128">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="97010-128">Cell index:</span></span>  <br/> |<span data-ttu-id="97010-129">**visCnnctType** (linhas não-estendidas) **visCnnctC** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="97010-129">**visCnnctType** (non-extended rows) **visCnnctC** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="97010-130">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="97010-130">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

