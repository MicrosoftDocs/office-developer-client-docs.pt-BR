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
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293489"
---
# <a name="bitand-function"></a><span data-ttu-id="dba21-104">Função BITAND</span><span class="sxs-lookup"><span data-stu-id="dba21-104">BITAND Function</span></span>

<span data-ttu-id="dba21-105">Retorna um número binário de 16 bits em que cada bit é definido como 1 somente se o bit correspondente em ambos binarynumber1 e binarynumber2 for 1.</span><span class="sxs-lookup"><span data-stu-id="dba21-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="dba21-106">Caso contrário, o bit será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="dba21-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dba21-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dba21-107">Syntax</span></span>

<span data-ttu-id="dba21-108">BITAND (***binarynumber1***, ***binarynumber2*** )</span><span class="sxs-lookup"><span data-stu-id="dba21-108">BITAND(***binarynumber1***, ***binarynumber2*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dba21-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dba21-109">Parameters</span></span>

|<span data-ttu-id="dba21-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dba21-110">**Name**</span></span>|<span data-ttu-id="dba21-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="dba21-111">**Required/Optional**</span></span>|<span data-ttu-id="dba21-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="dba21-112">**Data Type**</span></span>|<span data-ttu-id="dba21-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dba21-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dba21-114">_Número1 binário_</span><span class="sxs-lookup"><span data-stu-id="dba21-114">_binary number1_</span></span> <br/> |<span data-ttu-id="dba21-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dba21-115">Required</span></span>  <br/> |<span data-ttu-id="dba21-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="dba21-116">**Numeric**</span></span> <br/> |<span data-ttu-id="dba21-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="dba21-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="dba21-118">_número2 binário_</span><span class="sxs-lookup"><span data-stu-id="dba21-118">_binary number2_</span></span> <br/> |<span data-ttu-id="dba21-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dba21-119">Required</span></span>  <br/> |<span data-ttu-id="dba21-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="dba21-120">**Numeric**</span></span> <br/> |<span data-ttu-id="dba21-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="dba21-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dba21-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="dba21-122">Remarks</span></span>

<span data-ttu-id="dba21-123">É possível usar esta função para testar e alterar propriedades de uma forma armazenadas como bitmasks, por exemplo, o formato do texto da célula.</span><span class="sxs-lookup"><span data-stu-id="dba21-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="dba21-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dba21-124">Example</span></span>

<span data-ttu-id="dba21-125">BITAND (12, 6)</span><span class="sxs-lookup"><span data-stu-id="dba21-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="dba21-p103">Retornará 4. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="dba21-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

