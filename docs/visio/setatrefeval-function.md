---
title: Função SETATREFEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Usado no parâmetro set_expression da função SETATREF para indicar que set_expression deve ser avaliado antes de atribuir ao parâmetro de referência em SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432979"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="4fd45-103">Função SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="4fd45-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="4fd45-104">Usado no parâmetro _set_expression_ da função SETATREF para  indicar que set_expression deve ser avaliado  antes de atribuir ao parâmetro de referência em SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4fd45-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4fd45-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fd45-105">Syntax</span></span>

<span data-ttu-id="4fd45-106">SETATREFEVAL(\*\* *expr* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4fd45-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4fd45-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fd45-107">Parameters</span></span>

|<span data-ttu-id="4fd45-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4fd45-108">**Name**</span></span>|<span data-ttu-id="4fd45-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="4fd45-109">**Required/Optional**</span></span>|<span data-ttu-id="4fd45-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4fd45-110">**Data Type**</span></span>|<span data-ttu-id="4fd45-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4fd45-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4fd45-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="4fd45-112">_expr_</span></span> <br/> |<span data-ttu-id="4fd45-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4fd45-113">Required</span></span>  <br/> |<span data-ttu-id="4fd45-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="4fd45-114">**Varies**</span></span> <br/> | <span data-ttu-id="4fd45-115">Uma expressão avaliada quando a função SETATREF redireciona set_expression  _para_ outra célula.</span><span class="sxs-lookup"><span data-stu-id="4fd45-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fd45-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fd45-116">Remarks</span></span>

<span data-ttu-id="4fd45-117">Ao atribuir o *set_expression* parâmetro da função SETATREF a uma célula referenciada, o Microsoft Visio grava set_expression na célula como uma expressão por padrão. </span><span class="sxs-lookup"><span data-stu-id="4fd45-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="4fd45-118">No entanto, se qualquer parte do parâmetro set_expression for envolvida pela função SETATREFEVAL, o Visio avaliará a expressão e substituirá  *a*  função SETATREFEVAL pelo resultado antes de resolver a expressão SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4fd45-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4fd45-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4fd45-119">Example</span></span>

<span data-ttu-id="4fd45-120">Para ver um exemplo, consulte a função [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="4fd45-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

