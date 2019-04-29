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
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente em ambos, mas não no número binário e no número binário núm2 é 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439230"
---
# <a name="bitxor-function"></a><span data-ttu-id="23b3e-104">Função BITXOR</span><span class="sxs-lookup"><span data-stu-id="23b3e-104">BITXOR Function</span></span>

<span data-ttu-id="23b3e-105">Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente em ambos, mas não no número binário e no número binário núm2 é 1.</span><span class="sxs-lookup"><span data-stu-id="23b3e-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="23b3e-106">Caso contrário, o bit será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="23b3e-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="23b3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b3e-107">Syntax</span></span>

<span data-ttu-id="23b3e-108">BITXOR (\* \* *binário Número1* \* \*, \* \* *binário núm2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="23b3e-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="23b3e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23b3e-109">Parameters</span></span>

|<span data-ttu-id="23b3e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="23b3e-110">**Name**</span></span>|<span data-ttu-id="23b3e-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="23b3e-111">**Required/Optional**</span></span>|<span data-ttu-id="23b3e-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="23b3e-112">**Data Type**</span></span>|<span data-ttu-id="23b3e-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23b3e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="23b3e-114">_Número1 binário_</span><span class="sxs-lookup"><span data-stu-id="23b3e-114">_binary number1_</span></span> <br/> |<span data-ttu-id="23b3e-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="23b3e-115">Required</span></span>  <br/> |<span data-ttu-id="23b3e-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="23b3e-116">**Numeric**</span></span> <br/> |<span data-ttu-id="23b3e-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="23b3e-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="23b3e-118">_número2 binário_</span><span class="sxs-lookup"><span data-stu-id="23b3e-118">_binary number2_</span></span> <br/> |<span data-ttu-id="23b3e-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="23b3e-119">Required</span></span>  <br/> |<span data-ttu-id="23b3e-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="23b3e-120">**Numeric**</span></span> <br/> |<span data-ttu-id="23b3e-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="23b3e-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="23b3e-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="23b3e-122">Return value</span></span>

<span data-ttu-id="23b3e-123">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="23b3e-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="23b3e-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="23b3e-124">Example</span></span>

<span data-ttu-id="23b3e-125">BITXOR (12, 6)</span><span class="sxs-lookup"><span data-stu-id="23b3e-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="23b3e-p103">Retornará 10. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="23b3e-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

