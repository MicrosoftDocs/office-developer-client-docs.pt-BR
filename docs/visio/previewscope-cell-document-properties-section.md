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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356109"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="30a1c-104">Célula PreviewScope (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="30a1c-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="30a1c-p102">Determina se o desenho conterá uma visualização. Se o seu desenho contiver uma visualização, ela determinará se irá exibir somente a primeira página ou todas as páginas do desenho.</span><span class="sxs-lookup"><span data-stu-id="30a1c-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="30a1c-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="30a1c-107">**Value**</span></span>|<span data-ttu-id="30a1c-108">**Escopo de visualização**</span><span class="sxs-lookup"><span data-stu-id="30a1c-108">**Preview scope**</span></span>|<span data-ttu-id="30a1c-109">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="30a1c-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="30a1c-110">,0</span><span class="sxs-lookup"><span data-stu-id="30a1c-110">0</span></span>  <br/> | <span data-ttu-id="30a1c-111">Primeira página</span><span class="sxs-lookup"><span data-stu-id="30a1c-111">First page</span></span>  <br/> |<span data-ttu-id="30a1c-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="30a1c-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="30a1c-113">1</span><span class="sxs-lookup"><span data-stu-id="30a1c-113">1</span></span>  <br/> | <span data-ttu-id="30a1c-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="30a1c-114">None</span></span>  <br/> |<span data-ttu-id="30a1c-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="30a1c-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="30a1c-116">duas</span><span class="sxs-lookup"><span data-stu-id="30a1c-116">2</span></span>  <br/> | <span data-ttu-id="30a1c-117">Todas as páginas</span><span class="sxs-lookup"><span data-stu-id="30a1c-117">All pages</span></span>  <br/> |<span data-ttu-id="30a1c-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="30a1c-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30a1c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="30a1c-119">Remarks</span></span>

<span data-ttu-id="30a1c-120">Você também pode definir esse valor na guia **Resumo** da caixa de diálogo **Propriedades** (clique no botão **Office** , clique na guia **informações** , em **Propriedades do documento**e em **Propriedades avançadas**).</span><span class="sxs-lookup"><span data-stu-id="30a1c-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="30a1c-121">Para obter uma referência para a célula PreviewScope pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="30a1c-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30a1c-122">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="30a1c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="30a1c-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="30a1c-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="30a1c-124">Para obter uma referência para a célula PreviewScope pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="30a1c-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="30a1c-125">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="30a1c-125">Section index:</span></span>  <br/> |<span data-ttu-id="30a1c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30a1c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="30a1c-127">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="30a1c-127">Row index:</span></span>  <br/> |<span data-ttu-id="30a1c-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="30a1c-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="30a1c-129">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="30a1c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="30a1c-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="30a1c-130">**visDocPreviewScope**</span></span> <br/> |
   

