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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303371"
---
# <a name="bitor-function"></a><span data-ttu-id="5afc2-104">Função BITOR</span><span class="sxs-lookup"><span data-stu-id="5afc2-104">BITOR Function</span></span>

<span data-ttu-id="5afc2-105">Retorna um número binário de 16 bits em que cada bit é definido como 1 se o bit correspondente no número *binário* ou no número *binário núm2* for 1.</span><span class="sxs-lookup"><span data-stu-id="5afc2-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="5afc2-106">O bit é definido como 0 somente se o bit correspondente for 0 no *Número1 binário* e no *número2 binário* .</span><span class="sxs-lookup"><span data-stu-id="5afc2-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5afc2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5afc2-107">Syntax</span></span>

<span data-ttu-id="5afc2-108">BITOR (\* \* *binário Número1* \* \*, \* \* *binário núm2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5afc2-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5afc2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5afc2-109">Parameters</span></span>

|<span data-ttu-id="5afc2-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5afc2-110">**Name**</span></span>|<span data-ttu-id="5afc2-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="5afc2-111">**Required/Optional**</span></span>|<span data-ttu-id="5afc2-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="5afc2-112">**Data Type**</span></span>|<span data-ttu-id="5afc2-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5afc2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5afc2-114">_Número1 binário_</span><span class="sxs-lookup"><span data-stu-id="5afc2-114">_binary number1_</span></span> <br/> |<span data-ttu-id="5afc2-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5afc2-115">Required</span></span>  <br/> |<span data-ttu-id="5afc2-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="5afc2-116">**Numeric**</span></span> <br/> |<span data-ttu-id="5afc2-117">O primeiro número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5afc2-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="5afc2-118">_número2 binário_</span><span class="sxs-lookup"><span data-stu-id="5afc2-118">_binary number2_</span></span> <br/> |<span data-ttu-id="5afc2-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5afc2-119">Required</span></span>  <br/> |<span data-ttu-id="5afc2-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="5afc2-120">**Numeric**</span></span> <br/> |<span data-ttu-id="5afc2-121">O segundo número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5afc2-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5afc2-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5afc2-122">Return value</span></span>

<span data-ttu-id="5afc2-123">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="5afc2-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="5afc2-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5afc2-124">Example</span></span>

<span data-ttu-id="5afc2-125">BITOR (12, 6)</span><span class="sxs-lookup"><span data-stu-id="5afc2-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="5afc2-p103">Retornará 14. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITOR(12,6) = 0...01110.</span><span class="sxs-lookup"><span data-stu-id="5afc2-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

