---
title: Função USERUI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Avalia uma das duas expressões dependendo do valor de estado.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773238"
---
# <a name="userui-function"></a><span data-ttu-id="d0015-103">Função USERUI</span><span class="sxs-lookup"><span data-stu-id="d0015-103">USERUI Function</span></span>

<span data-ttu-id="d0015-104">Avalia uma das duas expressões dependendo do valor de _estado_.</span><span class="sxs-lookup"><span data-stu-id="d0015-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d0015-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0015-105">Syntax</span></span>

<span data-ttu-id="d0015-106">USERUI (* * *estado* * *, * * *defaultexpression* * *, * * *userexpression* * *)</span><span class="sxs-lookup"><span data-stu-id="d0015-106">USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0015-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0015-107">Parameters</span></span>

|<span data-ttu-id="d0015-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d0015-108">**Name**</span></span>|<span data-ttu-id="d0015-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d0015-109">**Required/Optional**</span></span>|<span data-ttu-id="d0015-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d0015-110">**Data Type**</span></span>|<span data-ttu-id="d0015-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d0015-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0015-112">_state_</span><span class="sxs-lookup"><span data-stu-id="d0015-112">_state_</span></span> <br/> |<span data-ttu-id="d0015-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d0015-113">Required</span></span>  <br/> |<span data-ttu-id="d0015-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d0015-114">**Boolean**</span></span> <br/> |<span data-ttu-id="d0015-115">Determina qual expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="d0015-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="d0015-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="d0015-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="d0015-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d0015-117">Required</span></span>  <br/> |<span data-ttu-id="d0015-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d0015-118">**String**</span></span> <br/> |<span data-ttu-id="d0015-119">A expressão padrão.</span><span class="sxs-lookup"><span data-stu-id="d0015-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="d0015-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="d0015-120">_userexpression_</span></span> <br/> |<span data-ttu-id="d0015-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d0015-121">Required</span></span>  <br/> |<span data-ttu-id="d0015-122">**String**</span><span class="sxs-lookup"><span data-stu-id="d0015-122">**String**</span></span> <br/> |<span data-ttu-id="d0015-123">Uma expressão fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d0015-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0015-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d0015-124">Remarks</span></span>

<span data-ttu-id="d0015-125">Se o _estado_ for 0, a função USERUI avalia o _defaultexpression_.</span><span class="sxs-lookup"><span data-stu-id="d0015-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="d0015-126">Se o _estado_ for 1, ela avalia o _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="d0015-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="d0015-127">Example</span><span class="sxs-lookup"><span data-stu-id="d0015-127">Example</span></span>

<span data-ttu-id="d0015-128">USERUI (1, se (largura\>6pol, 6pol, largura), largura\*0,75)</span><span class="sxs-lookup"><span data-stu-id="d0015-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="d0015-129">Avalia a expressão largura\*.075 e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="d0015-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

