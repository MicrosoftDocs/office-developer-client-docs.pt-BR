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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413112"
---
# <a name="flags-cell-paragraph-section"></a><span data-ttu-id="9944f-103">Célula Flags (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="9944f-103">Flags Cell (Paragraph Section)</span></span>

<span data-ttu-id="9944f-104">Indica a direção do texto: da esquerda para a direita ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="9944f-104">Indicates whether the text direction is left to right or right to left.</span></span>
  
|<span data-ttu-id="9944f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9944f-105">**Value**</span></span>|<span data-ttu-id="9944f-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9944f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9944f-107">0</span><span class="sxs-lookup"><span data-stu-id="9944f-107">0</span></span>  <br/> |<span data-ttu-id="9944f-108">A direção do texto é da esquerda para a direita (o padrão).</span><span class="sxs-lookup"><span data-stu-id="9944f-108">The text direction is left to right (the default).</span></span>  <br/> |
|<span data-ttu-id="9944f-109">1 </span><span class="sxs-lookup"><span data-stu-id="9944f-109">1</span></span>  <br/> |<span data-ttu-id="9944f-110">A direção do texto é da direita para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="9944f-110">The text direction is right to left.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9944f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9944f-111">Remarks</span></span>

<span data-ttu-id="9944f-112">O valor nesta célula corresponde  à configuração Direção  na guia Parágrafo da caixa de  diálogo Texto (na guia Página Início, clique na seta Fonte), que só aparecerá se um idioma que usa texto de scripts complexos tiver sido adicionado à caixa de diálogo Preferências de Idioma do **Microsoft Office.**  </span><span class="sxs-lookup"><span data-stu-id="9944f-112">The value in this cell corresponds to the **Direction** setting on the **Paragraph** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow), which appears only if a language that uses complex scripts text has been added in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="9944f-113">(Clique **em Iniciar,** em **Todos os Programas,** em **Microsoft Office,** em Ferramentas do **Microsoft Office** e em Preferências de Idioma do **Microsoft Office.)**</span><span class="sxs-lookup"><span data-stu-id="9944f-113">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.)</span></span> 
  
<span data-ttu-id="9944f-114">Para obter uma referência para a célula Flags pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="9944f-114">To get a reference to the Flags cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9944f-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9944f-115">Cell name:</span></span>  <br/> |<span data-ttu-id="9944f-116">Para.Flags[ *i*  ] onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9944f-116">Para.Flags[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9944f-117">Para obter uma referência para a célula Flags pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9944f-117">To get a reference to the Flags cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9944f-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9944f-118">Section index:</span></span>  <br/> |<span data-ttu-id="9944f-119">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="9944f-119">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="9944f-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="9944f-120">Row index:</span></span>  <br/> |<span data-ttu-id="9944f-121">**visRowParagraph**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9944f-121">**visRowParagraph** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9944f-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="9944f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="9944f-123">**visFlags**</span><span class="sxs-lookup"><span data-stu-id="9944f-123">**visFlags**</span></span> <br/> |
   

