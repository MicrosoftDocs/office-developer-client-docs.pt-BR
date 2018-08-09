---
title: Função LOCTOLOC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Retorna um ponto transformado em coordenadas locais no sistema de coordenadas de destino.
ms.openlocfilehash: 444200801ebd984fb735b95de6d58d35e5160d1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772296"
---
# <a name="loctoloc-function"></a><span data-ttu-id="25f82-103">Função LOCTOLOC</span><span class="sxs-lookup"><span data-stu-id="25f82-103">LOCTOLOC Function</span></span>

<span data-ttu-id="25f82-104">Retorna um ponto transformado em coordenadas locais no sistema de coordenadas de destino.</span><span class="sxs-lookup"><span data-stu-id="25f82-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="25f82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f82-105">Syntax</span></span>

<span data-ttu-id="25f82-106">LOCTOLOC (* * *srcPoint* * *, * * *srcRef* * *, * * *dstRef* * *)</span><span class="sxs-lookup"><span data-stu-id="25f82-106">LOCTOLOC(** *srcPoint* **, ** *srcRef* **, ** *dstRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="25f82-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25f82-107">Parameters</span></span>

|<span data-ttu-id="25f82-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="25f82-108">**Name**</span></span>|<span data-ttu-id="25f82-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="25f82-109">**Required/Optional**</span></span>|<span data-ttu-id="25f82-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="25f82-110">**Data Type**</span></span>|<span data-ttu-id="25f82-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="25f82-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="25f82-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="25f82-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="25f82-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="25f82-113">Required</span></span>  <br/> |<span data-ttu-id="25f82-114">**String**</span><span class="sxs-lookup"><span data-stu-id="25f82-114">**String**</span></span> <br/> | <span data-ttu-id="25f82-115">Um ponto nas coordenadas locais no sistema de coordenadas de origem.</span><span class="sxs-lookup"><span data-stu-id="25f82-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="25f82-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="25f82-116">_srcRef_</span></span> <br/> |<span data-ttu-id="25f82-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="25f82-117">Required</span></span>  <br/> |<span data-ttu-id="25f82-118">**String**</span><span class="sxs-lookup"><span data-stu-id="25f82-118">**String**</span></span> <br/> | <span data-ttu-id="25f82-119">Uma referência a uma célula no objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="25f82-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="25f82-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="25f82-120">_dstRef_</span></span> <br/> |<span data-ttu-id="25f82-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="25f82-121">Required</span></span>  <br/> |<span data-ttu-id="25f82-122">**String**</span><span class="sxs-lookup"><span data-stu-id="25f82-122">**String**</span></span> <br/> | <span data-ttu-id="25f82-123">Uma referência a uma célula no objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="25f82-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="25f82-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="25f82-124">Return value</span></span>

<span data-ttu-id="25f82-125">String</span><span class="sxs-lookup"><span data-stu-id="25f82-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25f82-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f82-126">Remarks</span></span>

<span data-ttu-id="25f82-p101">A função LOCTOLOC converte um ponto de coordenadas locais de uma forma de origem em coordenadas locais de uma forma de destino. Utilize essa função para criar uma forma, por exemplo, um ponto de um outro espaço de coordenadas. É possível também usar essa função para transformar um ponto local em coordenadas de páginas ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="25f82-p101">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape. You can use this function to construct a shape, for example, in terms of a point from another coordinate space. You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="25f82-p102">Esta função funciona mesmo que as formas de origem e de destino estejam em grupos. Além disso, ajusta para rotação e inverte na transformação intermediária.</span><span class="sxs-lookup"><span data-stu-id="25f82-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="25f82-132">As coordenadas de origem e de destino devem estar na mesma página.</span><span class="sxs-lookup"><span data-stu-id="25f82-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="25f82-133">Exemplo</span><span class="sxs-lookup"><span data-stu-id="25f82-133">Example</span></span>

<span data-ttu-id="25f82-134">A fórmula a seguir converte o pino local da forma associada com a fórmula em um ponto na página.</span><span class="sxs-lookup"><span data-stu-id="25f82-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```

