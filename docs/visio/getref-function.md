---
title: Função GETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é alterada.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771962"
---
# <a name="getref-function"></a><span data-ttu-id="c9577-103">Função GETREF</span><span class="sxs-lookup"><span data-stu-id="c9577-103">GETREF Function</span></span>

<span data-ttu-id="c9577-104">Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é alterada.</span><span class="sxs-lookup"><span data-stu-id="c9577-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c9577-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9577-105">Syntax</span></span>

<span data-ttu-id="c9577-106">GETREF (* * *nome da célula* * *)</span><span class="sxs-lookup"><span data-stu-id="c9577-106">GETREF(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c9577-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9577-107">Parameters</span></span>

|<span data-ttu-id="c9577-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c9577-108">**Name**</span></span>|<span data-ttu-id="c9577-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c9577-109">**Required/Optional**</span></span>|<span data-ttu-id="c9577-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c9577-110">**Data Type**</span></span>|<span data-ttu-id="c9577-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c9577-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c9577-112">_nome da célula_</span><span class="sxs-lookup"><span data-stu-id="c9577-112">_cellname_</span></span> <br/> |<span data-ttu-id="c9577-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c9577-113">Required</span></span>  <br/> |<span data-ttu-id="c9577-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c9577-114">**String**</span></span> <br/> |<span data-ttu-id="c9577-115">O nome da célula para fazer referência à.</span><span class="sxs-lookup"><span data-stu-id="c9577-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="c9577-116">Example</span><span class="sxs-lookup"><span data-stu-id="c9577-116">Example</span></span>

<span data-ttu-id="c9577-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="c9577-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="c9577-118">Define a fórmula da célula PinX para 5,1.</span><span class="sxs-lookup"><span data-stu-id="c9577-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

