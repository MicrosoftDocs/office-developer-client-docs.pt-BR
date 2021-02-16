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
description: Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é mudada.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424326"
---
# <a name="getref-function"></a><span data-ttu-id="6e06c-103">Função GETREF</span><span class="sxs-lookup"><span data-stu-id="6e06c-103">GETREF Function</span></span>

<span data-ttu-id="6e06c-104">Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é mudada.</span><span class="sxs-lookup"><span data-stu-id="6e06c-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6e06c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e06c-105">Syntax</span></span>

<span data-ttu-id="6e06c-106">GETREF(\*\* *cellname* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6e06c-106">GETREF(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6e06c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e06c-107">Parameters</span></span>

|<span data-ttu-id="6e06c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6e06c-108">**Name**</span></span>|<span data-ttu-id="6e06c-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="6e06c-109">**Required/Optional**</span></span>|<span data-ttu-id="6e06c-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6e06c-110">**Data Type**</span></span>|<span data-ttu-id="6e06c-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e06c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6e06c-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="6e06c-112">_cellname_</span></span> <br/> |<span data-ttu-id="6e06c-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6e06c-113">Required</span></span>  <br/> |<span data-ttu-id="6e06c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6e06c-114">**String**</span></span> <br/> |<span data-ttu-id="6e06c-115">O nome da célula a ser referenciada.</span><span class="sxs-lookup"><span data-stu-id="6e06c-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="6e06c-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6e06c-116">Example</span></span>

<span data-ttu-id="6e06c-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="6e06c-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="6e06c-118">Define a fórmula da célula PinX para 5,1.</span><span class="sxs-lookup"><span data-stu-id="6e06c-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

