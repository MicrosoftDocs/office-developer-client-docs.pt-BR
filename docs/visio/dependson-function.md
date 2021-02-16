---
title: Função DEPENDSON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Cria uma dependência de referência de célula.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423465"
---
# <a name="dependson-function"></a><span data-ttu-id="bac84-103">Função DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="bac84-103">DEPENDSON Function</span></span>

<span data-ttu-id="bac84-104">Cria uma dependência de referência de célula.</span><span class="sxs-lookup"><span data-stu-id="bac84-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bac84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bac84-105">Syntax</span></span>

<span data-ttu-id="bac84-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="bac84-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bac84-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bac84-107">Parameters</span></span>

|<span data-ttu-id="bac84-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="bac84-108">**Name**</span></span>|<span data-ttu-id="bac84-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="bac84-109">**Required/Optional**</span></span>|<span data-ttu-id="bac84-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="bac84-110">**Data Type**</span></span>|<span data-ttu-id="bac84-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bac84-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bac84-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="bac84-112">_cellref_</span></span> <br/> |<span data-ttu-id="bac84-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bac84-113">Required</span></span>  <br/> |<span data-ttu-id="bac84-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bac84-114">**String**</span></span> <br/> |<span data-ttu-id="bac84-115">A primeira referência de célula.</span><span class="sxs-lookup"><span data-stu-id="bac84-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="bac84-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="bac84-116">_cellref2_</span></span> <br/> |<span data-ttu-id="bac84-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="bac84-117">Optional</span></span>  <br/> |<span data-ttu-id="bac84-118">**String**</span><span class="sxs-lookup"><span data-stu-id="bac84-118">**String**</span></span> <br/> |<span data-ttu-id="bac84-119">A referência da segunda célula.</span><span class="sxs-lookup"><span data-stu-id="bac84-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bac84-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bac84-120">Remarks</span></span>

<span data-ttu-id="bac84-p101">Essa função sempre retornará FALSO. Ela não tem efeito quando utilizada em uma linha Event ou em uma célula Action.</span><span class="sxs-lookup"><span data-stu-id="bac84-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bac84-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bac84-123">Example</span></span>

<span data-ttu-id="bac84-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="bac84-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="bac84-125">Abre o bloco de texto para uma forma sempre que as células PinX ou PinY da forma forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="bac84-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

