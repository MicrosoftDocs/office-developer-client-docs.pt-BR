---
title: Célula LocalizeMerge (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Determina se as formas são localizadas quando copiadas entre documentos.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772222"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="d3340-103">Célula LocalizeMerge (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="d3340-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="d3340-104">Determina se as formas são localizadas quando copiadas entre documentos.</span><span class="sxs-lookup"><span data-stu-id="d3340-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="d3340-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3340-105">**Value**</span></span>|<span data-ttu-id="d3340-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d3340-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d3340-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="d3340-107">TRUE</span></span>  <br/> | <span data-ttu-id="d3340-108">Localiza uma forma para o idioma do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="d3340-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="d3340-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="d3340-109">FALSE</span></span>  <br/> | <span data-ttu-id="d3340-110">Não localiza uma forma com base no idioma do documento de destino (o padrão).</span><span class="sxs-lookup"><span data-stu-id="d3340-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3340-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3340-111">Remarks</span></span>

<span data-ttu-id="d3340-112">Para fazer referência à célula LocalizeMerge pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d3340-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3340-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d3340-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d3340-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="d3340-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="d3340-115">Para fazer referência à célula LocalizeMerge pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d3340-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3340-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d3340-116">Section index:</span></span>  <br/> |<span data-ttu-id="d3340-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3340-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d3340-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d3340-118">Row index:</span></span>  <br/> |<span data-ttu-id="d3340-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="d3340-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="d3340-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d3340-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d3340-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="d3340-121">**visObjLocalizeMerge**</span></span> <br/> |
   

