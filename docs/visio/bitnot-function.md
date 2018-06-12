---
title: Função BITNOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente no número binário for 0. Caso contrário, o bit é definido como 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771340"
---
# <a name="bitnot-function"></a><span data-ttu-id="a74bb-104">Função BITNOT</span><span class="sxs-lookup"><span data-stu-id="a74bb-104">BITNOT Function</span></span>

<span data-ttu-id="a74bb-105">Retorna um número binário de 16 bits no qual cada bit for definido como 1 somente se o bit correspondente no número binário for 0.</span><span class="sxs-lookup"><span data-stu-id="a74bb-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="a74bb-106">Caso contrário, o bit é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="a74bb-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a74bb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a74bb-107">Syntax</span></span>

<span data-ttu-id="a74bb-108">BITNOT (* * *número binário* * *)</span><span class="sxs-lookup"><span data-stu-id="a74bb-108">BITNOT(** *binary number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a74bb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a74bb-109">Parameters</span></span>

|<span data-ttu-id="a74bb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a74bb-110">**Name**</span></span>|<span data-ttu-id="a74bb-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a74bb-111">**Required/Optional**</span></span>|<span data-ttu-id="a74bb-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a74bb-112">**Data Type**</span></span>|<span data-ttu-id="a74bb-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a74bb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a74bb-114">_número binário_</span><span class="sxs-lookup"><span data-stu-id="a74bb-114">_binary number_</span></span> <br/> |<span data-ttu-id="a74bb-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a74bb-115">Required</span></span>  <br/> |<span data-ttu-id="a74bb-116">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="a74bb-116">**Numeric**</span></span> <br/> |<span data-ttu-id="a74bb-117">Um número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a74bb-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a74bb-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a74bb-118">Return value</span></span>

<span data-ttu-id="a74bb-119">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="a74bb-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="a74bb-120">Example</span><span class="sxs-lookup"><span data-stu-id="a74bb-120">Example</span></span>

<span data-ttu-id="a74bb-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="a74bb-121">BITNOT(6)</span></span>
  
<span data-ttu-id="a74bb-p103">Retornará 65529. Se 6 = 0...00110; consequentemente, BITNOT(6) = 1...11001.</span><span class="sxs-lookup"><span data-stu-id="a74bb-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

