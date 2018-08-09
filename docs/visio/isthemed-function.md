---
title: Função ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Retorna um valor Boolean que indica se uma forma tem um tema aplicado a ela.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772138"
---
# <a name="isthemed-function"></a><span data-ttu-id="1fb5e-103">Função ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="1fb5e-103">ISTHEMED Function</span></span>

<span data-ttu-id="1fb5e-104">Retorna um valor Boolean que indica se uma forma tem um tema aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="1fb5e-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="1fb5e-105">Version Information</span></span>

<span data-ttu-id="1fb5e-106">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="1fb5e-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1fb5e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fb5e-107">Syntax</span></span>

 <span data-ttu-id="1fb5e-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="1fb5e-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="1fb5e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1fb5e-109">Return value</span></span>

<span data-ttu-id="1fb5e-110">Booliano</span><span class="sxs-lookup"><span data-stu-id="1fb5e-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1fb5e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fb5e-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="1fb5e-112">A função **ISTHEMED** no Visio 2013 substitui a função **CELLISTHEMED** das versões anteriores do Visio.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="1fb5e-113">O **ISTHEMED** funcionar permite atribuir partes adequadas de formatação de um tema a uma forma, mas manter a capacidade de substituir a outras partes do tema formatação com a formatação aplicada manualmente.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="1fb5e-114">Se você subsequentemente reaplicar o tema, qualquer formatação manual será substituída e forma leva em toda a formatação do tema.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="1fb5e-115">**ISTHEMED** é avaliada como TRUE se a célula [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) na forma for maior que 0.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="1fb5e-116">Se esta célula for igual a 0, **ISTHEMED** avalie como FALSE.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="1fb5e-117">O tema do DocumentSheet e PageSheet não afetará o valor da função **ISTHEMED** usado em um ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="1fb5e-118">Somente se a função **ISTHEMED** aparecerá no PageSheet faz questão de tema da página.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1fb5e-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1fb5e-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="1fb5e-120">Célula</span><span class="sxs-lookup"><span data-stu-id="1fb5e-120">Cell</span></span>  <br/> |<span data-ttu-id="1fb5e-121">Fórmula</span><span class="sxs-lookup"><span data-stu-id="1fb5e-121">Formula</span></span>  <br/> |<span data-ttu-id="1fb5e-122">Resultado</span><span class="sxs-lookup"><span data-stu-id="1fb5e-122">Result</span></span>  <br/> |
|<span data-ttu-id="1fb5e-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="1fb5e-123">Char.Font</span></span>  <br/> |<span data-ttu-id="1fb5e-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="1fb5e-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="1fb5e-125">Se a forma tiver um com tema aplicado a ele, o texto da forma aceita a formatação do tema de fonte.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="1fb5e-126">Se a forma não estiver com temas, o texto da forma é formatado com a fonte "Calibri".</span><span class="sxs-lookup"><span data-stu-id="1fb5e-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="1fb5e-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="1fb5e-127">LineColor</span></span>  <br/> |<span data-ttu-id="1fb5e-128">IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="1fb5e-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="1fb5e-129">Se a forma tiver um com tema aplicado a ela, a cor da linha da forma é vermelho.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="1fb5e-130">Se a forma não estiver com temas, a cor da linha da forma é verde.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

