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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412076"
---
# <a name="rept-function"></a><span data-ttu-id="2b97d-103">Função REPT</span><span class="sxs-lookup"><span data-stu-id="2b97d-103">REPT Function</span></span>

<span data-ttu-id="2b97d-104">Repete um texto um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="2b97d-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2b97d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b97d-105">Syntax</span></span>

<span data-ttu-id="2b97d-106">REPT (\*\* *texto* \*\*, \*\* *number_times* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2b97d-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2b97d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b97d-107">Parameters</span></span>

|<span data-ttu-id="2b97d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b97d-108">**Name**</span></span>|<span data-ttu-id="2b97d-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2b97d-109">**Required/Optional**</span></span>|<span data-ttu-id="2b97d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2b97d-110">**Data Type**</span></span>|<span data-ttu-id="2b97d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2b97d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2b97d-112">_text_</span><span class="sxs-lookup"><span data-stu-id="2b97d-112">_text_</span></span> <br/> |<span data-ttu-id="2b97d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2b97d-113">Required</span></span>  <br/> |<span data-ttu-id="2b97d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2b97d-114">**String**</span></span> <br/> | <span data-ttu-id="2b97d-115">O texto a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="2b97d-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="2b97d-116">_number_times_</span><span class="sxs-lookup"><span data-stu-id="2b97d-116">_number_times_</span></span> <br/> |<span data-ttu-id="2b97d-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2b97d-117">Required</span></span>  <br/> |<span data-ttu-id="2b97d-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="2b97d-118">**Number**</span></span> <br/> |<span data-ttu-id="2b97d-119">Um número positivo que especifica o número de vezes que o texto será repetido.</span><span class="sxs-lookup"><span data-stu-id="2b97d-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b97d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b97d-120">Remarks</span></span>

<span data-ttu-id="2b97d-121">Se  *number_times*  for:</span><span class="sxs-lookup"><span data-stu-id="2b97d-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="2b97d-122">For zero (0), REPT retornará "" (texto vazio).</span><span class="sxs-lookup"><span data-stu-id="2b97d-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="2b97d-123">Não for um inteiro, estará truncado.</span><span class="sxs-lookup"><span data-stu-id="2b97d-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="2b97d-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2b97d-124">Example</span></span>

<span data-ttu-id="2b97d-125">REPT (" \* ", 5)</span><span class="sxs-lookup"><span data-stu-id="2b97d-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="2b97d-126">Retorna \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="2b97d-126">Returns \*\*\*\*\*.</span></span> 
  

