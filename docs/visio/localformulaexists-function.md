---
title: Função LOCALFORMULAEXISTS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indica se a célula referenciada contém uma fórmula local.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433287"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="00edc-103">Função LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="00edc-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="00edc-104">Indica se a célula referenciada contém uma fórmula local.</span><span class="sxs-lookup"><span data-stu-id="00edc-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00edc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00edc-105">Syntax</span></span>

<span data-ttu-id="00edc-106">LOCALFORMULAEXISTS (\* \* *cellref* \* \*)</span><span class="sxs-lookup"><span data-stu-id="00edc-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00edc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00edc-107">Parameters</span></span>

|<span data-ttu-id="00edc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="00edc-108">**Name**</span></span>|<span data-ttu-id="00edc-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="00edc-109">**Required/Optional**</span></span>|<span data-ttu-id="00edc-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="00edc-110">**Data Type**</span></span>|<span data-ttu-id="00edc-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="00edc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00edc-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="00edc-112">_cellref_</span></span> <br/> |<span data-ttu-id="00edc-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="00edc-113">Required</span></span>  <br/> |<span data-ttu-id="00edc-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="00edc-114">**String**</span></span> <br/> | <span data-ttu-id="00edc-115">A célula cuja presença de fórmula você deseja verificar.</span><span class="sxs-lookup"><span data-stu-id="00edc-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00edc-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="00edc-116">Return value</span></span>

<span data-ttu-id="00edc-117">Booliano</span><span class="sxs-lookup"><span data-stu-id="00edc-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00edc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="00edc-118">Remarks</span></span>

<span data-ttu-id="00edc-119">A função LOCALFORMULAEXISTS retornará 1 se a célula contiver uma fórmula local; se não houver fórmula ou se a fórmula for herdada, retornará 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="00edc-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

