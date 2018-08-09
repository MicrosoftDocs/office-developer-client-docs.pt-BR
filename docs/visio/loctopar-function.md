---
title: Função LOCTOPAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Retorna um ponto transformado em coordenadas pai no sistema de coordenadas de destino.
ms.openlocfilehash: 7d882ec34de93db2828fc751f99d87fc3e961d64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772305"
---
# <a name="loctopar-function"></a><span data-ttu-id="c7ea1-103">Função LOCTOPAR</span><span class="sxs-lookup"><span data-stu-id="c7ea1-103">LOCTOPAR Function</span></span>

<span data-ttu-id="c7ea1-104">Retorna um ponto transformado em coordenadas pai no sistema de coordenadas de destino.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-104">Returns a transformed point in parent coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c7ea1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7ea1-105">Syntax</span></span>

<span data-ttu-id="c7ea1-106">LOCTOPAR (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="c7ea1-106">LOCTOPAR(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c7ea1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7ea1-107">Parameters</span></span>

|<span data-ttu-id="c7ea1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-108">**Name**</span></span>|<span data-ttu-id="c7ea1-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-109">**Required/Optional**</span></span>|<span data-ttu-id="c7ea1-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-110">**Data Type**</span></span>|<span data-ttu-id="c7ea1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c7ea1-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="c7ea1-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="c7ea1-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c7ea1-113">Required</span></span>  <br/> |<span data-ttu-id="c7ea1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-114">**String**</span></span> <br/> | <span data-ttu-id="c7ea1-115">Um ponto nas coordenadas locais no sistema de coordenadas de origem.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="c7ea1-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="c7ea1-116">_srcRef_</span></span> <br/> |<span data-ttu-id="c7ea1-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c7ea1-117">Required</span></span>  <br/> |<span data-ttu-id="c7ea1-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-118">**String**</span></span> <br/> | <span data-ttu-id="c7ea1-119">Uma referência a uma célula no objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="c7ea1-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="c7ea1-120">_dstRef_</span></span> <br/> |<span data-ttu-id="c7ea1-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c7ea1-121">Required</span></span>  <br/> |<span data-ttu-id="c7ea1-122">**String**</span><span class="sxs-lookup"><span data-stu-id="c7ea1-122">**String**</span></span> <br/> | <span data-ttu-id="c7ea1-123">Uma referência a uma célula no objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c7ea1-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c7ea1-124">Return value</span></span>

<span data-ttu-id="c7ea1-125">String</span><span class="sxs-lookup"><span data-stu-id="c7ea1-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7ea1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ea1-126">Remarks</span></span>

<span data-ttu-id="c7ea1-p101">Converte um ponto de coordenadas locais em uma forma de origem em coordenadas pai em uma forma de destino. Utilize a função LOCTOPAR para definir coordenadas pai em células, como PinX, PinY, BeginX e BeginY, em uma forma que esteja usando outro ponto de um outro sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-p101">Converts a point from local coordinates in a source shape to parent coordinates in a destination shape. You can use the LOCTOPAR function to set parent coordinates in cells, such as PinX, PinY, BeginX, and BeginY in a shape using another point from another coordinate system.</span></span> 
  
<span data-ttu-id="c7ea1-p102">Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span> 
  
<span data-ttu-id="c7ea1-131">As coordenadas de origem e de destino devem estar na mesma página.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-131">The source and destination coordinates must be on the same page.</span></span> 
  
<span data-ttu-id="c7ea1-132">Se o destino for uma página que não tem um pai, o resultado será expresso em coordenadas locais da página.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-132">If the destination is a page, which has no parent, the result is expressed in the page's local coordinates.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c7ea1-133">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c7ea1-133">Example</span></span>

<span data-ttu-id="c7ea1-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span><span class="sxs-lookup"><span data-stu-id="c7ea1-134">LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width)</span></span> 
  
<span data-ttu-id="c7ea1-135">Converterá o pino local da forma associada à fórmula em coordenadas pai de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="c7ea1-135">Converts the local pin of the shape associated with the formula to parent coordinates of Sheet.4.</span></span> 
  

