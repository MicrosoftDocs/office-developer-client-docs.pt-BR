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
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente no número binário ou no número binário núm2 for 1. O bit é definido como 0 somente se o bit correspondente for 0 no Número1 binário e no número2 binário.
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408079"
---
# <a name="bitor-function"></a><span data-ttu-id="a0b4d-104">Função BITOR</span><span class="sxs-lookup"><span data-stu-id="a0b4d-104">BITOR Function</span></span>

<span data-ttu-id="a0b4d-105">Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente no número *binário* ou no número *binário núm2* for 1.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="a0b4d-106">O bit é definido como 0 somente se o bit correspondente for 0 no *Número1 binário* e no *número2 binário* .</span><span class="sxs-lookup"><span data-stu-id="a0b4d-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0b4d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0b4d-107">Syntax</span></span>

<span data-ttu-id="a0b4d-108">BITOR (\* \* *binário Número1* \* \*, \* \* *binário núm2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a0b4d-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a0b4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0b4d-109">Parameters</span></span>

|<span data-ttu-id="a0b4d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0b4d-110">**Name**</span></span>|<span data-ttu-id="a0b4d-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a0b4d-111">**Required/Optional**</span></span>|<span data-ttu-id="a0b4d-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a0b4d-112">**Data Type**</span></span>|<span data-ttu-id="a0b4d-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a0b4d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0b4d-114">_Número1 binário_</span><span class="sxs-lookup"><span data-stu-id="a0b4d-114">_binary number1_</span></span> <br/> |<span data-ttu-id="a0b4d-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a0b4d-115">Required</span></span>  <br/> |<span data-ttu-id="a0b4d-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="a0b4d-116">**Numeric**</span></span> <br/> |<span data-ttu-id="a0b4d-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="a0b4d-118">_número2 binário_</span><span class="sxs-lookup"><span data-stu-id="a0b4d-118">_binary number2_</span></span> <br/> |<span data-ttu-id="a0b4d-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a0b4d-119">Required</span></span>  <br/> |<span data-ttu-id="a0b4d-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="a0b4d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="a0b4d-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a0b4d-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a0b4d-122">Return value</span></span>

<span data-ttu-id="a0b4d-123">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="a0b4d-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="a0b4d-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a0b4d-124">Example</span></span>

<span data-ttu-id="a0b4d-125">BITOR (12, 6)</span><span class="sxs-lookup"><span data-stu-id="a0b4d-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="a0b4d-p103">Retornará 14. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITOR(12,6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="a0b4d-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

