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
description: Retorna um número binário de 16 bits no qual cada bit é definido como 1 somente se o bit correspondente no número binário for 0. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438831"
---
# <a name="bitnot-function"></a><span data-ttu-id="66151-104">Função BITNOT</span><span class="sxs-lookup"><span data-stu-id="66151-104">BITNOT Function</span></span>

<span data-ttu-id="66151-105">Retorna um número binário de 16 bits no qual cada bit é definido como 1 somente se o bit correspondente no número binário for 0.</span><span class="sxs-lookup"><span data-stu-id="66151-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="66151-106">Caso contrário, o bit será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="66151-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="66151-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66151-107">Syntax</span></span>

<span data-ttu-id="66151-108">BITNOT(\*\* *binary number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="66151-108">BITNOT(\*\* *binary number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66151-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66151-109">Parameters</span></span>

|<span data-ttu-id="66151-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="66151-110">**Name**</span></span>|<span data-ttu-id="66151-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="66151-111">**Required/Optional**</span></span>|<span data-ttu-id="66151-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="66151-112">**Data Type**</span></span>|<span data-ttu-id="66151-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="66151-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66151-114">_número binário_</span><span class="sxs-lookup"><span data-stu-id="66151-114">_binary number_</span></span> <br/> |<span data-ttu-id="66151-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="66151-115">Required</span></span>  <br/> |<span data-ttu-id="66151-116">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="66151-116">**Numeric**</span></span> <br/> |<span data-ttu-id="66151-117">Um número binário de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="66151-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="66151-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="66151-118">Return value</span></span>

<span data-ttu-id="66151-119">Binário de 16 bits</span><span class="sxs-lookup"><span data-stu-id="66151-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="66151-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="66151-120">Example</span></span>

<span data-ttu-id="66151-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="66151-121">BITNOT(6)</span></span>
  
<span data-ttu-id="66151-p103">Retornará 65529. Se 6 = 0...00110; consequentemente, BITNOT(6) = 1...11001.</span><span class="sxs-lookup"><span data-stu-id="66151-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

