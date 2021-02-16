---
title: Função ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Retorna um valor Boolean indicando se uma forma tem um tema aplicado a ela.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418117"
---
# <a name="isthemed-function"></a><span data-ttu-id="3cd57-103">Função ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="3cd57-103">ISTHEMED Function</span></span>

<span data-ttu-id="3cd57-104">Retorna um valor Boolean indicando se uma forma tem um tema aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="3cd57-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="3cd57-105">Informações sobre a versão</span><span class="sxs-lookup"><span data-stu-id="3cd57-105">Version Information</span></span>

<span data-ttu-id="3cd57-106">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="3cd57-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3cd57-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cd57-107">Syntax</span></span>

 <span data-ttu-id="3cd57-108">**ISTHEMED**()</span><span class="sxs-lookup"><span data-stu-id="3cd57-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3cd57-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3cd57-109">Return value</span></span>

<span data-ttu-id="3cd57-110">Booliano</span><span class="sxs-lookup"><span data-stu-id="3cd57-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3cd57-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd57-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="3cd57-112">A **função ISTHEMED** no Visio 2013 substitui a função **CELLISTHEMED** de versões anteriores do Visio.</span><span class="sxs-lookup"><span data-stu-id="3cd57-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="3cd57-113">A **função ISTHEMED** permite atribuir partes apropriadas da formatação de um tema a uma forma, mas mantém a capacidade de substituir outras partes da formatação do tema pela formatação aplicada manualmente.</span><span class="sxs-lookup"><span data-stu-id="3cd57-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="3cd57-114">Se você reaplicar posteriormente o tema, qualquer formatação manual será substituído e a forma assumirá toda a formatação do tema.</span><span class="sxs-lookup"><span data-stu-id="3cd57-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="3cd57-115">**ISTHEMED** avalia como TRUE se a [célula ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) na forma for maior que 0.</span><span class="sxs-lookup"><span data-stu-id="3cd57-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="3cd57-116">Se essa célula for igual a 0, **ISTHEMED** será avaliada como FALSE.</span><span class="sxs-lookup"><span data-stu-id="3cd57-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="3cd57-117">O tema da DocumentSheet e pageSheet não afetará o valor da função **ISTHEMED** usada em um ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="3cd57-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="3cd57-118">Somente se a **função ISTHEMED** aparecer no PageSheet, o tema da página será importante.</span><span class="sxs-lookup"><span data-stu-id="3cd57-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3cd57-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3cd57-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="3cd57-120">Cell</span><span class="sxs-lookup"><span data-stu-id="3cd57-120">Cell</span></span>  <br/> |<span data-ttu-id="3cd57-121">Fórmula</span><span class="sxs-lookup"><span data-stu-id="3cd57-121">Formula</span></span>  <br/> |<span data-ttu-id="3cd57-122">Resultado</span><span class="sxs-lookup"><span data-stu-id="3cd57-122">Result</span></span>  <br/> |
|<span data-ttu-id="3cd57-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="3cd57-123">Char.Font</span></span>  <br/> |<span data-ttu-id="3cd57-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="3cd57-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="3cd57-125">Se a forma tiver um tema aplicado a ela, o texto da forma aceitará a formatação da fonte do tema.</span><span class="sxs-lookup"><span data-stu-id="3cd57-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="3cd57-126">Se a forma não tiver temas, o texto da forma será formatado com a fonte "Calibri".</span><span class="sxs-lookup"><span data-stu-id="3cd57-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="3cd57-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="3cd57-127">LineColor</span></span>  <br/> |<span data-ttu-id="3cd57-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="3cd57-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="3cd57-129">Se a forma tiver um temas aplicado a ela, a cor da linha da forma será vermelho.</span><span class="sxs-lookup"><span data-stu-id="3cd57-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="3cd57-130">Se a forma não tiver temas, a cor da linha da forma será verde.</span><span class="sxs-lookup"><span data-stu-id="3cd57-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

