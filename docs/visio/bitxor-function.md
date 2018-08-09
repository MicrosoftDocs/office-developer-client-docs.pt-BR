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
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em ambos, mas não ambos binário Núm1 e núm2 binário é 1. Caso contrário, o bit é definido como 0.
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771376"
---
# <a name="bitxor-function"></a><span data-ttu-id="1a668-104">Função BITXOR</span><span class="sxs-lookup"><span data-stu-id="1a668-104">BITXOR Function</span></span>

<span data-ttu-id="1a668-105">Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em ambos, mas não ambos binário Núm1 e núm2 binário é 1.</span><span class="sxs-lookup"><span data-stu-id="1a668-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="1a668-106">Caso contrário, o bit é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="1a668-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1a668-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a668-107">Syntax</span></span>

<span data-ttu-id="1a668-108">BITXOR (* * *Número1 binário* * *, * * *binário 2* * *)</span><span class="sxs-lookup"><span data-stu-id="1a668-108">BITXOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1a668-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a668-109">Parameters</span></span>

|<span data-ttu-id="1a668-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="1a668-110">**Name**</span></span>|<span data-ttu-id="1a668-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="1a668-111">**Required/Optional**</span></span>|<span data-ttu-id="1a668-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="1a668-112">**Data Type**</span></span>|<span data-ttu-id="1a668-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1a668-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1a668-114">_Número1 binários_</span><span class="sxs-lookup"><span data-stu-id="1a668-114">_binary number1_</span></span> <br/> |<span data-ttu-id="1a668-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1a668-115">Required</span></span>  <br/> |<span data-ttu-id="1a668-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="1a668-116">**Numeric**</span></span> <br/> |<span data-ttu-id="1a668-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1a668-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="1a668-118">_binário 2_</span><span class="sxs-lookup"><span data-stu-id="1a668-118">_binary number2_</span></span> <br/> |<span data-ttu-id="1a668-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1a668-119">Required</span></span>  <br/> |<span data-ttu-id="1a668-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="1a668-120">**Numeric**</span></span> <br/> |<span data-ttu-id="1a668-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1a668-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1a668-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1a668-122">Return value</span></span>

<span data-ttu-id="1a668-123">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="1a668-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="1a668-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1a668-124">Example</span></span>

<span data-ttu-id="1a668-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="1a668-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="1a668-p103">Retornará 10. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="1a668-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

