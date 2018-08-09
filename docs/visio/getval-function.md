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
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771964"
---
# <a name="getval-function"></a><span data-ttu-id="a39f5-103">Função GETVAL</span><span class="sxs-lookup"><span data-stu-id="a39f5-103">GETVAL Function</span></span>

<span data-ttu-id="a39f5-104">Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.</span><span class="sxs-lookup"><span data-stu-id="a39f5-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a39f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a39f5-105">Syntax</span></span>

<span data-ttu-id="a39f5-106">GETVAL (* * *nome da célula* * *)</span><span class="sxs-lookup"><span data-stu-id="a39f5-106">GETVAL(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a39f5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a39f5-107">Parameters</span></span>

|<span data-ttu-id="a39f5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a39f5-108">**Name**</span></span>|<span data-ttu-id="a39f5-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a39f5-109">**Required/Optional**</span></span>|<span data-ttu-id="a39f5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a39f5-110">**Data Type**</span></span>|<span data-ttu-id="a39f5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a39f5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a39f5-112">_nome da célula_</span><span class="sxs-lookup"><span data-stu-id="a39f5-112">_cellname_</span></span> <br/> |<span data-ttu-id="a39f5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a39f5-113">Required</span></span>  <br/> |<span data-ttu-id="a39f5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a39f5-114">**String**</span></span> <br/> |<span data-ttu-id="a39f5-115">O nome da célula de onde obter o valor.</span><span class="sxs-lookup"><span data-stu-id="a39f5-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="a39f5-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a39f5-116">Example</span></span>

<span data-ttu-id="a39f5-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="a39f5-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="a39f5-118">Retorna a soma do valor das células PinX, PinY e Width.</span><span class="sxs-lookup"><span data-stu-id="a39f5-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

