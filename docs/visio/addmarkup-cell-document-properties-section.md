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
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771268"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="678bf-103">Célula AddMarkup (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="678bf-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="678bf-104">Indica se as marcações do documento estão sendo revisadas.</span><span class="sxs-lookup"><span data-stu-id="678bf-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="678bf-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="678bf-105">**Value**</span></span>|<span data-ttu-id="678bf-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="678bf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="678bf-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="678bf-107">TRUE</span></span>  <br/> |<span data-ttu-id="678bf-108">O documento está sendo revisado.</span><span class="sxs-lookup"><span data-stu-id="678bf-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="678bf-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="678bf-109">FALSE</span></span>  <br/> |<span data-ttu-id="678bf-110">O documento não está sendo revisado (o padrão).</span><span class="sxs-lookup"><span data-stu-id="678bf-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="678bf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="678bf-111">Remarks</span></span>

<span data-ttu-id="678bf-112">Quando a célula AddMarkup está definida como TRUE, o revisor está adicionando marcações e as alterações são aplicadas às páginas de sobreposição de marcação, não às páginas de desenho originais.</span><span class="sxs-lookup"><span data-stu-id="678bf-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="678bf-113">Quando a célula AddMarkup é FALSE, o rastreamento de marcação está desativado e as alterações são aplicadas a páginas do desenho originais.</span><span class="sxs-lookup"><span data-stu-id="678bf-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="678bf-114">Você pode impedir a marcação em seus documentos usando a função GUARD.</span><span class="sxs-lookup"><span data-stu-id="678bf-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="678bf-115">Se a célula AddMarkup contém a fórmula = Guard (FALSO), o comando **Rastrear Marcação** está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="678bf-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="678bf-116">Essa configuração corresponde à configuração de comando **Rastrear Marcação** no grupo **marcação** na guia **revisão** .</span><span class="sxs-lookup"><span data-stu-id="678bf-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="678bf-117">Para obter uma referência à célula AddMarkup pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="678bf-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="678bf-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="678bf-118">Cell name:</span></span>  <br/> |<span data-ttu-id="678bf-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="678bf-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="678bf-120">Para obter uma referência à célula AddMarkup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="678bf-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="678bf-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="678bf-121">Section index:</span></span>  <br/> |<span data-ttu-id="678bf-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="678bf-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="678bf-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="678bf-123">Row index:</span></span>  <br/> |<span data-ttu-id="678bf-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="678bf-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="678bf-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="678bf-125">Cell index:</span></span>  <br/> |<span data-ttu-id="678bf-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="678bf-126">**visDocAddMarkup**</span></span> <br/> |
   

