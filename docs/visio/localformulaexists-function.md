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
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772237"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="9abb3-103">Função LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="9abb3-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="9abb3-104">Indica se a célula referenciada contém uma fórmula local.</span><span class="sxs-lookup"><span data-stu-id="9abb3-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9abb3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9abb3-105">Syntax</span></span>

<span data-ttu-id="9abb3-106">LOCALFORMULAEXISTS (* * *cellref* * *)</span><span class="sxs-lookup"><span data-stu-id="9abb3-106">LOCALFORMULAEXISTS (** *cellref* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9abb3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9abb3-107">Parameters</span></span>

|<span data-ttu-id="9abb3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9abb3-108">**Name**</span></span>|<span data-ttu-id="9abb3-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="9abb3-109">**Required/Optional**</span></span>|<span data-ttu-id="9abb3-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9abb3-110">**Data Type**</span></span>|<span data-ttu-id="9abb3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9abb3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9abb3-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="9abb3-112">_cellref_</span></span> <br/> |<span data-ttu-id="9abb3-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9abb3-113">Required</span></span>  <br/> |<span data-ttu-id="9abb3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9abb3-114">**String**</span></span> <br/> | <span data-ttu-id="9abb3-115">A célula cuja presença de fórmula você deseja verificar.</span><span class="sxs-lookup"><span data-stu-id="9abb3-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9abb3-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9abb3-116">Return value</span></span>

<span data-ttu-id="9abb3-117">Booliano</span><span class="sxs-lookup"><span data-stu-id="9abb3-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9abb3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9abb3-118">Remarks</span></span>

<span data-ttu-id="9abb3-119">A função LOCALFORMULAEXISTS retornará 1 se a célula contiver uma fórmula local; se não houver fórmula ou se a fórmula for herdada, retornará 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="9abb3-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

