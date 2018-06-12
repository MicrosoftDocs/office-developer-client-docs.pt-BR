---
title: Função RECTSECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcula o setor de um retângulo associado a x e y e retorna um inteiro de 0 a 4, indicando o setor.
ms.openlocfilehash: 1f35704cdb827c9c751f11593436c110755d7777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772641"
---
# <a name="rectsect-function"></a><span data-ttu-id="695a1-103">Função RECTSECT</span><span class="sxs-lookup"><span data-stu-id="695a1-103">RECTSECT Function</span></span>

<span data-ttu-id="695a1-104">Calcula o setor de um retângulo associado a *x* e *y* e retorna um inteiro de 0 a 4, indicando o setor.</span><span class="sxs-lookup"><span data-stu-id="695a1-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="695a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="695a1-105">Syntax</span></span>

<span data-ttu-id="695a1-106">RECTSECT (* * *largura* * *, * * *Altura* * *, * * *x* * *, * * *y* * *, * * *opção* * *)</span><span class="sxs-lookup"><span data-stu-id="695a1-106">RECTSECT(** *width* **, ** *height* **, ** *x* **, ** *y* **, ** *option* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="695a1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="695a1-107">Parameters</span></span>

|<span data-ttu-id="695a1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="695a1-108">**Name**</span></span>|<span data-ttu-id="695a1-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="695a1-109">**Required/Optional**</span></span>|<span data-ttu-id="695a1-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="695a1-110">**Data Type**</span></span>|<span data-ttu-id="695a1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="695a1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="695a1-112">_width_</span><span class="sxs-lookup"><span data-stu-id="695a1-112">_width_</span></span> <br/> |<span data-ttu-id="695a1-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="695a1-113">Required</span></span>  <br/> |<span data-ttu-id="695a1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="695a1-114">**String**</span></span> <br/> |<span data-ttu-id="695a1-115">Largura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="695a1-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="695a1-116">_height_</span><span class="sxs-lookup"><span data-stu-id="695a1-116">_height_</span></span> <br/> |<span data-ttu-id="695a1-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="695a1-117">Required</span></span>  <br/> |<span data-ttu-id="695a1-118">**String**</span><span class="sxs-lookup"><span data-stu-id="695a1-118">**String**</span></span> <br/> |<span data-ttu-id="695a1-119">Altura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="695a1-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="695a1-120">_x_</span><span class="sxs-lookup"><span data-stu-id="695a1-120">_x_</span></span> <br/> |<span data-ttu-id="695a1-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="695a1-121">Required</span></span>  <br/> |<span data-ttu-id="695a1-122">**String**</span><span class="sxs-lookup"><span data-stu-id="695a1-122">**String**</span></span> <br/> |<span data-ttu-id="695a1-123">Uma coordenada x.</span><span class="sxs-lookup"><span data-stu-id="695a1-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="695a1-124">_y_</span><span class="sxs-lookup"><span data-stu-id="695a1-124">_y_</span></span> <br/> |<span data-ttu-id="695a1-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="695a1-125">Required</span></span>  <br/> |<span data-ttu-id="695a1-126">**String**</span><span class="sxs-lookup"><span data-stu-id="695a1-126">**String**</span></span> <br/> |<span data-ttu-id="695a1-127">Uma coordenada y.</span><span class="sxs-lookup"><span data-stu-id="695a1-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="695a1-128">_opção_</span><span class="sxs-lookup"><span data-stu-id="695a1-128">_option_</span></span> <br/> |<span data-ttu-id="695a1-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="695a1-129">Required</span></span>  <br/> |<span data-ttu-id="695a1-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="695a1-130">**Boolean**</span></span> <br/> |<span data-ttu-id="695a1-p101">Especifica como os pontos colocados nas diagonais são tratados. Configure o valor como 0 para usar os setores esquerdo e direito para os pontos em uma diagonal. Configure o valor como 1 para usar os setores superior e inferior para os pontos em uma diagonal.</span><span class="sxs-lookup"><span data-stu-id="695a1-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="695a1-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="695a1-134">Remarks</span></span>

<span data-ttu-id="695a1-135">Considere um retângulo que tem uma *largura* e *Altura* e um ponto (*x, y*) a partir do ponto central do retângulo.</span><span class="sxs-lookup"><span data-stu-id="695a1-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="695a1-136">Desenhe linhas diagonais por meio de cantos do retângulo para dividi-lo em quatro setores e um ponto central.</span><span class="sxs-lookup"><span data-stu-id="695a1-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="695a1-137">Os setores de 0 a 4 representam o ponto central direita, superior, esquerda e inferior respectivamente.</span><span class="sxs-lookup"><span data-stu-id="695a1-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="695a1-138">Example</span><span class="sxs-lookup"><span data-stu-id="695a1-138">Example</span></span>

<span data-ttu-id="695a1-139">RECTSECT(1 pol, 2 pol, 1 pol, -7 pol, 0)</span><span class="sxs-lookup"><span data-stu-id="695a1-139">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="695a1-140">Retornará 4.</span><span class="sxs-lookup"><span data-stu-id="695a1-140">Returns 4.</span></span> 
  

