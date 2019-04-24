---
title: Célula ViewMarkup (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Determina se a marcação é exibida na janela de desenho.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355822"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="23bcf-103">Célula ViewMarkup (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="23bcf-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="23bcf-104">Determina se a marcação é exibida na janela de desenho.</span><span class="sxs-lookup"><span data-stu-id="23bcf-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="23bcf-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="23bcf-105">**Value**</span></span>|<span data-ttu-id="23bcf-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23bcf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23bcf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="23bcf-107">TRUE</span></span>  <br/> |<span data-ttu-id="23bcf-108">A marcação é exibida no desenho.</span><span class="sxs-lookup"><span data-stu-id="23bcf-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="23bcf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="23bcf-109">FALSE</span></span>  <br/> |<span data-ttu-id="23bcf-110">A marcação não é exibida (o padrão).</span><span class="sxs-lookup"><span data-stu-id="23bcf-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23bcf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="23bcf-111">Remarks</span></span>

 <span data-ttu-id="23bcf-112">Quando o rastreamento de marcação está ativado (a célula addMarkup é TRUE), a célula ViewMarkup é definida automaticamente como TRUE e permanece TRUE, mesmo após o rastreamento de marcação ter sido desativado (a célula addMarkup é FALSE).</span><span class="sxs-lookup"><span data-stu-id="23bcf-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="23bcf-113">O valor da célula ViewMarkup é ignorado quando a célula AddMarkup está definida como VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="23bcf-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="23bcf-114">A célula ViewMarkup também é definida como VERDADEIRO quando são inseridos comentários em um desenho (independente de o rastreamento de marcação estar ativado ou não) e precisa ser VERDADEIRO para que os comentários sejam exibidos no desenho.</span><span class="sxs-lookup"><span data-stu-id="23bcf-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="23bcf-115">Essa célula corresponde à configuração de comando **Mostrar Marcação** no grupo **Marcação** na guia **Revisão**.</span><span class="sxs-lookup"><span data-stu-id="23bcf-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="23bcf-116">Para obter uma referência à célula ViewMarkup pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="23bcf-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23bcf-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="23bcf-117">Cell name:</span></span>  <br/> |<span data-ttu-id="23bcf-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="23bcf-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="23bcf-119">Para obter uma referência para a célula ViewMarkup pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="23bcf-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23bcf-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="23bcf-120">Section index:</span></span>  <br/> |<span data-ttu-id="23bcf-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23bcf-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="23bcf-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="23bcf-122">Row index:</span></span>  <br/> |<span data-ttu-id="23bcf-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="23bcf-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="23bcf-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="23bcf-124">Cell index:</span></span>  <br/> |<span data-ttu-id="23bcf-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="23bcf-125">**visDocViewMarkup**</span></span> <br/> |
   

