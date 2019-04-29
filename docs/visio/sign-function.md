---
title: Função SIGN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Retorna um valor que representa o sinal de um número.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420651"
---
# <a name="sign-function"></a><span data-ttu-id="fa238-103">Função SIGN</span><span class="sxs-lookup"><span data-stu-id="fa238-103">SIGN Function</span></span>

<span data-ttu-id="fa238-104">Retorna um valor que representa o sinal de um número.</span><span class="sxs-lookup"><span data-stu-id="fa238-104">Returns a value that represents the sign of a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fa238-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa238-105">Syntax</span></span>

<span data-ttu-id="fa238-106">ASSINAR (\* \* *número* \* \*, \* \* *difusão* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fa238-106">SIGN(\*\* *number* \*\*, \*\* *fuzz* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fa238-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa238-107">Parameters</span></span>

|<span data-ttu-id="fa238-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fa238-108">**Name**</span></span>|<span data-ttu-id="fa238-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="fa238-109">**Required/Optional**</span></span>|<span data-ttu-id="fa238-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="fa238-110">**Data Type**</span></span>|<span data-ttu-id="fa238-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa238-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fa238-112">_number_</span><span class="sxs-lookup"><span data-stu-id="fa238-112">_number_</span></span> <br/> |<span data-ttu-id="fa238-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fa238-113">Required</span></span>  <br/> |<span data-ttu-id="fa238-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="fa238-114">**Numeric**</span></span> <br/> | <span data-ttu-id="fa238-115">O número para o qual deseja determinar o sinal.</span><span class="sxs-lookup"><span data-stu-id="fa238-115">The number for which you want to determine the sign.</span></span>  <br/> |
| <span data-ttu-id="fa238-116">_difusa_</span><span class="sxs-lookup"><span data-stu-id="fa238-116">_fuzz_</span></span> <br/> |<span data-ttu-id="fa238-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="fa238-117">Optional</span></span>  <br/> |<span data-ttu-id="fa238-118">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="fa238-118">**Numeric**</span></span> <br/> |<span data-ttu-id="fa238-119">Especifica o quanto o número deve estar próximo do zero para ser considerado igual a zero.</span><span class="sxs-lookup"><span data-stu-id="fa238-119">Specifies how close to zero the number must be in order to be considered equal to zero.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fa238-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fa238-120">Return value</span></span>

<span data-ttu-id="fa238-121">Numeric</span><span class="sxs-lookup"><span data-stu-id="fa238-121">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa238-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa238-122">Remarks</span></span>

<span data-ttu-id="fa238-123">A função SIGN retornará 1 se _núm_ for positivo, 0 se _núm_ for zero ou-1 se _núm_ for negativo.</span><span class="sxs-lookup"><span data-stu-id="fa238-123">The SIGN function returns 1 if  _number_ is positive, 0 if  _number_ is zero, or -1 if  _number_ is negative.</span></span> 
  
<span data-ttu-id="fa238-124">Especificar um valor de _difusão_ ajuda a evitar erros de ponto flutuante roundoff quando um cálculo é quase zero.</span><span class="sxs-lookup"><span data-stu-id="fa238-124">Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero.</span></span> <span data-ttu-id="fa238-125">Se você não especificar um valor de _difusão_ , o Visio usará 1e-9 (0, 1).</span><span class="sxs-lookup"><span data-stu-id="fa238-125">If you do not specify a  _fuzz_ value, Visio uses 1E-9 (0.000000001).</span></span> <span data-ttu-id="fa238-126">Convém fornecer um valor diferente ao colocar o desenho em escala ou quando desejar obter uma comparação exata.</span><span class="sxs-lookup"><span data-stu-id="fa238-126">You may want to supply a different value when you scale drawings or when you want an exact comparison.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fa238-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fa238-127">Example 1</span></span>

<span data-ttu-id="fa238-128">SINAL (-5)</span><span class="sxs-lookup"><span data-stu-id="fa238-128">SIGN(-5)</span></span>
  
<span data-ttu-id="fa238-129">Retornará -1.</span><span class="sxs-lookup"><span data-stu-id="fa238-129">Returns -1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fa238-130">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fa238-130">Example 2</span></span>

<span data-ttu-id="fa238-131">SINAL (0)</span><span class="sxs-lookup"><span data-stu-id="fa238-131">SIGN(0)</span></span>
  
<span data-ttu-id="fa238-132">Retornará 0.</span><span class="sxs-lookup"><span data-stu-id="fa238-132">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fa238-133">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fa238-133">Example 3</span></span>

<span data-ttu-id="fa238-134">SINAL (0.00000000001)</span><span class="sxs-lookup"><span data-stu-id="fa238-134">SIGN(0.00000000001)</span></span>
  
<span data-ttu-id="fa238-135">Retornará 0.</span><span class="sxs-lookup"><span data-stu-id="fa238-135">Returns 0.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="fa238-136">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="fa238-136">Example 4</span></span>

<span data-ttu-id="fa238-137">SINAL (0.00000000001, 0)</span><span class="sxs-lookup"><span data-stu-id="fa238-137">SIGN(0.00000000001,0)</span></span>
  
<span data-ttu-id="fa238-138">Retornará 1.</span><span class="sxs-lookup"><span data-stu-id="fa238-138">Returns 1.</span></span>
  

