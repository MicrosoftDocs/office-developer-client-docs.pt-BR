---
title: Célula AddMarkup (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Indica se as marcações do documento estão sendo revisadas.
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338630"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="d0334-103">Célula AddMarkup (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="d0334-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="d0334-104">Indica se as marcações do documento estão sendo revisadas.</span><span class="sxs-lookup"><span data-stu-id="d0334-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="d0334-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d0334-105">**Value**</span></span>|<span data-ttu-id="d0334-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d0334-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0334-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d0334-107">TRUE</span></span>  <br/> |<span data-ttu-id="d0334-108">O documento está sendo revisado.</span><span class="sxs-lookup"><span data-stu-id="d0334-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="d0334-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d0334-109">FALSE</span></span>  <br/> |<span data-ttu-id="d0334-110">O documento não está sendo revisado (o padrão).</span><span class="sxs-lookup"><span data-stu-id="d0334-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0334-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0334-111">Remarks</span></span>

<span data-ttu-id="d0334-112">Quando a célula AddMarkup está definida como VERDADEIRO, o revisor está adicionando marcações e as alterações são aplicadas às páginas de sobreposição de marcação, e não às páginas de desenho originais.</span><span class="sxs-lookup"><span data-stu-id="d0334-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="d0334-113">Quando a célula AddMarkup está definida como FALSO, o controle de marcação está desativado e as alterações são aplicadas às páginas de desenho originais.</span><span class="sxs-lookup"><span data-stu-id="d0334-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d0334-114">Você pode impedir a marcação em seus documentos usando a função GUARD.</span><span class="sxs-lookup"><span data-stu-id="d0334-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="d0334-115">Se a célula addMarkup contiver a fórmula = GUARD (FALSE), o comando **rastrear marcação** será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d0334-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="d0334-116">Essa configuração corresponde à configuração de comando **Rastrear Marcação** no grupo **Marcação** na guia **Revisão**.</span><span class="sxs-lookup"><span data-stu-id="d0334-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="d0334-117">Para fazer referência à célula AddMarkup pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d0334-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0334-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d0334-118">Cell name:</span></span>  <br/> |<span data-ttu-id="d0334-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="d0334-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="d0334-120">Para fazer referência à célula AddMarkup pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d0334-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0334-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d0334-121">Section index:</span></span>  <br/> |<span data-ttu-id="d0334-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d0334-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d0334-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d0334-123">Row index:</span></span>  <br/> |<span data-ttu-id="d0334-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="d0334-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="d0334-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d0334-125">Cell index:</span></span>  <br/> |<span data-ttu-id="d0334-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="d0334-126">**visDocAddMarkup**</span></span> <br/> |
   

