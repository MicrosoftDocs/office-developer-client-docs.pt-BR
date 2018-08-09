---
title: Função NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772404"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="6736b-103">Função NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="6736b-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="6736b-104">Retorna o percentual da distância no caminho do ponto mais próximo às coordenadas especificadas, como um valor entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="6736b-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="6736b-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="6736b-105">Version Information</span></span>

<span data-ttu-id="6736b-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="6736b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6736b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6736b-107">Syntax</span></span>

<span data-ttu-id="6736b-108">NEARESTPOINTONPATH (* * *seção* * *, * * *x* * *, * * *y* * *)</span><span class="sxs-lookup"><span data-stu-id="6736b-108">NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6736b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6736b-109">Parameters</span></span>

|<span data-ttu-id="6736b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="6736b-110">**Name**</span></span>|<span data-ttu-id="6736b-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="6736b-111">**Required/Optional**</span></span>|<span data-ttu-id="6736b-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6736b-112">**Data Type**</span></span>|<span data-ttu-id="6736b-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6736b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6736b-114">_section_</span><span class="sxs-lookup"><span data-stu-id="6736b-114">_section_</span></span> <br/> |<span data-ttu-id="6736b-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6736b-115">Required</span></span>  <br/> |<span data-ttu-id="6736b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="6736b-116">**String**</span></span> <br/> |<span data-ttu-id="6736b-117">A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="6736b-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="6736b-118">_x_</span><span class="sxs-lookup"><span data-stu-id="6736b-118">_x_</span></span> <br/> |<span data-ttu-id="6736b-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6736b-119">Required</span></span>  <br/> |<span data-ttu-id="6736b-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="6736b-120">**Double**</span></span> <br/> |<span data-ttu-id="6736b-121">_X_-coordenadas do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="6736b-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="6736b-122">_y_</span><span class="sxs-lookup"><span data-stu-id="6736b-122">_y_</span></span> <br/> |<span data-ttu-id="6736b-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6736b-123">Required</span></span>  <br/> |<span data-ttu-id="6736b-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="6736b-124">**Double**</span></span> <br/> |<span data-ttu-id="6736b-125">_Y_-coordenadas do ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="6736b-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6736b-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6736b-126">Return value</span></span>

 <span data-ttu-id="6736b-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="6736b-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6736b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="6736b-128">Remarks</span></span>

<span data-ttu-id="6736b-129">Se a _seção_ não existir, o Microsoft Visio retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="6736b-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

