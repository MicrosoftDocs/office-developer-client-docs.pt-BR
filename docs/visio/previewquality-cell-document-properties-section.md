---
title: Célula PreviewQuality (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Determina se a visualização do desenho é um rascunho ou detalhada.
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772576"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="15294-103">Célula PreviewQuality (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="15294-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="15294-104">Determina se a visualização do desenho é um rascunho ou detalhada.</span><span class="sxs-lookup"><span data-stu-id="15294-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="15294-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="15294-105">**Value**</span></span>|<span data-ttu-id="15294-106">**Qualidade de visualização**</span><span class="sxs-lookup"><span data-stu-id="15294-106">**Preview quality**</span></span>|<span data-ttu-id="15294-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="15294-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="15294-108">0</span><span class="sxs-lookup"><span data-stu-id="15294-108">0</span></span>  <br/> | <span data-ttu-id="15294-109">Rascunho</span><span class="sxs-lookup"><span data-stu-id="15294-109">Draft</span></span>  <br/> |<span data-ttu-id="15294-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="15294-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="15294-111">1</span><span class="sxs-lookup"><span data-stu-id="15294-111">1</span></span>  <br/> | <span data-ttu-id="15294-112">Detalhada</span><span class="sxs-lookup"><span data-stu-id="15294-112">Detailed</span></span>  <br/> |<span data-ttu-id="15294-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="15294-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15294-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="15294-114">Remarks</span></span>

<span data-ttu-id="15294-115">Você também pode definir esse valor na guia **Resumo** na caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , clique em **Propriedades do documento**e, em seguida, clique em **Propriedades avançadas**).</span><span class="sxs-lookup"><span data-stu-id="15294-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="15294-116">Para obter uma referência para a célula PreviewQuality pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="15294-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15294-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="15294-117">Cell name:</span></span>  <br/> | <span data-ttu-id="15294-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="15294-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="15294-119">Para obter uma referência para a célula PreviewQuality pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="15294-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="15294-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="15294-120">Section index:</span></span>  <br/> |<span data-ttu-id="15294-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="15294-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="15294-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="15294-122">Row index:</span></span>  <br/> |<span data-ttu-id="15294-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="15294-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="15294-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="15294-124">Cell index:</span></span>  <br/> |<span data-ttu-id="15294-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="15294-125">**visDocPreviewQuality**</span></span> <br/> |
   

