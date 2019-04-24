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
ms.openlocfilehash: a7d2c6762e96fc19986521c2ba164666b925c928
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344524"
---
# <a name="scratch-section"></a><span data-ttu-id="fccb9-103">Seção Scratch</span><span class="sxs-lookup"><span data-stu-id="fccb9-103">Scratch Section</span></span>

<span data-ttu-id="fccb9-104">Uma área de trabalho para inserir e testar fórmulas que podem ser referenciadas por outras células.</span><span class="sxs-lookup"><span data-stu-id="fccb9-104">A work area for entering and testing formulas that can be referred to by other cells.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fccb9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="fccb9-105">Remarks</span></span>

<span data-ttu-id="fccb9-p101">É possível adicionar essa seção usando a caixa de diálogo **Inserir Seção**. Clique com o botão direito do mouse na janela do ShapeSheet e clique em **Inserir Seção**.</span><span class="sxs-lookup"><span data-stu-id="fccb9-p101">You can add this section by using the **Insert Section** dialog box. Right-click in the ShapeSheet window, and then click **Insert Section**.</span></span>
  
<span data-ttu-id="fccb9-108">A seção **Scratch** é normalmente usada para isolar cálculos complexos repetidos.</span><span class="sxs-lookup"><span data-stu-id="fccb9-108">The **Scratch** section is typically used to isolate repeated complex calculations.</span></span> <span data-ttu-id="fccb9-109">Se a sua solução tiver um objetivo bem definido, é mais sensato usar uma célula na seção **User-defined Cells** para maior clareza, pois as células do usuário podem ser nomeadas.</span><span class="sxs-lookup"><span data-stu-id="fccb9-109">If your solution has a well-defined purpose, it's wiser to use a cell in the **User-Defined Cells** section for clarity because User cells can be named.</span></span> 
  
<span data-ttu-id="fccb9-110">As células na seção **Scratch** usam unidades de duas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="fccb9-110">Cells in the **Scratch** section use units in two different ways.</span></span> <span data-ttu-id="fccb9-111">As células X e Y usam unidades de desenho; as células de A a D não usam unidades.</span><span class="sxs-lookup"><span data-stu-id="fccb9-111">X and Y cells use drawing units; A through D cells don't use units.</span></span> <span data-ttu-id="fccb9-112">(No jargão dos programadores de C, as células X e Y são "digitadas" e as células de A a D são "anuladas".) As células de **rascunho x** e **Scratch** são usadas com frequência para derivar coordenadas *x* e *y* , como **PinX** e **Piny**, ou as células x e Y encontradas em uma célula de seção **Geometry** .</span><span class="sxs-lookup"><span data-stu-id="fccb9-112">(In C programmers' jargon, X and Y cells are "typed," and cells A through D are "void.") The **Scratch X** and **Scratch Y** cells are often used for deriving  *x-*  and  *y-*  coordinates, such as **PinX** and **PinY**, or the X and Y cells found in a **Geometry** section cell.</span></span> <span data-ttu-id="fccb9-113">As células de A a D da seção Scratch podem exibir qualquer unidade que for especificada.</span><span class="sxs-lookup"><span data-stu-id="fccb9-113">Scratch cells A through D can display whatever units you specify.</span></span> 
  
<span data-ttu-id="fccb9-114">Outra diferença é a maneira com que essas células armazenam valores de ponto.</span><span class="sxs-lookup"><span data-stu-id="fccb9-114">A further difference is the way these cells store point values.</span></span> <span data-ttu-id="fccb9-115">Um ponto no Visio é um pacote de dados único para uma coordenada ( *x, y*).</span><span class="sxs-lookup"><span data-stu-id="fccb9-115">A point in Visio is a single data package for an ( *x,y*) coordinate.</span></span> <span data-ttu-id="fccb9-116">Quando uma fórmula retorna um valor de ponto, esse valor pode ser interpretado de três formas, que dependerá em que célula ShapeSheet a fórmula se encontra.</span><span class="sxs-lookup"><span data-stu-id="fccb9-116">When a formula returns a point value, that value is interpreted in one of three ways, depending on the ShapeSheet cell the formula is in.</span></span> <span data-ttu-id="fccb9-117">As células que estão relacionadas às coordenadas *x* (por exemplo, **PinX**ou células na coluna x de uma seção **Geometry** ) extraem apenas a parte coordenada *x* de um valor de ponto.</span><span class="sxs-lookup"><span data-stu-id="fccb9-117">Cells that relate to  *x*  -coordinates (for example, **PinX**, or cells in the X column of a **Geometry** section) extract just the  *x*  -coordinate part of a point value.</span></span> <span data-ttu-id="fccb9-118">As células que estão relacionadas às coordenadas *y* extrairão apenas a parte da coordenada *y* de um valor de ponto.</span><span class="sxs-lookup"><span data-stu-id="fccb9-118">Cells that relate to  *y*  -coordinates extract just the  *y*  -coordinate part of a point value.</span></span> 
  
<span data-ttu-id="fccb9-119">Por exemplo, o Visio extrai a fórmula `PNT(3,4)` dessas três maneiras.</span><span class="sxs-lookup"><span data-stu-id="fccb9-119">For example, Visio extracts the formula  `PNT(3,4)` in these three ways.</span></span> 
  
|<span data-ttu-id="fccb9-120">**Cell**</span><span class="sxs-lookup"><span data-stu-id="fccb9-120">**Cell**</span></span>|<span data-ttu-id="fccb9-121">**Se você digitar**</span><span class="sxs-lookup"><span data-stu-id="fccb9-121">**If you enter**</span></span>|<span data-ttu-id="fccb9-122">**O Visio tratará como**</span><span class="sxs-lookup"><span data-stu-id="fccb9-122">**Visio treats it as**</span></span>|<span data-ttu-id="fccb9-123">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="fccb9-123">**Result**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fccb9-124">X</span><span class="sxs-lookup"><span data-stu-id="fccb9-124">X</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTX(PNT(3,4))` <br/> | <span data-ttu-id="fccb9-125">3.0000 pol.</span><span class="sxs-lookup"><span data-stu-id="fccb9-125">3.0000 in.</span></span>  <br/> |
| <span data-ttu-id="fccb9-126">S</span><span class="sxs-lookup"><span data-stu-id="fccb9-126">Y</span></span>  <br/> | `PNT(3,4)` <br/> | `PNTY(PNT(3,4))` <br/> | <span data-ttu-id="fccb9-127">4.0000 pol.</span><span class="sxs-lookup"><span data-stu-id="fccb9-127">4.0000 in.</span></span>  <br/> |
| <span data-ttu-id="fccb9-128">A-D</span><span class="sxs-lookup"><span data-stu-id="fccb9-128">A-D</span></span>  <br/> | `PNT(3,4)` <br/> | `PNT(3,4)` <br/> | <span data-ttu-id="fccb9-129">PNT (3.0000 em., 4, 0)</span><span class="sxs-lookup"><span data-stu-id="fccb9-129">PNT(3.0000 in., 4.0000 in.)</span></span>  <br/> |
   

