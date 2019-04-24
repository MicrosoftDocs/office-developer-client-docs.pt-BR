---
title: Função BITAND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente em ambos binarynumber1 e binarynumber2 for 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284466"
---
# <a name="bitand-function"></a><span data-ttu-id="ecb4a-104">Função BITAND</span><span class="sxs-lookup"><span data-stu-id="ecb4a-104">BITAND Function</span></span>

<span data-ttu-id="ecb4a-105">Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente em ambos binarynumber1 e binarynumber2 for 1.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="ecb4a-106">Caso contrário, o bit será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ecb4a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecb4a-107">Syntax</span></span>

<span data-ttu-id="ecb4a-108">BITAND (\* \* *binarynumber1* \* \*, \* \* *binarynumber2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ecb4a-108">BITAND(\*\* *binarynumber1* \*\*, \*\* *binarynumber2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ecb4a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecb4a-109">Parameters</span></span>

|<span data-ttu-id="ecb4a-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ecb4a-110">**Name**</span></span>|<span data-ttu-id="ecb4a-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ecb4a-111">**Required/Optional**</span></span>|<span data-ttu-id="ecb4a-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ecb4a-112">**Data Type**</span></span>|<span data-ttu-id="ecb4a-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ecb4a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ecb4a-114">_Número1 binário_</span><span class="sxs-lookup"><span data-stu-id="ecb4a-114">_binary number1_</span></span> <br/> |<span data-ttu-id="ecb4a-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ecb4a-115">Required</span></span>  <br/> |<span data-ttu-id="ecb4a-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ecb4a-116">**Numeric**</span></span> <br/> |<span data-ttu-id="ecb4a-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="ecb4a-118">_número2 binário_</span><span class="sxs-lookup"><span data-stu-id="ecb4a-118">_binary number2_</span></span> <br/> |<span data-ttu-id="ecb4a-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ecb4a-119">Required</span></span>  <br/> |<span data-ttu-id="ecb4a-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ecb4a-120">**Numeric**</span></span> <br/> |<span data-ttu-id="ecb4a-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecb4a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecb4a-122">Remarks</span></span>

<span data-ttu-id="ecb4a-123">É possível usar esta função para testar e alterar propriedades de uma forma armazenadas como bitmasks, por exemplo, o formato do texto da célula.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="ecb4a-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ecb4a-124">Example</span></span>

<span data-ttu-id="ecb4a-125">BITAND (12, 6)</span><span class="sxs-lookup"><span data-stu-id="ecb4a-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="ecb4a-p103">Retornará 4. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="ecb4a-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

