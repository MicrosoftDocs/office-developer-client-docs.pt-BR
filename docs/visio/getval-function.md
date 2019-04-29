---
title: Função GETVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416885"
---
# <a name="getval-function"></a><span data-ttu-id="18a8f-103">Função GETVAL</span><span class="sxs-lookup"><span data-stu-id="18a8f-103">GETVAL Function</span></span>

<span data-ttu-id="18a8f-104">Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.</span><span class="sxs-lookup"><span data-stu-id="18a8f-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="18a8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18a8f-105">Syntax</span></span>

<span data-ttu-id="18a8f-106">GETVAL (\* \* *cellname* \* \*)</span><span class="sxs-lookup"><span data-stu-id="18a8f-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="18a8f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18a8f-107">Parameters</span></span>

|<span data-ttu-id="18a8f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="18a8f-108">**Name**</span></span>|<span data-ttu-id="18a8f-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="18a8f-109">**Required/Optional**</span></span>|<span data-ttu-id="18a8f-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="18a8f-110">**Data Type**</span></span>|<span data-ttu-id="18a8f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18a8f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="18a8f-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="18a8f-112">_cellname_</span></span> <br/> |<span data-ttu-id="18a8f-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="18a8f-113">Required</span></span>  <br/> |<span data-ttu-id="18a8f-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="18a8f-114">**String**</span></span> <br/> |<span data-ttu-id="18a8f-115">O nome da célula de onde obter o valor.</span><span class="sxs-lookup"><span data-stu-id="18a8f-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="18a8f-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="18a8f-116">Example</span></span>

<span data-ttu-id="18a8f-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="18a8f-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="18a8f-118">Retorna a soma do valor das células PinX, PinY e Width.</span><span class="sxs-lookup"><span data-stu-id="18a8f-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

