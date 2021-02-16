---
title: Função AND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Retorna VERDADEIRO (1) se todas as expressões lógicas fornecidas são TRUE. Se qualquer uma das expressões lógicas for FALSO ou 0, a função AND retornará FALSO (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422009"
---
# <a name="and-function"></a><span data-ttu-id="52229-104">Função E</span><span class="sxs-lookup"><span data-stu-id="52229-104">AND Function</span></span>

<span data-ttu-id="52229-105">Retorna VERDADEIRO (1) se todas as expressões lógicas fornecidas são VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="52229-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="52229-106">Se qualquer uma das expressões lógicas for FALSO ou 0, a função AND retornará FALSO (0).</span><span class="sxs-lookup"><span data-stu-id="52229-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="52229-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52229-107">Syntax</span></span>

<span data-ttu-id="52229-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="52229-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="52229-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52229-109">Parameters</span></span>

|<span data-ttu-id="52229-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="52229-110">**Name**</span></span>|<span data-ttu-id="52229-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="52229-111">**Required/Optional**</span></span>|<span data-ttu-id="52229-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="52229-112">**Data Type**</span></span>|<span data-ttu-id="52229-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52229-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="52229-114">_expressão lógica_</span><span class="sxs-lookup"><span data-stu-id="52229-114">_logical expression_</span></span> <br/> |<span data-ttu-id="52229-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="52229-115">Required</span></span>  <br/> |<span data-ttu-id="52229-116">**String**</span><span class="sxs-lookup"><span data-stu-id="52229-116">**String**</span></span> <br/> | <span data-ttu-id="52229-p103">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor. Qualquer expressão avaliada como um valor diferente de zero é considerada VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="52229-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="52229-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="52229-119">Example</span></span>

<span data-ttu-id="52229-120">AND(Height \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="52229-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="52229-121">Retorna VERDADEIRO se ambas as expressões forem VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="52229-121">Returns TRUE if both expressions are TRUE.</span></span> <span data-ttu-id="52229-122">Se uma das expressões for FALSO, será retornado FALSO.</span><span class="sxs-lookup"><span data-stu-id="52229-122">Returns FALSE if either expression is FALSE.</span></span>
  

