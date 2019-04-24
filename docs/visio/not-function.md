---
title: Função NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Retorna TRUE (1) se logicaly for FALSE. Caso contrário, retornará FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341124"
---
# <a name="not-function"></a><span data-ttu-id="4a808-104">Função NOT</span><span class="sxs-lookup"><span data-stu-id="4a808-104">NOT Function</span></span>

<span data-ttu-id="4a808-105">Retorna TRUE (1) se _logicaly_ for false.</span><span class="sxs-lookup"><span data-stu-id="4a808-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="4a808-106">Caso contrário, retornará FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="4a808-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4a808-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a808-107">Syntax</span></span>

<span data-ttu-id="4a808-108">NOT (\* \* *logicalid* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4a808-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4a808-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a808-109">Parameters</span></span>

|<span data-ttu-id="4a808-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4a808-110">**Name**</span></span>|<span data-ttu-id="4a808-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="4a808-111">**Required/Optional**</span></span>|<span data-ttu-id="4a808-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4a808-112">**Data Type**</span></span>|<span data-ttu-id="4a808-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a808-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4a808-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="4a808-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="4a808-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4a808-115">Required</span></span>  <br/> |<span data-ttu-id="4a808-116">**String**</span><span class="sxs-lookup"><span data-stu-id="4a808-116">**String**</span></span> <br/> |<span data-ttu-id="4a808-117">A expressão lógica a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="4a808-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4a808-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4a808-118">Return value</span></span>

<span data-ttu-id="4a808-119">Booliano</span><span class="sxs-lookup"><span data-stu-id="4a808-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="4a808-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4a808-120">Example</span></span>

<span data-ttu-id="4a808-121">Não (altura \> de 0,75 in)</span><span class="sxs-lookup"><span data-stu-id="4a808-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="4a808-122">Retorna 1 se a Altura for menor que ou igual a 0,75 polegadas.</span><span class="sxs-lookup"><span data-stu-id="4a808-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="4a808-123">Retorna 0 se a Altura for maior que 0,75 polegadas.</span><span class="sxs-lookup"><span data-stu-id="4a808-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

