---
title: Função IFERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: Retorna o resultado avaliado de uma expressão principal, se ele não é avaliada como um erro. Caso contrário, retornará o resultado avaliado de uma expressão alternativa.
ms.openlocfilehash: 5915d0cb8219ced190c6b53043188c96d2b56b5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772062"
---
# <a name="iferror-function"></a><span data-ttu-id="eeb8c-104">Função IFERROR</span><span class="sxs-lookup"><span data-stu-id="eeb8c-104">IFERROR Function</span></span>

<span data-ttu-id="eeb8c-105">Retorna o resultado avaliado de uma expressão principal, se ele não é avaliada como um erro.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="eeb8c-106">Caso contrário, retornará o resultado avaliado de uma expressão alternativa.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="eeb8c-107">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="eeb8c-107">Version Information</span></span>

<span data-ttu-id="eeb8c-108">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="eeb8c-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eeb8c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eeb8c-109">Syntax</span></span>

<span data-ttu-id="eeb8c-110">SEERRO (* * *expressão principal* * *, * * *expressão alternativa* * *)</span><span class="sxs-lookup"><span data-stu-id="eeb8c-110">IFERROR(** *primary expression* **, ** *alternate expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eeb8c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eeb8c-111">Parameters</span></span>

|<span data-ttu-id="eeb8c-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="eeb8c-112">**Name**</span></span>|<span data-ttu-id="eeb8c-113">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="eeb8c-113">**Required/Optional**</span></span>|<span data-ttu-id="eeb8c-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="eeb8c-114">**Data Type**</span></span>|<span data-ttu-id="eeb8c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eeb8c-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eeb8c-116">_expressão principal_</span><span class="sxs-lookup"><span data-stu-id="eeb8c-116">_primary expression_</span></span> <br/> |<span data-ttu-id="eeb8c-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="eeb8c-117">Required</span></span>  <br/> |<span data-ttu-id="eeb8c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="eeb8c-118">**String**</span></span> <br/> |<span data-ttu-id="eeb8c-119">A primeira expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="eeb8c-120">_expressão alternativa_</span><span class="sxs-lookup"><span data-stu-id="eeb8c-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="eeb8c-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="eeb8c-121">Required</span></span>  <br/> |<span data-ttu-id="eeb8c-122">**String**</span><span class="sxs-lookup"><span data-stu-id="eeb8c-122">**String**</span></span> <br/> |<span data-ttu-id="eeb8c-123">A expressão alternativa a ser avaliada caso a expressão principal resulte em erro.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eeb8c-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eeb8c-124">Return value</span></span>

<span data-ttu-id="eeb8c-125">Varia</span><span class="sxs-lookup"><span data-stu-id="eeb8c-125">Varies</span></span>
  

