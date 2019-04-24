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
description: Avalia uma das duas expressões dependendo do valor de State.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331322"
---
# <a name="userui-function"></a><span data-ttu-id="96119-103">Função USERUI</span><span class="sxs-lookup"><span data-stu-id="96119-103">USERUI Function</span></span>

<span data-ttu-id="96119-104">Avalia uma das duas expressões dependendo do valor de _State_.</span><span class="sxs-lookup"><span data-stu-id="96119-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="96119-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96119-105">Syntax</span></span>

<span data-ttu-id="96119-106">USERUI (\* \* *estado* \* \*, \* \* *DefaultName* \* \*, \* \* *username* \* \*)</span><span class="sxs-lookup"><span data-stu-id="96119-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="96119-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96119-107">Parameters</span></span>

|<span data-ttu-id="96119-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="96119-108">**Name**</span></span>|<span data-ttu-id="96119-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="96119-109">**Required/Optional**</span></span>|<span data-ttu-id="96119-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="96119-110">**Data Type**</span></span>|<span data-ttu-id="96119-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="96119-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="96119-112">_state_</span><span class="sxs-lookup"><span data-stu-id="96119-112">_state_</span></span> <br/> |<span data-ttu-id="96119-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="96119-113">Required</span></span>  <br/> |<span data-ttu-id="96119-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="96119-114">**Boolean**</span></span> <br/> |<span data-ttu-id="96119-115">Determina a expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="96119-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="96119-116">_DefaultName_</span><span class="sxs-lookup"><span data-stu-id="96119-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="96119-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="96119-117">Required</span></span>  <br/> |<span data-ttu-id="96119-118">**String**</span><span class="sxs-lookup"><span data-stu-id="96119-118">**String**</span></span> <br/> |<span data-ttu-id="96119-119">A expressão padrão.</span><span class="sxs-lookup"><span data-stu-id="96119-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="96119-120">_username_</span><span class="sxs-lookup"><span data-stu-id="96119-120">_userexpression_</span></span> <br/> |<span data-ttu-id="96119-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="96119-121">Required</span></span>  <br/> |<span data-ttu-id="96119-122">**String**</span><span class="sxs-lookup"><span data-stu-id="96119-122">**String**</span></span> <br/> |<span data-ttu-id="96119-123">Uma expressão fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="96119-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96119-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="96119-124">Remarks</span></span>

<span data-ttu-id="96119-125">Se _State_ for 0, a função USERUI avaliará o _DefaultName_.</span><span class="sxs-lookup"><span data-stu-id="96119-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="96119-126">Se _State_ for 1, ele avaliará a _username_.</span><span class="sxs-lookup"><span data-stu-id="96119-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="96119-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="96119-127">Example</span></span>

<span data-ttu-id="96119-128">USERUI (1, se (Width\>6pol, 6Pol, Width), Width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="96119-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="96119-129">Avalia a expressão largura\*. 075 e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="96119-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

