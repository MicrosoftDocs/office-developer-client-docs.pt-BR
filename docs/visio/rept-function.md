---
title: Função REPT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Repete um texto um determinado número de vezes.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326800"
---
# <a name="rept-function"></a><span data-ttu-id="714e6-103">Função REPT</span><span class="sxs-lookup"><span data-stu-id="714e6-103">REPT Function</span></span>

<span data-ttu-id="714e6-104">Repete um texto um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="714e6-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="714e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="714e6-105">Syntax</span></span>

<span data-ttu-id="714e6-106">REPT (\* \* *texto* \* \*, \* \* *number_times* \* \*)</span><span class="sxs-lookup"><span data-stu-id="714e6-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="714e6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="714e6-107">Parameters</span></span>

|<span data-ttu-id="714e6-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="714e6-108">**Name**</span></span>|<span data-ttu-id="714e6-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="714e6-109">**Required/Optional**</span></span>|<span data-ttu-id="714e6-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="714e6-110">**Data Type**</span></span>|<span data-ttu-id="714e6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="714e6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="714e6-112">_text_</span><span class="sxs-lookup"><span data-stu-id="714e6-112">_text_</span></span> <br/> |<span data-ttu-id="714e6-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="714e6-113">Required</span></span>  <br/> |<span data-ttu-id="714e6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="714e6-114">**String**</span></span> <br/> | <span data-ttu-id="714e6-115">O texto a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="714e6-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="714e6-116">_number_times_</span><span class="sxs-lookup"><span data-stu-id="714e6-116">_number_times_</span></span> <br/> |<span data-ttu-id="714e6-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="714e6-117">Required</span></span>  <br/> |<span data-ttu-id="714e6-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="714e6-118">**Number**</span></span> <br/> |<span data-ttu-id="714e6-119">Um número positivo que especifica o número de vezes que o texto será repetido.</span><span class="sxs-lookup"><span data-stu-id="714e6-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="714e6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="714e6-120">Remarks</span></span>

<span data-ttu-id="714e6-121">Se *number_times* for:</span><span class="sxs-lookup"><span data-stu-id="714e6-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="714e6-122">For zero (0), REPT retornará "" (texto vazio).</span><span class="sxs-lookup"><span data-stu-id="714e6-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="714e6-123">Não for um inteiro, estará truncado.</span><span class="sxs-lookup"><span data-stu-id="714e6-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="714e6-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="714e6-124">Example</span></span>

<span data-ttu-id="714e6-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="714e6-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="714e6-126">\* \*Retorna \*. \* \*</span><span class="sxs-lookup"><span data-stu-id="714e6-126">Returns \*\*\*\*\*.</span></span> 
  

