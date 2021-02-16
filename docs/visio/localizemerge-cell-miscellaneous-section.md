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
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405671"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="45a59-103">Célula LocalizeMerge (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="45a59-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="45a59-104">Determina se as formas são localizadas quando copiadas entre documentos.</span><span class="sxs-lookup"><span data-stu-id="45a59-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="45a59-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="45a59-105">**Value**</span></span>|<span data-ttu-id="45a59-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="45a59-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="45a59-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="45a59-107">TRUE</span></span>  <br/> | <span data-ttu-id="45a59-108">Localiza uma forma para o idioma do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="45a59-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="45a59-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="45a59-109">FALSE</span></span>  <br/> | <span data-ttu-id="45a59-110">Não localiza uma forma com base no idioma do documento de destino (o padrão).</span><span class="sxs-lookup"><span data-stu-id="45a59-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45a59-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="45a59-111">Remarks</span></span>

<span data-ttu-id="45a59-112">Para fazer referência à célula LocalizeMerge pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="45a59-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45a59-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="45a59-113">Cell name:</span></span>  <br/> | <span data-ttu-id="45a59-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="45a59-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="45a59-115">Para fazer referência à célula LocalizeMerge pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="45a59-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="45a59-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="45a59-116">Section index:</span></span>  <br/> |<span data-ttu-id="45a59-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="45a59-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="45a59-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="45a59-118">Row index:</span></span>  <br/> |<span data-ttu-id="45a59-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="45a59-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="45a59-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="45a59-120">Cell index:</span></span>  <br/> |<span data-ttu-id="45a59-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="45a59-121">**visObjLocalizeMerge**</span></span> <br/> |
   

