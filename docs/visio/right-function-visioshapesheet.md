---
title: Função RIGHT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Retorna o último caractere ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411453"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="43750-103">Função RIGHT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="43750-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="43750-104">Retorna o último caractere ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="43750-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="43750-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43750-105">Syntax</span></span>

<span data-ttu-id="43750-106">Right (\* \* *Text* \* \* [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="43750-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="43750-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43750-107">Parameters</span></span>

|<span data-ttu-id="43750-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="43750-108">**Name**</span></span>|<span data-ttu-id="43750-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="43750-109">**Required/Optional**</span></span>|<span data-ttu-id="43750-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="43750-110">**Data Type**</span></span>|<span data-ttu-id="43750-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43750-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="43750-112">_text_</span><span class="sxs-lookup"><span data-stu-id="43750-112">_text_</span></span> <br/> |<span data-ttu-id="43750-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="43750-113">Required</span></span>  <br/> |<span data-ttu-id="43750-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43750-114">**String**</span></span> <br/> | <span data-ttu-id="43750-115">A cadeia de caracteres de texto que contém os caracteres a serem extraídos.</span><span class="sxs-lookup"><span data-stu-id="43750-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="43750-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="43750-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="43750-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="43750-117">Optional</span></span>  <br/> |<span data-ttu-id="43750-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="43750-118">**Number**</span></span> <br/> |<span data-ttu-id="43750-119">O número de caracteres que deseja extrair.</span><span class="sxs-lookup"><span data-stu-id="43750-119">The number of characters you want to extract.</span></span> <span data-ttu-id="43750-120">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="43750-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="43750-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="43750-121">Return value</span></span>

<span data-ttu-id="43750-122">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="43750-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43750-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="43750-123">Remarks</span></span>

<span data-ttu-id="43750-124">O valor de _num_chars_opt_ deve ser maior ou igual a zero (0).</span><span class="sxs-lookup"><span data-stu-id="43750-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="43750-125">Se _num_chars_opt_ for maior do que o comprimento do texto, Right retornará todo o texto.</span><span class="sxs-lookup"><span data-stu-id="43750-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="43750-126">Se _num_chars_opt_ for omitido, será considerado 1.</span><span class="sxs-lookup"><span data-stu-id="43750-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="43750-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="43750-127">Example</span></span>

<span data-ttu-id="43750-128">RIGHT ("1º de janeiro de 2004", 4)</span><span class="sxs-lookup"><span data-stu-id="43750-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="43750-129">Retornará o valor 2004.</span><span class="sxs-lookup"><span data-stu-id="43750-129">Returns the value 2004.</span></span> 
  

