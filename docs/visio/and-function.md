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
description: Retorna verdadeiro (1) se todas as expressões lógicas fornecidas forem TRUE. Se qualquer uma das expressões lógicas for FALSE ou 0, a função AND retorna FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771278"
---
# <a name="and-function"></a><span data-ttu-id="a2bae-104">Função E</span><span class="sxs-lookup"><span data-stu-id="a2bae-104">AND Function</span></span>

<span data-ttu-id="a2bae-105">Retorna verdadeiro (1) se todas as expressões lógicas fornecidas forem TRUE.</span><span class="sxs-lookup"><span data-stu-id="a2bae-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="a2bae-106">Se qualquer uma das expressões lógicas for FALSE ou 0, a função AND retorna FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="a2bae-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a2bae-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2bae-107">Syntax</span></span>

<span data-ttu-id="a2bae-108">E (* * *expression1 lógica* * *, * * *expression2 lógica* * *,..., * * *lógicaN* * *)</span><span class="sxs-lookup"><span data-stu-id="a2bae-108">AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a2bae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2bae-109">Parameters</span></span>

|<span data-ttu-id="a2bae-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a2bae-110">**Name**</span></span>|<span data-ttu-id="a2bae-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a2bae-111">**Required/Optional**</span></span>|<span data-ttu-id="a2bae-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a2bae-112">**Data Type**</span></span>|<span data-ttu-id="a2bae-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2bae-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a2bae-114">_expressão lógica_</span><span class="sxs-lookup"><span data-stu-id="a2bae-114">_logical expression_</span></span> <br/> |<span data-ttu-id="a2bae-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a2bae-115">Required</span></span>  <br/> |<span data-ttu-id="a2bae-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a2bae-116">**String**</span></span> <br/> | <span data-ttu-id="a2bae-p103">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor. Qualquer expressão avaliada como um valor diferente de zero é considerada VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="a2bae-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="a2bae-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a2bae-119">Example</span></span>

<span data-ttu-id="a2bae-120">E (altura \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="a2bae-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="a2bae-p104">Retorna VERDADEIRO se ambas as expressões forem VERDADEIRO. Se uma das expressões for FALSO, será retornado FALSO.</span><span class="sxs-lookup"><span data-stu-id="a2bae-p104">Returns TRUE if both expressions are TRUE. Returns FALSE if either expression is FALSE.</span></span>
  

