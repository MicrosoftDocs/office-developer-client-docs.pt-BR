---
title: Função LEFT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Retorna os caracteres mais à esquerda em uma sequência de caracteres de texto, com base no número de caracteres especificado.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309461"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="c186c-103">Função LEFT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c186c-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c186c-104">Retorna os caracteres mais à esquerda em uma sequência de caracteres de texto, com base no número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="c186c-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c186c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c186c-105">Syntax</span></span>

<span data-ttu-id="c186c-106">Left (\* \* *Text* \* \*, [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="c186c-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c186c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c186c-107">Parameters</span></span>

|<span data-ttu-id="c186c-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c186c-108">**Name**</span></span>|<span data-ttu-id="c186c-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="c186c-109">**Required/Optional**</span></span>|<span data-ttu-id="c186c-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c186c-110">**Data Type**</span></span>|<span data-ttu-id="c186c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c186c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c186c-112">_text_</span><span class="sxs-lookup"><span data-stu-id="c186c-112">_text_</span></span> <br/> |<span data-ttu-id="c186c-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c186c-113">Required</span></span>  <br/> |<span data-ttu-id="c186c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c186c-114">**String**</span></span> <br/> |<span data-ttu-id="c186c-115">A cadeia de caracteres de texto que contém os caracteres a serem extraídos.</span><span class="sxs-lookup"><span data-stu-id="c186c-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="c186c-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="c186c-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="c186c-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="c186c-117">Optional</span></span>  <br/> |<span data-ttu-id="c186c-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="c186c-118">**Numeric**</span></span> <br/> |<span data-ttu-id="c186c-119">O número de caracteres que deseja extrair.</span><span class="sxs-lookup"><span data-stu-id="c186c-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c186c-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c186c-120">Return value</span></span>

<span data-ttu-id="c186c-121">String</span><span class="sxs-lookup"><span data-stu-id="c186c-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c186c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c186c-122">Remarks</span></span>

<span data-ttu-id="c186c-123">O valor de _num_chars_opt_ deve ser maior ou igual a zero (0).</span><span class="sxs-lookup"><span data-stu-id="c186c-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="c186c-124">Se _num_chars_opt_ for maior do que o comprimento do texto, Left retornará todo o texto.</span><span class="sxs-lookup"><span data-stu-id="c186c-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="c186c-125">Se _num_chars_opt_ for omitido, será considerado 1.</span><span class="sxs-lookup"><span data-stu-id="c186c-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c186c-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c186c-126">Example</span></span>

<span data-ttu-id="c186c-127">LEFT ("1º de janeiro de 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="c186c-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="c186c-128">Retorna o valor "Jan".</span><span class="sxs-lookup"><span data-stu-id="c186c-128">Returns the value "Jan".</span></span> 
  

