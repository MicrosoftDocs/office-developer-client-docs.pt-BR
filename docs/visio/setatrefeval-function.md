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
description: Usado no parâmetro set_expression da função SETATREF para indicar que set_expression deve ser avaliada antes de atribuir ao parâmetro de referência em SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772858"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="f9367-103">Função SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="f9367-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="f9367-104">Usado no parâmetro _set_expression_ da função SETATREF para indicar _set_expression_ deve ser avaliada antes de atribuir ao parâmetro de _referência_ em SETATREF.</span><span class="sxs-lookup"><span data-stu-id="f9367-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f9367-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9367-105">Syntax</span></span>

<span data-ttu-id="f9367-106">SETATREFEVAL (* * *expr* * *)</span><span class="sxs-lookup"><span data-stu-id="f9367-106">SETATREFEVAL(** *expr* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f9367-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9367-107">Parameters</span></span>

|<span data-ttu-id="f9367-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f9367-108">**Name**</span></span>|<span data-ttu-id="f9367-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f9367-109">**Required/Optional**</span></span>|<span data-ttu-id="f9367-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f9367-110">**Data Type**</span></span>|<span data-ttu-id="f9367-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f9367-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f9367-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="f9367-112">_expr_</span></span> <br/> |<span data-ttu-id="f9367-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f9367-113">Required</span></span>  <br/> |<span data-ttu-id="f9367-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="f9367-114">**Varies**</span></span> <br/> | <span data-ttu-id="f9367-115">Uma expressão que é avaliada quando a função SETATREF redireciona _set_expression_ para outra célula.</span><span class="sxs-lookup"><span data-stu-id="f9367-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9367-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9367-116">Remarks</span></span>

<span data-ttu-id="f9367-117">Ao atribuir o parâmetro *set_expression* da função SETATREF a uma célula referenciada, o Microsoft Visio grava *set_expression* para a célula como uma expressão por padrão.</span><span class="sxs-lookup"><span data-stu-id="f9367-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="f9367-118">No entanto, se qualquer parte do parâmetro *set_expression* é empacotado pela função SETATREFEVAL, o Visio avalia a expressão e substitui a função SETATREFEVAL pelo seu resultado antes de resolver a expressão SETATREF.</span><span class="sxs-lookup"><span data-stu-id="f9367-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f9367-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f9367-119">Example</span></span>

<span data-ttu-id="f9367-120">Para ver um exemplo, consulte a função [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="f9367-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

