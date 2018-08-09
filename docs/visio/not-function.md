---
title: Função NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Retorna verdadeiro (1) se logicalexpression for FALSE. Caso contrário, ele retornará FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772419"
---
# <a name="not-function"></a><span data-ttu-id="8a001-104">Função NOT</span><span class="sxs-lookup"><span data-stu-id="8a001-104">NOT Function</span></span>

<span data-ttu-id="8a001-105">Retorna verdadeiro (1) se _logicalexpression_ for FALSE.</span><span class="sxs-lookup"><span data-stu-id="8a001-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="8a001-106">Caso contrário, ele retornará FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="8a001-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8a001-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a001-107">Syntax</span></span>

<span data-ttu-id="8a001-108">NÃO (* * *logicalexpression* * *)</span><span class="sxs-lookup"><span data-stu-id="8a001-108">NOT(** *logicalexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8a001-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a001-109">Parameters</span></span>

|<span data-ttu-id="8a001-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8a001-110">**Name**</span></span>|<span data-ttu-id="8a001-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8a001-111">**Required/Optional**</span></span>|<span data-ttu-id="8a001-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8a001-112">**Data Type**</span></span>|<span data-ttu-id="8a001-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8a001-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8a001-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="8a001-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="8a001-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8a001-115">Required</span></span>  <br/> |<span data-ttu-id="8a001-116">**String**</span><span class="sxs-lookup"><span data-stu-id="8a001-116">**String**</span></span> <br/> |<span data-ttu-id="8a001-117">A expressão lógica a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="8a001-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8a001-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8a001-118">Return value</span></span>

<span data-ttu-id="8a001-119">Booliano</span><span class="sxs-lookup"><span data-stu-id="8a001-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="8a001-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8a001-120">Example</span></span>

<span data-ttu-id="8a001-121">NÃO (altura \> 0,75 pol)</span><span class="sxs-lookup"><span data-stu-id="8a001-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="8a001-p103">Retorna 1 se a Altura for menor que ou igual a 0,75 polegadas. Retorna 0 se a Altura for maior que 0,75 polegadas.</span><span class="sxs-lookup"><span data-stu-id="8a001-p103">Returns 1 if Height is less than or equal to 0.75 inches. Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

