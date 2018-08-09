---
title: Função CHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Retorna o caractere ANSI para um número.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771479"
---
# <a name="char-function"></a><span data-ttu-id="8063b-103">Função CHAR</span><span class="sxs-lookup"><span data-stu-id="8063b-103">CHAR Function</span></span>

<span data-ttu-id="8063b-104">Retorna o caractere ANSI para um número.</span><span class="sxs-lookup"><span data-stu-id="8063b-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8063b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8063b-105">Syntax</span></span>

<span data-ttu-id="8063b-106">CHAR (* * *número* * *)</span><span class="sxs-lookup"><span data-stu-id="8063b-106">CHAR(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8063b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8063b-107">Parameters</span></span>

|<span data-ttu-id="8063b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8063b-108">**Name**</span></span>|<span data-ttu-id="8063b-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8063b-109">**Required/Optional**</span></span>|<span data-ttu-id="8063b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8063b-110">**Data Type**</span></span>|<span data-ttu-id="8063b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8063b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8063b-112">_number_</span><span class="sxs-lookup"><span data-stu-id="8063b-112">_number_</span></span> <br/> |<span data-ttu-id="8063b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8063b-113">Required</span></span>  <br/> |<span data-ttu-id="8063b-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="8063b-114">**Number**</span></span> <br/> |<span data-ttu-id="8063b-115">O número de caractere ANSI você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="8063b-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8063b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8063b-116">Remarks</span></span>

<span data-ttu-id="8063b-117">A cadeia de caracteres resultante é um caractere de comprimento.</span><span class="sxs-lookup"><span data-stu-id="8063b-117">The resulting string is one character in length.</span></span> <span data-ttu-id="8063b-118">O parâmetro _número_ deve ser um inteiro entre 1 e 255 (inclusive) ou a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="8063b-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8063b-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8063b-119">Example</span></span>

<span data-ttu-id="8063b-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="8063b-120">CHAR(9)</span></span> 
  
<span data-ttu-id="8063b-121">Retornará o caractere de tabulação.</span><span class="sxs-lookup"><span data-stu-id="8063b-121">Returns the tab character.</span></span> 
  

