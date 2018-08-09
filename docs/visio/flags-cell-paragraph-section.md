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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771879"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="f8f1d-103">Célula Flags (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="f8f1d-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="f8f1d-104">Indica a direção do texto: da esquerda para a direita ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="f8f1d-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="f8f1d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-105">**Value**</span></span>|<span data-ttu-id="f8f1d-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8f1d-107">0</span><span class="sxs-lookup"><span data-stu-id="f8f1d-107">0</span></span>  <br/> |<span data-ttu-id="f8f1d-108">A direção do texto é da esquerda para a direita (o padrão).</span><span class="sxs-lookup"><span data-stu-id="f8f1d-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="f8f1d-109">1</span><span class="sxs-lookup"><span data-stu-id="f8f1d-109">1</span></span>  <br/> |<span data-ttu-id="f8f1d-110">A direção do texto é da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="f8f1d-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8f1d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8f1d-111">Remarks</span></span>

<span data-ttu-id="f8f1d-112">O valor desta célula corresponde à configuração **direção** na guia **parágrafo** na caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ), que aparecerá somente se o texto de um idioma que usa um complexo scripts ficou adicionada na caixa de diálogo **Preferências de idioma do Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="f8f1d-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="f8f1d-113">(Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.)</span><span class="sxs-lookup"><span data-stu-id="f8f1d-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="f8f1d-114">Para obter uma referência para a célula Flags pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f8f1d-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8f1d-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f8f1d-115">Cell name:</span></span>  <br/> |<span data-ttu-id="f8f1d-116">Para.Flags [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f8f1d-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f8f1d-117">Para obter uma referência para a célula Flags pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f8f1d-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8f1d-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f8f1d-118">Section index:</span></span>  <br/> |<span data-ttu-id="f8f1d-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="f8f1d-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f8f1d-120">Row index:</span></span>  <br/> |<span data-ttu-id="f8f1d-121">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f8f1d-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f8f1d-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f8f1d-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f8f1d-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="f8f1d-123">**visFlags**</span></span> <br/> |
   

