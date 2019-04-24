---
title: Célula Flags (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: 'Indica a direção do texto: da esquerda para a direita ou vice-versa.'
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346218"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="e3531-103">Célula Flags (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="e3531-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="e3531-104">Indica a direção do texto: da esquerda para a direita ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="e3531-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="e3531-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e3531-105">**Value**</span></span>|<span data-ttu-id="e3531-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e3531-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3531-107">,0</span><span class="sxs-lookup"><span data-stu-id="e3531-107">0</span></span>  <br/> |<span data-ttu-id="e3531-108">A direção do texto é da esquerda para a direita (o padrão).</span><span class="sxs-lookup"><span data-stu-id="e3531-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="e3531-109">1</span><span class="sxs-lookup"><span data-stu-id="e3531-109">1</span></span>  <br/> |<span data-ttu-id="e3531-110">A direção do texto é da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="e3531-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3531-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3531-111">Remarks</span></span>

<span data-ttu-id="e3531-112">O valor desta célula corresponde à configuração de **direção** da guia **parágrafo** da caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ), que aparece somente se um idioma que usa o texto de scripts complexos tiver sido adicionado na caixa de diálogo **preferências de idioma do Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="e3531-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="e3531-113">(Clique em **Iniciar**, **todos os programas**, **Microsoft Office**, **Ferramentas do Microsoft Office**e, em seguida, em preferências de **idioma do Microsoft Office**.)</span><span class="sxs-lookup"><span data-stu-id="e3531-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="e3531-114">Para obter uma referência para a célula Flags pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e3531-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3531-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e3531-115">Cell name:</span></span>  <br/> |<span data-ttu-id="e3531-116">Para. Flags [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e3531-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e3531-117">Para obter uma referência para a célula Flags pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e3531-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3531-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e3531-118">Section index:</span></span>  <br/> |<span data-ttu-id="e3531-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="e3531-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="e3531-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e3531-120">Row index:</span></span>  <br/> |<span data-ttu-id="e3531-121">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3531-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e3531-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e3531-122">Cell index:</span></span>  <br/> |<span data-ttu-id="e3531-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="e3531-123">**visFlags**</span></span> <br/> |
   

