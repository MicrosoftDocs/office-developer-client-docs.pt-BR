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
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356032"
---
# <a name="previewquality-cell-document-properties-section"></a><span data-ttu-id="e86a5-103">Célula PreviewQuality (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="e86a5-103">PreviewQuality Cell (Document Properties Section)</span></span>

<span data-ttu-id="e86a5-104">Determina se a visualização do desenho é um rascunho ou detalhada.</span><span class="sxs-lookup"><span data-stu-id="e86a5-104">Determines whether the drawing preview is draft quality or detailed.</span></span>
  
|<span data-ttu-id="e86a5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e86a5-105">**Value**</span></span>|<span data-ttu-id="e86a5-106">**Qualidade de visualização**</span><span class="sxs-lookup"><span data-stu-id="e86a5-106">**Preview quality**</span></span>|<span data-ttu-id="e86a5-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e86a5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e86a5-108">,0</span><span class="sxs-lookup"><span data-stu-id="e86a5-108">0</span></span>  <br/> | <span data-ttu-id="e86a5-109">Rascunho</span><span class="sxs-lookup"><span data-stu-id="e86a5-109">Draft</span></span>  <br/> |<span data-ttu-id="e86a5-110">**visDocPreviewQualityDraft**</span><span class="sxs-lookup"><span data-stu-id="e86a5-110">**visDocPreviewQualityDraft**</span></span> <br/> |
| <span data-ttu-id="e86a5-111">1</span><span class="sxs-lookup"><span data-stu-id="e86a5-111">1</span></span>  <br/> | <span data-ttu-id="e86a5-112">Análise</span><span class="sxs-lookup"><span data-stu-id="e86a5-112">Detailed</span></span>  <br/> |<span data-ttu-id="e86a5-113">**visDocPreviewQualityDetailed**</span><span class="sxs-lookup"><span data-stu-id="e86a5-113">**visDocPreviewQualityDetailed**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e86a5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e86a5-114">Remarks</span></span>

<span data-ttu-id="e86a5-115">Você também pode definir esse valor na guia **Resumo** da caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , em **Propriedades do documento**e em **Propriedades avançadas**).</span><span class="sxs-lookup"><span data-stu-id="e86a5-115">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="e86a5-116">Para obter uma referência para a célula PreviewQuality pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e86a5-116">To get a reference to the PreviewQuality cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e86a5-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e86a5-117">Cell name:</span></span>  <br/> | <span data-ttu-id="e86a5-118">PreviewQuality</span><span class="sxs-lookup"><span data-stu-id="e86a5-118">PreviewQuality</span></span>  <br/> |
   
<span data-ttu-id="e86a5-119">Para obter uma referência para a célula PreviewQuality pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e86a5-119">To get a reference to the PreviewQuality cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e86a5-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e86a5-120">Section index:</span></span>  <br/> |<span data-ttu-id="e86a5-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e86a5-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e86a5-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e86a5-122">Row index:</span></span>  <br/> |<span data-ttu-id="e86a5-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="e86a5-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="e86a5-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e86a5-124">Cell index:</span></span>  <br/> |<span data-ttu-id="e86a5-125">**visDocPreviewQuality**</span><span class="sxs-lookup"><span data-stu-id="e86a5-125">**visDocPreviewQuality**</span></span> <br/> |
   

