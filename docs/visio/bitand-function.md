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
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente em númerobinário1 e númerobinário2 é 1. Caso contrário, o bit é definido como 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771365"
---
# <a name="bitand-function"></a><span data-ttu-id="2aa14-104">Função BITAND</span><span class="sxs-lookup"><span data-stu-id="2aa14-104">BITAND Function</span></span>

<span data-ttu-id="2aa14-105">Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente em númerobinário1 e númerobinário2 é 1.</span><span class="sxs-lookup"><span data-stu-id="2aa14-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="2aa14-106">Caso contrário, o bit é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="2aa14-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2aa14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aa14-107">Syntax</span></span>

<span data-ttu-id="2aa14-108">BITAND (* * *númerobinário1* * *, * * *númerobinário2* * *)</span><span class="sxs-lookup"><span data-stu-id="2aa14-108">BITAND(** *binarynumber1* **, ** *binarynumber2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2aa14-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2aa14-109">Parameters</span></span>

|<span data-ttu-id="2aa14-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2aa14-110">**Name**</span></span>|<span data-ttu-id="2aa14-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="2aa14-111">**Required/Optional**</span></span>|<span data-ttu-id="2aa14-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2aa14-112">**Data Type**</span></span>|<span data-ttu-id="2aa14-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2aa14-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2aa14-114">_Número1 binários_</span><span class="sxs-lookup"><span data-stu-id="2aa14-114">_binary number1_</span></span> <br/> |<span data-ttu-id="2aa14-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2aa14-115">Required</span></span>  <br/> |<span data-ttu-id="2aa14-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="2aa14-116">**Numeric**</span></span> <br/> |<span data-ttu-id="2aa14-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2aa14-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="2aa14-118">_binário 2_</span><span class="sxs-lookup"><span data-stu-id="2aa14-118">_binary number2_</span></span> <br/> |<span data-ttu-id="2aa14-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2aa14-119">Required</span></span>  <br/> |<span data-ttu-id="2aa14-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="2aa14-120">**Numeric**</span></span> <br/> |<span data-ttu-id="2aa14-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2aa14-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aa14-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aa14-122">Remarks</span></span>

<span data-ttu-id="2aa14-123">É possível usar esta função para testar e alterar propriedades de uma forma armazenadas como bitmasks, por exemplo, o formato do texto da célula.</span><span class="sxs-lookup"><span data-stu-id="2aa14-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="2aa14-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2aa14-124">Example</span></span>

<span data-ttu-id="2aa14-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="2aa14-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="2aa14-p103">Retornará 4. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITAND(12,6) = 0...00100.</span><span class="sxs-lookup"><span data-stu-id="2aa14-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

