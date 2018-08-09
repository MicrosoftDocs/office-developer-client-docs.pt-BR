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
description: Retorna o caractere mais à esquerda ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772178"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="b60b3-103">Função LEFT (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b60b3-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b60b3-104">Retorna o caractere mais à esquerda ou caracteres em uma cadeia de caracteres de texto, com base no número de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="b60b3-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b60b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b60b3-105">Syntax</span></span>

<span data-ttu-id="b60b3-106">ESQUERDA (* * *texto* * *, [, * * *num_chars_opt* * *])</span><span class="sxs-lookup"><span data-stu-id="b60b3-106">LEFT(** *text* **, [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b60b3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b60b3-107">Parameters</span></span>

|<span data-ttu-id="b60b3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b60b3-108">**Name**</span></span>|<span data-ttu-id="b60b3-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="b60b3-109">**Required/Optional**</span></span>|<span data-ttu-id="b60b3-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="b60b3-110">**Data Type**</span></span>|<span data-ttu-id="b60b3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b60b3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b60b3-112">_text_</span><span class="sxs-lookup"><span data-stu-id="b60b3-112">_text_</span></span> <br/> |<span data-ttu-id="b60b3-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b60b3-113">Required</span></span>  <br/> |<span data-ttu-id="b60b3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b60b3-114">**String**</span></span> <br/> |<span data-ttu-id="b60b3-115">A cadeia de caracteres de texto que contém os caracteres a serem extraídos.</span><span class="sxs-lookup"><span data-stu-id="b60b3-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="b60b3-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="b60b3-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="b60b3-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="b60b3-117">Optional</span></span>  <br/> |<span data-ttu-id="b60b3-118">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="b60b3-118">**Numeric**</span></span> <br/> |<span data-ttu-id="b60b3-119">O número de caracteres a extrair.</span><span class="sxs-lookup"><span data-stu-id="b60b3-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b60b3-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b60b3-120">Return value</span></span>

<span data-ttu-id="b60b3-121">String</span><span class="sxs-lookup"><span data-stu-id="b60b3-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b60b3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b60b3-122">Remarks</span></span>

<span data-ttu-id="b60b3-123">O valor de _num_chars_opt_ deve ser maior ou igual a zero (0).</span><span class="sxs-lookup"><span data-stu-id="b60b3-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="b60b3-124">Se _num_chars_opt_ for maior que o comprimento do texto, esquerda retornará todo o texto.</span><span class="sxs-lookup"><span data-stu-id="b60b3-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="b60b3-125">Se _num_chars_opt_ for omitido, presume-se a 1.</span><span class="sxs-lookup"><span data-stu-id="b60b3-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b60b3-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b60b3-126">Example</span></span>

<span data-ttu-id="b60b3-127">LEFT ("1º de janeiro de 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="b60b3-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="b60b3-128">Retorna o valor "Jan".</span><span class="sxs-lookup"><span data-stu-id="b60b3-128">Returns the value "Jan".</span></span> 
  

