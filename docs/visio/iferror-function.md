---
title: Função IFERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 232fa528-2375-90be-8e18-7a064ce1345e
description: Retorna o resultado avaliado de uma expressão primária, se ela não for avaliada como um erro. Caso contrário, retornará o valor avaliado de uma expressão alternativa.
ms.openlocfilehash: 7b9b42b5c7e7053bae862ddadf17e65015d8ecc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431173"
---
# <a name="iferror-function"></a><span data-ttu-id="2bb32-104">Função IFERROR</span><span class="sxs-lookup"><span data-stu-id="2bb32-104">IFERROR Function</span></span>

<span data-ttu-id="2bb32-105">Retorna o resultado avaliado de uma expressão primária, se ela não for avaliada como um erro.</span><span class="sxs-lookup"><span data-stu-id="2bb32-105">Returns the evaluated result of a primary expression, if it does not evaluate to an error.</span></span> <span data-ttu-id="2bb32-106">Caso contrário, retornará o valor avaliado de uma expressão alternativa.</span><span class="sxs-lookup"><span data-stu-id="2bb32-106">Otherwise, returns the evaluated result of an alternate expression.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="2bb32-107">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="2bb32-107">Version Information</span></span>

<span data-ttu-id="2bb32-108">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="2bb32-108">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2bb32-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bb32-109">Syntax</span></span>

<span data-ttu-id="2bb32-110">SEERRO (\* \* *expressão primária* \* \*, \* \* *expressão alternativa* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2bb32-110">IFERROR(\*\* *primary expression* \*\*, \*\* *alternate expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2bb32-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bb32-111">Parameters</span></span>

|<span data-ttu-id="2bb32-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="2bb32-112">**Name**</span></span>|<span data-ttu-id="2bb32-113">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="2bb32-113">**Required/Optional**</span></span>|<span data-ttu-id="2bb32-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="2bb32-114">**Data Type**</span></span>|<span data-ttu-id="2bb32-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2bb32-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2bb32-116">_expressão principal_</span><span class="sxs-lookup"><span data-stu-id="2bb32-116">_primary expression_</span></span> <br/> |<span data-ttu-id="2bb32-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2bb32-117">Required</span></span>  <br/> |<span data-ttu-id="2bb32-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bb32-118">**String**</span></span> <br/> |<span data-ttu-id="2bb32-119">A primeira expressão a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="2bb32-119">The first expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2bb32-120">_expressão alternativa_</span><span class="sxs-lookup"><span data-stu-id="2bb32-120">_alternate expression_</span></span> <br/> |<span data-ttu-id="2bb32-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2bb32-121">Required</span></span>  <br/> |<span data-ttu-id="2bb32-122">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bb32-122">**String**</span></span> <br/> |<span data-ttu-id="2bb32-123">A expressão alternativa a ser avaliada caso a expressão principal resulte em erro.</span><span class="sxs-lookup"><span data-stu-id="2bb32-123">The alternate expression to evaluate if the primary expression evaluates to an error.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2bb32-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2bb32-124">Return value</span></span>

<span data-ttu-id="2bb32-125">Várias</span><span class="sxs-lookup"><span data-stu-id="2bb32-125">Varies</span></span>
  

