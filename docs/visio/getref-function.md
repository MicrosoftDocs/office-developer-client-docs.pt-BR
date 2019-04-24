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
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356492"
---
# <a name="getref-function"></a><span data-ttu-id="ff536-103">Função GETREF</span><span class="sxs-lookup"><span data-stu-id="ff536-103">GETREF Function</span></span>

<span data-ttu-id="ff536-104">Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é alterada.</span><span class="sxs-lookup"><span data-stu-id="ff536-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ff536-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff536-105">Syntax</span></span>

<span data-ttu-id="ff536-106">GETREF (\* \* *cellname* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ff536-106">GETREF(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ff536-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff536-107">Parameters</span></span>

|<span data-ttu-id="ff536-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ff536-108">**Name**</span></span>|<span data-ttu-id="ff536-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ff536-109">**Required/Optional**</span></span>|<span data-ttu-id="ff536-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ff536-110">**Data Type**</span></span>|<span data-ttu-id="ff536-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff536-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ff536-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="ff536-112">_cellname_</span></span> <br/> |<span data-ttu-id="ff536-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ff536-113">Required</span></span>  <br/> |<span data-ttu-id="ff536-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ff536-114">**String**</span></span> <br/> |<span data-ttu-id="ff536-115">O nome da célula para obter uma referência.</span><span class="sxs-lookup"><span data-stu-id="ff536-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="ff536-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ff536-116">Example</span></span>

<span data-ttu-id="ff536-117">SETF (GETREF (PinX), 5.1)</span><span class="sxs-lookup"><span data-stu-id="ff536-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="ff536-118">Define a fórmula da célula PinX para 5,1.</span><span class="sxs-lookup"><span data-stu-id="ff536-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

