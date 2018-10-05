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
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395081"
---
# <a name="rectsect-function"></a><span data-ttu-id="6033a-103">Função RECTSECT</span><span class="sxs-lookup"><span data-stu-id="6033a-103">RECTSECT Function</span></span>

<span data-ttu-id="6033a-104">Calcula o setor de um retângulo associado a *x* e *y* e retorna um inteiro de 0 a 4, indicando o setor.</span><span class="sxs-lookup"><span data-stu-id="6033a-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6033a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6033a-105">Syntax</span></span>

<span data-ttu-id="6033a-106">RECTSECT (\* \* *largura* \* \*, \* \* *Altura* \* \*, \* \* *x* \* \*, \* \* *y* \* \*, \* \* *opção* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6033a-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6033a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6033a-107">Parameters</span></span>

|<span data-ttu-id="6033a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6033a-108">**Name**</span></span>|<span data-ttu-id="6033a-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6033a-109">**Required/Optional**</span></span>|<span data-ttu-id="6033a-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6033a-110">**Data Type**</span></span>|<span data-ttu-id="6033a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6033a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6033a-112">_width_</span><span class="sxs-lookup"><span data-stu-id="6033a-112">_width_</span></span> <br/> |<span data-ttu-id="6033a-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6033a-113">Required</span></span>  <br/> |<span data-ttu-id="6033a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6033a-114">**String**</span></span> <br/> |<span data-ttu-id="6033a-115">Largura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="6033a-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="6033a-116">_height_</span><span class="sxs-lookup"><span data-stu-id="6033a-116">_height_</span></span> <br/> |<span data-ttu-id="6033a-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6033a-117">Required</span></span>  <br/> |<span data-ttu-id="6033a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="6033a-118">**String**</span></span> <br/> |<span data-ttu-id="6033a-119">Altura do retângulo.</span><span class="sxs-lookup"><span data-stu-id="6033a-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="6033a-120">_x_</span><span class="sxs-lookup"><span data-stu-id="6033a-120">_x_</span></span> <br/> |<span data-ttu-id="6033a-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6033a-121">Required</span></span>  <br/> |<span data-ttu-id="6033a-122">**String**</span><span class="sxs-lookup"><span data-stu-id="6033a-122">**String**</span></span> <br/> |<span data-ttu-id="6033a-123">Uma coordenada x.</span><span class="sxs-lookup"><span data-stu-id="6033a-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="6033a-124">_y_</span><span class="sxs-lookup"><span data-stu-id="6033a-124">_y_</span></span> <br/> |<span data-ttu-id="6033a-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6033a-125">Required</span></span>  <br/> |<span data-ttu-id="6033a-126">**String**</span><span class="sxs-lookup"><span data-stu-id="6033a-126">**String**</span></span> <br/> |<span data-ttu-id="6033a-127">Uma coordenada y.</span><span class="sxs-lookup"><span data-stu-id="6033a-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="6033a-128">_opção_</span><span class="sxs-lookup"><span data-stu-id="6033a-128">_option_</span></span> <br/> |<span data-ttu-id="6033a-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6033a-129">Required</span></span>  <br/> |<span data-ttu-id="6033a-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6033a-130">**Boolean**</span></span> <br/> |<span data-ttu-id="6033a-p101">Especifica como os pontos colocados nas diagonais são tratados. Configure o valor como 0 para usar os setores esquerdo e direito para os pontos em uma diagonal. Configure o valor como 1 para usar os setores superior e inferior para os pontos em uma diagonal.</span><span class="sxs-lookup"><span data-stu-id="6033a-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6033a-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="6033a-134">Remarks</span></span>

<span data-ttu-id="6033a-135">Considere um retângulo que tem uma *largura* e *Altura* e um ponto (*x, y*) a partir do ponto central do retângulo.</span><span class="sxs-lookup"><span data-stu-id="6033a-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="6033a-136">Desenhe linhas diagonais por meio de cantos do retângulo para dividi-lo em quatro setores e um ponto central.</span><span class="sxs-lookup"><span data-stu-id="6033a-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="6033a-137">Os setores de 0 a 4 representam o ponto central direita, superior, esquerda e inferior respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6033a-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Setores 0 a 4 representam o ponto central direita, superior, esquerda e baixo respectivamente](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="6033a-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6033a-139">Example</span></span>

<span data-ttu-id="6033a-140">RECTSECT(1 pol, 2 pol, 1 pol, -7 pol, 0)</span><span class="sxs-lookup"><span data-stu-id="6033a-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="6033a-141">Retornará 4.</span><span class="sxs-lookup"><span data-stu-id="6033a-141">Returns 4.</span></span> 
  

