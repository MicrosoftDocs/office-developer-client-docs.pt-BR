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
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772395"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="fbf5f-103">Função MID (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fbf5f-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fbf5f-104">Retorna um número específico de caracteres de uma cadeia de caracteres de texto, começando na posição especificada, com base no número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="fbf5f-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fbf5f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbf5f-105">Syntax</span></span>

<span data-ttu-id="fbf5f-106">MID (* * *texto* * *, * * *Núm_inicial* * *, * * *Núm_caract* * *)</span><span class="sxs-lookup"><span data-stu-id="fbf5f-106">MID (** *text* **, ** *start_num* **, ** *num_chars* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fbf5f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbf5f-107">Parameters</span></span>

|<span data-ttu-id="fbf5f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-108">**Name**</span></span>|<span data-ttu-id="fbf5f-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-109">**Required/Optional**</span></span>|<span data-ttu-id="fbf5f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-110">**Data Type**</span></span>|<span data-ttu-id="fbf5f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fbf5f-112">_text_</span><span class="sxs-lookup"><span data-stu-id="fbf5f-112">_text_</span></span> <br/> |<span data-ttu-id="fbf5f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbf5f-113">Required</span></span>  <br/> |<span data-ttu-id="fbf5f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-114">**String**</span></span> <br/> |<span data-ttu-id="fbf5f-115">A cadeia de caracteres de texto que contém os caracteres a serem extraídos.</span><span class="sxs-lookup"><span data-stu-id="fbf5f-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="fbf5f-116">_Núm_inicial_</span><span class="sxs-lookup"><span data-stu-id="fbf5f-116">_start_num_</span></span> <br/> |<span data-ttu-id="fbf5f-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbf5f-117">Required</span></span>  <br/> |<span data-ttu-id="fbf5f-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-118">**Number**</span></span> <br/> |<span data-ttu-id="fbf5f-p101">A posição do primeiro caractere a ser extraído. O primeiro caractere na cadeia de caracteres de texto está na posição 1.</span><span class="sxs-lookup"><span data-stu-id="fbf5f-p101">The position of the first character you want to extract. The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="fbf5f-121">_Núm_caract_</span><span class="sxs-lookup"><span data-stu-id="fbf5f-121">_num_chars_</span></span> <br/> |<span data-ttu-id="fbf5f-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="fbf5f-122">Required</span></span>  <br/> |<span data-ttu-id="fbf5f-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="fbf5f-123">**Number**</span></span> <br/> |<span data-ttu-id="fbf5f-124">O número de caracteres a retornar.</span><span class="sxs-lookup"><span data-stu-id="fbf5f-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fbf5f-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fbf5f-125">Return value</span></span>

<span data-ttu-id="fbf5f-126">String</span><span class="sxs-lookup"><span data-stu-id="fbf5f-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbf5f-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbf5f-127">Remarks</span></span>

<span data-ttu-id="fbf5f-128">Se *Núm_inicial* for:</span><span class="sxs-lookup"><span data-stu-id="fbf5f-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="fbf5f-129">Maior que o comprimento de *text* , MID retornará "" (texto vazio).</span><span class="sxs-lookup"><span data-stu-id="fbf5f-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="fbf5f-130">Menor que o comprimento do *texto* , mas se *start_num* mais *num_chars* ultrapassarem o comprimento de *text* , MID retornará os caracteres até o final do *texto* .</span><span class="sxs-lookup"><span data-stu-id="fbf5f-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="fbf5f-p102">Menor que 1, MID retornará o valor de erro #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fbf5f-p102">Less than 1, MID returns the #VALUE! error value.</span></span> 
    
<span data-ttu-id="fbf5f-133">Se *num_chars* for negativo, MID retornará o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fbf5f-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="fbf5f-134">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="fbf5f-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fbf5f-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fbf5f-135">Example</span></span>

<span data-ttu-id="fbf5f-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="fbf5f-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="fbf5f-137">Retorna 999-99-9999.</span><span class="sxs-lookup"><span data-stu-id="fbf5f-137">Returns 999-99-9999.</span></span> 
  

