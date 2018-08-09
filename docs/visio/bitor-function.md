---
title: Função BITOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em binário Número1 ou Número2 binário é 1. O bit é definido como 0 somente se o bit correspondente for 0 em binário Núm1 e núm2 binário.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771357"
---
# <a name="bitor-function"></a><span data-ttu-id="24dfb-104">Função BITOR</span><span class="sxs-lookup"><span data-stu-id="24dfb-104">BITOR Function</span></span>

<span data-ttu-id="24dfb-105">Retorna um número binário de 16 bits no qual cada bit for definido como 1 se o bit correspondente em *binário Número1* ou *número2 binário* é 1.</span><span class="sxs-lookup"><span data-stu-id="24dfb-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="24dfb-106">O bit é definido como 0 somente se o bit correspondente for 0 em *binário Núm1* e *núm2 binário* .</span><span class="sxs-lookup"><span data-stu-id="24dfb-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="24dfb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24dfb-107">Syntax</span></span>

<span data-ttu-id="24dfb-108">BITOR (* * *Número1 binário* * *, * * *binário 2* * *)</span><span class="sxs-lookup"><span data-stu-id="24dfb-108">BITOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="24dfb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24dfb-109">Parameters</span></span>

|<span data-ttu-id="24dfb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="24dfb-110">**Name**</span></span>|<span data-ttu-id="24dfb-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="24dfb-111">**Required/Optional**</span></span>|<span data-ttu-id="24dfb-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="24dfb-112">**Data Type**</span></span>|<span data-ttu-id="24dfb-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="24dfb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="24dfb-114">_Número1 binários_</span><span class="sxs-lookup"><span data-stu-id="24dfb-114">_binary number1_</span></span> <br/> |<span data-ttu-id="24dfb-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="24dfb-115">Required</span></span>  <br/> |<span data-ttu-id="24dfb-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="24dfb-116">**Numeric**</span></span> <br/> |<span data-ttu-id="24dfb-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="24dfb-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="24dfb-118">_binário 2_</span><span class="sxs-lookup"><span data-stu-id="24dfb-118">_binary number2_</span></span> <br/> |<span data-ttu-id="24dfb-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="24dfb-119">Required</span></span>  <br/> |<span data-ttu-id="24dfb-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="24dfb-120">**Numeric**</span></span> <br/> |<span data-ttu-id="24dfb-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="24dfb-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="24dfb-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="24dfb-122">Return value</span></span>

<span data-ttu-id="24dfb-123">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="24dfb-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="24dfb-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="24dfb-124">Example</span></span>

<span data-ttu-id="24dfb-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="24dfb-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="24dfb-p103">Retornará 14. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITOR(12,6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="24dfb-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

