---
title: Função LOWER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Retorna uma cadeia de caracteres convertida em minúsculas.
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421239"
---
# <a name="lower-function"></a><span data-ttu-id="612f0-103">Função LOWER</span><span class="sxs-lookup"><span data-stu-id="612f0-103">LOWER Function</span></span>

<span data-ttu-id="612f0-104">Retorna uma cadeia de caracteres convertida em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="612f0-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="612f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="612f0-105">Syntax</span></span>

<span data-ttu-id="612f0-106">Expressão LOWER(\*\*  \*\* )</span><span class="sxs-lookup"><span data-stu-id="612f0-106">LOWER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="612f0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="612f0-107">Parameters</span></span>

|<span data-ttu-id="612f0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="612f0-108">**Name**</span></span>|<span data-ttu-id="612f0-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="612f0-109">**Required/Optional**</span></span>|<span data-ttu-id="612f0-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="612f0-110">**Data Type**</span></span>|<span data-ttu-id="612f0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="612f0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="612f0-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="612f0-112">_expression_</span></span> <br/> |<span data-ttu-id="612f0-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="612f0-113">Required</span></span>  <br/> |<span data-ttu-id="612f0-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="612f0-114">**Varies**</span></span> <br/> | <span data-ttu-id="612f0-115">Uma cadeia de caracteres, uma referência de célula ou uma expressão: o resultado é convertido em uma cadeia, que é depois convertida em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="612f0-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="612f0-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="612f0-116">Return value</span></span>

<span data-ttu-id="612f0-117">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="612f0-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="612f0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="612f0-118">Remarks</span></span>

<span data-ttu-id="612f0-119">A conversão de maiúsculas e minúsculas é específica a cada local, tendo por base as configurações de usuário atuais.</span><span class="sxs-lookup"><span data-stu-id="612f0-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="612f0-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="612f0-120">Example</span></span>

<span data-ttu-id="612f0-121">LOWER("MAiúsculas/minÚsculas")</span><span class="sxs-lookup"><span data-stu-id="612f0-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="612f0-122">Retornará "maiúsculas/minúsculas".</span><span class="sxs-lookup"><span data-stu-id="612f0-122">Returns "mixed case".</span></span> 
  

