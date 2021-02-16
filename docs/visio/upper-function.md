---
title: Função UPPER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: Retorna uma cadeia de caracteres convertida em maiúsculas.
ms.openlocfilehash: b88958526bfb5e08839077217759f7ffb50151b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415142"
---
# <a name="upper-function"></a><span data-ttu-id="b4b31-103">Função UPPER</span><span class="sxs-lookup"><span data-stu-id="b4b31-103">UPPER Function</span></span>

<span data-ttu-id="b4b31-104">Retorna uma cadeia de caracteres convertida em maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="b4b31-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b4b31-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4b31-105">Syntax</span></span>

<span data-ttu-id="b4b31-106">Expressão UPPER(\*\* \*\*\*\* )</span><span class="sxs-lookup"><span data-stu-id="b4b31-106">UPPER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b4b31-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4b31-107">Parameters</span></span>

|<span data-ttu-id="b4b31-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b4b31-108">**Name**</span></span>|<span data-ttu-id="b4b31-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="b4b31-109">**Required/Optional**</span></span>|<span data-ttu-id="b4b31-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="b4b31-110">**Data Type**</span></span>|<span data-ttu-id="b4b31-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b4b31-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b4b31-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b4b31-112">_expression_</span></span> <br/> |<span data-ttu-id="b4b31-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b4b31-113">Required</span></span>  <br/> |<span data-ttu-id="b4b31-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="b4b31-114">**Varies**</span></span> <br/> | <span data-ttu-id="b4b31-115">Uma cadeia de caracteres, uma referência de célula ou uma expressão: o resultado é convertido em uma cadeia, que é depois convertida em maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="b4b31-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4b31-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4b31-116">Remarks</span></span>

<span data-ttu-id="b4b31-117">A conversão de maiúsculas e minúsculas é específica a cada local, tendo por base as configurações de usuário atuais.</span><span class="sxs-lookup"><span data-stu-id="b4b31-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b4b31-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b4b31-118">Example</span></span>

<span data-ttu-id="b4b31-119">UPPER("MAiúsculas/minÚsculas")</span><span class="sxs-lookup"><span data-stu-id="b4b31-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="b4b31-120">Retornará "MAIÚSCULAS/MINÚSCULAS".</span><span class="sxs-lookup"><span data-stu-id="b4b31-120">Returns "MIXED CASE".</span></span> 
  

