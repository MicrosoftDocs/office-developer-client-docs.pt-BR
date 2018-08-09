---
title: Célula PreviewScope (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772590"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="75959-104">Célula PreviewScope (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="75959-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="75959-p102">Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.</span><span class="sxs-lookup"><span data-stu-id="75959-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="75959-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="75959-107">**Value**</span></span>|<span data-ttu-id="75959-108">**Escopo de visualização**</span><span class="sxs-lookup"><span data-stu-id="75959-108">**Preview scope**</span></span>|<span data-ttu-id="75959-109">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="75959-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="75959-110">0</span><span class="sxs-lookup"><span data-stu-id="75959-110">0</span></span>  <br/> | <span data-ttu-id="75959-111">Primeira página</span><span class="sxs-lookup"><span data-stu-id="75959-111">First page</span></span>  <br/> |<span data-ttu-id="75959-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="75959-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="75959-113">1</span><span class="sxs-lookup"><span data-stu-id="75959-113">1</span></span>  <br/> | <span data-ttu-id="75959-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="75959-114">None</span></span>  <br/> |<span data-ttu-id="75959-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="75959-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="75959-116">2</span><span class="sxs-lookup"><span data-stu-id="75959-116">2</span></span>  <br/> | <span data-ttu-id="75959-117">Todas as páginas</span><span class="sxs-lookup"><span data-stu-id="75959-117">All pages</span></span>  <br/> |<span data-ttu-id="75959-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="75959-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75959-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="75959-119">Remarks</span></span>

<span data-ttu-id="75959-120">Você também pode definir esse valor na guia **Resumo** na caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , clique em **Propriedades do documento**e, em seguida, clique em **Propriedades avançadas**).</span><span class="sxs-lookup"><span data-stu-id="75959-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="75959-121">Para obter uma referência para a célula PreviewScope pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="75959-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75959-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="75959-122">Cell name:</span></span>  <br/> | <span data-ttu-id="75959-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="75959-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="75959-124">Para obter uma referência para a célula PreviewScope pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="75959-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75959-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="75959-125">Section index:</span></span>  <br/> |<span data-ttu-id="75959-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75959-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="75959-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="75959-127">Row index:</span></span>  <br/> |<span data-ttu-id="75959-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="75959-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="75959-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="75959-129">Cell index:</span></span>  <br/> |<span data-ttu-id="75959-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="75959-130">**visDocPreviewScope**</span></span> <br/> |
   

