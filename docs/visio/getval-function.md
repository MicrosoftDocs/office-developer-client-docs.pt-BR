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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327311"
---
# <a name="getval-function"></a><span data-ttu-id="52e42-103">Função GETVAL</span><span class="sxs-lookup"><span data-stu-id="52e42-103">GETVAL Function</span></span>

<span data-ttu-id="52e42-104">Obtém o valor de uma célula e não recalcula a fórmula quando o valor da célula é alterado.</span><span class="sxs-lookup"><span data-stu-id="52e42-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="52e42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52e42-105">Syntax</span></span>

<span data-ttu-id="52e42-106">GETVAL (\* \* *cellname* \* \*)</span><span class="sxs-lookup"><span data-stu-id="52e42-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="52e42-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52e42-107">Parameters</span></span>

|<span data-ttu-id="52e42-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="52e42-108">**Name**</span></span>|<span data-ttu-id="52e42-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="52e42-109">**Required/Optional**</span></span>|<span data-ttu-id="52e42-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="52e42-110">**Data Type**</span></span>|<span data-ttu-id="52e42-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52e42-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="52e42-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="52e42-112">_cellname_</span></span> <br/> |<span data-ttu-id="52e42-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="52e42-113">Required</span></span>  <br/> |<span data-ttu-id="52e42-114">**String**</span><span class="sxs-lookup"><span data-stu-id="52e42-114">**String**</span></span> <br/> |<span data-ttu-id="52e42-115">O nome da célula de onde obter o valor.</span><span class="sxs-lookup"><span data-stu-id="52e42-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="52e42-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="52e42-116">Example</span></span>

<span data-ttu-id="52e42-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="52e42-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="52e42-118">Retorna a soma do valor das células PinX, PinY e Width.</span><span class="sxs-lookup"><span data-stu-id="52e42-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

