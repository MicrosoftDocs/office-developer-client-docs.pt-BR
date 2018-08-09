---
title: Seção Scratch
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm2125
localization_priority: Normal
ms.assetid: 144dd06f-7225-57db-fd19-a58d6bccf0e1
description: Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.
ms.openlocfilehash: 16f0bac8f139c0b03d7826ac377a964d15296dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772845"
---
# <a name="scratch-section"></a><span data-ttu-id="a3834-103">Seção Scratch</span><span class="sxs-lookup"><span data-stu-id="a3834-103">Scratch Section</span></span>

<span data-ttu-id="a3834-104">Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.</span><span class="sxs-lookup"><span data-stu-id="a3834-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3834-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3834-105">Remarks</span></span>

<span data-ttu-id="a3834-p101">É possível adicionar essa seção usando a caixa de diálogo **Inserir Seção**. Clique com o botão direito do mouse na janela do ShapeSheet e clique em **Inserir Seção**.</span><span class="sxs-lookup"><span data-stu-id="a3834-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="a3834-108">A seção **Scratch** geralmente é usada para isolar cálculos complexos repetidos.</span><span class="sxs-lookup"><span data-stu-id="a3834-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="a3834-109">Se a solução tiver um objetivo bem definido, é mais sensato usar uma célula na seção **User-Defined Cells** para manter a clareza, pois as células de usuário podem ser nomeadas.</span><span class="sxs-lookup"><span data-stu-id="a3834-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="a3834-110">Células na seção **Scratch** usem unidades de duas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="a3834-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="a3834-111">Células X e Y usam unidades de desenho; Um até células de D não usam unidades.</span><span class="sxs-lookup"><span data-stu-id="a3834-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="a3834-112">(No jargão dos programadores C, células X e Y são "digitadas" e células de À D são "anuladas".) As células **Scratch X** e **Y de Scratch** geralmente são usadas para derivar as coordenadas *x* e *y* , como **PinX** e **PinY**ou as células X e Y encontradas em uma célula da seção **Geometry** .</span><span class="sxs-lookup"><span data-stu-id="a3834-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="a3834-113">Células de que à D pode exibir qualquer unidade que você especificar transitórias.</span><span class="sxs-lookup"><span data-stu-id="a3834-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="a3834-114">Outra diferença é a maneira que essas células armazenam valores de ponto.</span><span class="sxs-lookup"><span data-stu-id="a3834-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="a3834-115">Um ponto no Visio é um pacote de dados único para uma coordenada ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="a3834-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="a3834-116">Quando uma fórmula retorna um valor de ponto, esse valor será interpretado em uma destas três formas, dependendo da célula ShapeSheet que a fórmula é no.</span><span class="sxs-lookup"><span data-stu-id="a3834-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="a3834-117">As células que se relacionam com *x* -coordenadas (por exemplo, **PinX**ou células na coluna X de uma seção **Geometry** ) extrair apenas o *x* -coordenar a parte de um valor de ponto.</span><span class="sxs-lookup"><span data-stu-id="a3834-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="a3834-118">As células que se relacionam com *y* -coordenadas extrair apenas *y* -coordenar a parte de um valor de ponto.</span><span class="sxs-lookup"><span data-stu-id="a3834-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="a3834-119">Por exemplo, o Visio extrai a fórmula `PNT(3,4)` dessas três maneiras.</span><span class="sxs-lookup"><span data-stu-id="a3834-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="a3834-120">**Célula**</span><span class="sxs-lookup"><span data-stu-id="a3834-120">**Cell**</span></span>|<span data-ttu-id="a3834-121">**Se você digitar**</span><span class="sxs-lookup"><span data-stu-id="a3834-121">**If you enter**</span></span>|<span data-ttu-id="a3834-122">**O Visio tratará como**</span><span class="sxs-lookup"><span data-stu-id="a3834-122">**Visio treats it as**</span></span>|<span data-ttu-id="a3834-123">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="a3834-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3834-124">X</span><span class="sxs-lookup"><span data-stu-id="a3834-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="a3834-125">3.0000 pol.</span><span class="sxs-lookup"><span data-stu-id="a3834-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="a3834-126">Y</span><span class="sxs-lookup"><span data-stu-id="a3834-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="a3834-127">4.0000 pol.</span><span class="sxs-lookup"><span data-stu-id="a3834-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="a3834-128">A-D</span><span class="sxs-lookup"><span data-stu-id="a3834-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="a3834-129">PNT (3.0000 pol., 4,0000 pol.)</span><span class="sxs-lookup"><span data-stu-id="a3834-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

