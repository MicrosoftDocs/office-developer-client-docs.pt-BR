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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420343"
---
# <a name="userui-function"></a><span data-ttu-id="a3646-103">Função USERUI</span><span class="sxs-lookup"><span data-stu-id="a3646-103">USERUI Function</span></span>

<span data-ttu-id="a3646-104">Avalia uma das duas expressões dependendo do valor de _State_.</span><span class="sxs-lookup"><span data-stu-id="a3646-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a3646-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3646-105">Syntax</span></span>

<span data-ttu-id="a3646-106">USERUI (\* \* *estado* \* \*, \* \* *DefaultName* \* \*, \* \* *username* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a3646-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a3646-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3646-107">Parameters</span></span>

|<span data-ttu-id="a3646-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a3646-108">**Name**</span></span>|<span data-ttu-id="a3646-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a3646-109">**Required/Optional**</span></span>|<span data-ttu-id="a3646-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a3646-110">**Data Type**</span></span>|<span data-ttu-id="a3646-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a3646-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3646-112">_state_</span><span class="sxs-lookup"><span data-stu-id="a3646-112">_state_</span></span> <br/> |<span data-ttu-id="a3646-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3646-113">Required</span></span>  <br/> |<span data-ttu-id="a3646-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a3646-114">**Boolean**</span></span> <br/> |<span data-ttu-id="a3646-115">Determina a expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="a3646-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a3646-116">_DefaultName_</span><span class="sxs-lookup"><span data-stu-id="a3646-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="a3646-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3646-117">Required</span></span>  <br/> |<span data-ttu-id="a3646-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3646-118">**String**</span></span> <br/> |<span data-ttu-id="a3646-119">A expressão padrão.</span><span class="sxs-lookup"><span data-stu-id="a3646-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="a3646-120">_username_</span><span class="sxs-lookup"><span data-stu-id="a3646-120">_userexpression_</span></span> <br/> |<span data-ttu-id="a3646-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3646-121">Required</span></span>  <br/> |<span data-ttu-id="a3646-122">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a3646-122">**String**</span></span> <br/> |<span data-ttu-id="a3646-123">Uma expressão fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a3646-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3646-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3646-124">Remarks</span></span>

<span data-ttu-id="a3646-125">Se _State_ for 0, a função USERUI avaliará o _DefaultName_.</span><span class="sxs-lookup"><span data-stu-id="a3646-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="a3646-126">Se _State_ for 1, ele avaliará a _username_.</span><span class="sxs-lookup"><span data-stu-id="a3646-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="a3646-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a3646-127">Example</span></span>

<span data-ttu-id="a3646-128">USERUI (1, se (Width\>6pol, 6Pol, Width), Width\*0,75)</span><span class="sxs-lookup"><span data-stu-id="a3646-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="a3646-129">Avalia a expressão largura\*. 075 e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="a3646-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

