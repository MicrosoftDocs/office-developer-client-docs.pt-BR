---
title: Função BITXOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Retorna um número binário de 16 bits no qual cada bit é definido como 1 se o bit correspondente em um deles, mas não o número binário1 e o número binário2 for 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439230"
---
# <a name="bitxor-function"></a><span data-ttu-id="2e920-104">Função BITXOR</span><span class="sxs-lookup"><span data-stu-id="2e920-104">BITXOR Function</span></span>

<span data-ttu-id="2e920-105">Retorna um número binário de 16 bits no qual cada bit é definido como 1 se o bit correspondente em um deles, mas não o número binário1 e o número binário2 for 1.</span><span class="sxs-lookup"><span data-stu-id="2e920-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="2e920-106">Caso contrário, o bit será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="2e920-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2e920-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e920-107">Syntax</span></span>

<span data-ttu-id="2e920-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2e920-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e920-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e920-109">Parameters</span></span>

|<span data-ttu-id="2e920-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e920-110">**Name**</span></span>|<span data-ttu-id="2e920-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2e920-111">**Required/Optional**</span></span>|<span data-ttu-id="2e920-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2e920-112">**Data Type**</span></span>|<span data-ttu-id="2e920-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2e920-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e920-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="2e920-114">_binary number1_</span></span> <br/> |<span data-ttu-id="2e920-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2e920-115">Required</span></span>  <br/> |<span data-ttu-id="2e920-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="2e920-116">**Numeric**</span></span> <br/> |<span data-ttu-id="2e920-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e920-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="2e920-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="2e920-118">_binary number2_</span></span> <br/> |<span data-ttu-id="2e920-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2e920-119">Required</span></span>  <br/> |<span data-ttu-id="2e920-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="2e920-120">**Numeric**</span></span> <br/> |<span data-ttu-id="2e920-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2e920-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2e920-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2e920-122">Return value</span></span>

<span data-ttu-id="2e920-123">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="2e920-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="2e920-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2e920-124">Example</span></span>

<span data-ttu-id="2e920-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="2e920-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="2e920-p103">Retornará 10. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="2e920-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

