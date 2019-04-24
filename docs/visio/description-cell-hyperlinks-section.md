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
description: Representa uma cadeia de texto descritiva de um hiperlink.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360239"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="c1558-103">Célula Description (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="c1558-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="c1558-104">Representa uma cadeia de texto descritiva de um hiperlink.</span><span class="sxs-lookup"><span data-stu-id="c1558-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1558-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1558-105">Remarks</span></span>

<span data-ttu-id="c1558-106">Utilize esta célula para armazenar comentários sobre o hiperlink; por exemplo, "Link para nosso site de preços".</span><span class="sxs-lookup"><span data-stu-id="c1558-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="c1558-107">Você também pode definir o valor dessa célula na caixa de diálogo **Hiperlinks** (clique em **Hiperlink** na guia **Inserir**).</span><span class="sxs-lookup"><span data-stu-id="c1558-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="c1558-108">Para obter uma referência à célula Descrição pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="c1558-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1558-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c1558-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c1558-110">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="c1558-110">Hyperlink.</span></span>  <span data-ttu-id="c1558-111">*Name*. Descrição em que Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="c1558-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="c1558-112">*Name* é o nome da linha de hiperlink</span><span class="sxs-lookup"><span data-stu-id="c1558-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="c1558-113">Para obter uma referência à célula Description pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c1558-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1558-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c1558-114">Section index:</span></span>  <br/> |<span data-ttu-id="c1558-115">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="c1558-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="c1558-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c1558-116">Row index:</span></span>  <br/> |<span data-ttu-id="c1558-117">**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c1558-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c1558-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="c1558-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c1558-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="c1558-119">**visHLinkDescription**</span></span> <br/> |
   

