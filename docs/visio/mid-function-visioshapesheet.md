---
title: Função MID (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Retorna um número específico de caracteres de uma cadeia de caracteres de texto, começando na posição especificada, com base no número de caracteres especificado.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410263"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="fbc28-103">Função MID (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fbc28-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fbc28-104">Retorna um número específico de caracteres de uma cadeia de caracteres de texto, começando na posição especificada, com base no número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="fbc28-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fbc28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbc28-105">Syntax</span></span>

<span data-ttu-id="fbc28-106">MID (\*\* *texto* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span><span class="sxs-lookup"><span data-stu-id="fbc28-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fbc28-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbc28-107">Parameters</span></span>

|<span data-ttu-id="fbc28-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fbc28-108">**Name**</span></span>|<span data-ttu-id="fbc28-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="fbc28-109">**Required/Optional**</span></span>|<span data-ttu-id="fbc28-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="fbc28-110">**Data Type**</span></span>|<span data-ttu-id="fbc28-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbc28-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fbc28-112">_text_</span><span class="sxs-lookup"><span data-stu-id="fbc28-112">_text_</span></span> <br/> |<span data-ttu-id="fbc28-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbc28-113">Required</span></span>  <br/> |<span data-ttu-id="fbc28-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fbc28-114">**String**</span></span> <br/> |<span data-ttu-id="fbc28-115">A cadeia de caracteres de texto que contém os caracteres a serem extraídos.</span><span class="sxs-lookup"><span data-stu-id="fbc28-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="fbc28-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="fbc28-116">_start_num_</span></span> <br/> |<span data-ttu-id="fbc28-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbc28-117">Required</span></span>  <br/> |<span data-ttu-id="fbc28-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="fbc28-118">**Number**</span></span> <br/> |<span data-ttu-id="fbc28-119">A posição do primeiro caractere a ser extraído.</span><span class="sxs-lookup"><span data-stu-id="fbc28-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="fbc28-120">O primeiro caractere na cadeia de caracteres de texto está na posição 1.</span><span class="sxs-lookup"><span data-stu-id="fbc28-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="fbc28-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="fbc28-121">_num_chars_</span></span> <br/> |<span data-ttu-id="fbc28-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbc28-122">Required</span></span>  <br/> |<span data-ttu-id="fbc28-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="fbc28-123">**Number**</span></span> <br/> |<span data-ttu-id="fbc28-124">O número de caracteres a retornar.</span><span class="sxs-lookup"><span data-stu-id="fbc28-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fbc28-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fbc28-125">Return value</span></span>

<span data-ttu-id="fbc28-126">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="fbc28-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbc28-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbc28-127">Remarks</span></span>

<span data-ttu-id="fbc28-128">Se  *start_num*  for:</span><span class="sxs-lookup"><span data-stu-id="fbc28-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="fbc28-129">Maior que o comprimento do  *texto,*  MID retornará "" (texto vazio).</span><span class="sxs-lookup"><span data-stu-id="fbc28-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="fbc28-130">Menor que o comprimento do  *texto,*  mas  *start_num*  mais  *num_chars*  exceder o comprimento do texto  *,*  MID retorna os caracteres até o final do  *texto*  .</span><span class="sxs-lookup"><span data-stu-id="fbc28-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="fbc28-131">Menor que 1, MID retornará o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fbc28-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="fbc28-132">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="fbc28-132">error value.</span></span> 
    
<span data-ttu-id="fbc28-133">Se  *num_chars*  for negativo, MID retornará a #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fbc28-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="fbc28-134">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="fbc28-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fbc28-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fbc28-135">Example</span></span>

<span data-ttu-id="fbc28-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="fbc28-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="fbc28-137">Retorna 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="fbc28-137">Returns 999-99-9999.</span></span> 
  

