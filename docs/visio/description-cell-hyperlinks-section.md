---
title: Célula Description (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Representa uma cadeia de caracteres de texto descritivo para um hiperlink.
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771728"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="9cb23-103">Célula Description (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="9cb23-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="9cb23-104">Representa uma cadeia de caracteres de texto descritivo para um hiperlink.</span><span class="sxs-lookup"><span data-stu-id="9cb23-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9cb23-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cb23-105">Remarks</span></span>

<span data-ttu-id="9cb23-106">Utilize esta célula para armazenar comentários sobre o hiperlink; por exemplo, "Link para nosso site de preços na Web".</span><span class="sxs-lookup"><span data-stu-id="9cb23-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing Web site."</span></span>
  
<span data-ttu-id="9cb23-107">Você também pode definir o valor dessa célula na caixa de diálogo **hiperlinks** (clique em **hiperlink** na guia **Inserir** ).</span><span class="sxs-lookup"><span data-stu-id="9cb23-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="9cb23-108">Para fazer referência à célula Description pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="9cb23-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cb23-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9cb23-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9cb23-110">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="9cb23-110">Hyperlink.</span></span>  <span data-ttu-id="9cb23-111">*Nome* . Descrição onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="9cb23-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="9cb23-112">*Nome* é o nome da linha do hiperlink</span><span class="sxs-lookup"><span data-stu-id="9cb23-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="9cb23-113">Para obter uma referência à célula Description pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9cb23-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cb23-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9cb23-114">Section index:</span></span>  <br/> |<span data-ttu-id="9cb23-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="9cb23-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="9cb23-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9cb23-116">Row index:</span></span>  <br/> |<span data-ttu-id="9cb23-117">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9cb23-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9cb23-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9cb23-118">Cell index:</span></span>  <br/> |<span data-ttu-id="9cb23-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="9cb23-119">**visHLinkDescription**</span></span> <br/> |
   

