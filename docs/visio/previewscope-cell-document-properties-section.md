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
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426503"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="6cf08-104">Célula PreviewScope (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="6cf08-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="6cf08-p102">Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.</span><span class="sxs-lookup"><span data-stu-id="6cf08-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="6cf08-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6cf08-107">**Value**</span></span>|<span data-ttu-id="6cf08-108">**Escopo de visualização**</span><span class="sxs-lookup"><span data-stu-id="6cf08-108">**Preview scope**</span></span>|<span data-ttu-id="6cf08-109">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="6cf08-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6cf08-110">,0</span><span class="sxs-lookup"><span data-stu-id="6cf08-110">0</span></span>  <br/> | <span data-ttu-id="6cf08-111">Primeira página</span><span class="sxs-lookup"><span data-stu-id="6cf08-111">First page</span></span>  <br/> |<span data-ttu-id="6cf08-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="6cf08-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="6cf08-113">1</span><span class="sxs-lookup"><span data-stu-id="6cf08-113">1</span></span>  <br/> | <span data-ttu-id="6cf08-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6cf08-114">None</span></span>  <br/> |<span data-ttu-id="6cf08-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="6cf08-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="6cf08-116">duas</span><span class="sxs-lookup"><span data-stu-id="6cf08-116">2</span></span>  <br/> | <span data-ttu-id="6cf08-117">Todas as páginas</span><span class="sxs-lookup"><span data-stu-id="6cf08-117">All pages</span></span>  <br/> |<span data-ttu-id="6cf08-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="6cf08-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cf08-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cf08-119">Remarks</span></span>

<span data-ttu-id="6cf08-120">Você também pode definir esse valor na guia **Resumo** da caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , em **Propriedades do documento**e em **Propriedades avançadas**).</span><span class="sxs-lookup"><span data-stu-id="6cf08-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="6cf08-121">Para obter uma referência para a célula PreviewScope pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6cf08-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6cf08-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6cf08-122">Cell name:</span></span>  <br/> | <span data-ttu-id="6cf08-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="6cf08-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="6cf08-124">Para obter uma referência para a célula PreviewScope pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6cf08-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6cf08-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6cf08-125">Section index:</span></span>  <br/> |<span data-ttu-id="6cf08-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6cf08-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6cf08-127">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6cf08-127">Row index:</span></span>  <br/> |<span data-ttu-id="6cf08-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="6cf08-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="6cf08-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6cf08-129">Cell index:</span></span>  <br/> |<span data-ttu-id="6cf08-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="6cf08-130">**visDocPreviewScope**</span></span> <br/> |
   

