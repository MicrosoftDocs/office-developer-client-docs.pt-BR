---
title: Função USE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Aplica o padrão de linha, o padrão de preenchimento ou o fim de linha denominado nome à forma quando colocada na célula LinePattern, FillPattern, BeginArrow ou EndArrow.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773224"
---
# <a name="use-function"></a><span data-ttu-id="179a5-103">Função USE</span><span class="sxs-lookup"><span data-stu-id="179a5-103">USE Function</span></span>

<span data-ttu-id="179a5-104">Aplica o padrão de linha, o padrão de preenchimento ou o fim de linha denominado _nome_ à forma quando colocada na célula LinePattern, FillPattern, BeginArrow ou EndArrow.</span><span class="sxs-lookup"><span data-stu-id="179a5-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="179a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="179a5-105">Syntax</span></span>

<span data-ttu-id="179a5-106">USO ("* * *nome* * *")</span><span class="sxs-lookup"><span data-stu-id="179a5-106">USE(" ** *name* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="179a5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="179a5-107">Parameters</span></span>

|<span data-ttu-id="179a5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="179a5-108">**Name**</span></span>|<span data-ttu-id="179a5-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="179a5-109">**Required/Optional**</span></span>|<span data-ttu-id="179a5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="179a5-110">**Data Type**</span></span>|<span data-ttu-id="179a5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="179a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="179a5-112">_name_</span><span class="sxs-lookup"><span data-stu-id="179a5-112">_name_</span></span> <br/> |<span data-ttu-id="179a5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="179a5-113">Required</span></span>  <br/> |<span data-ttu-id="179a5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="179a5-114">**String**</span></span> <br/> |<span data-ttu-id="179a5-115">Qualquer cadeia de caracteres que seja um nome de mestre válido.</span><span class="sxs-lookup"><span data-stu-id="179a5-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="179a5-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="179a5-116">Return value</span></span>

<span data-ttu-id="179a5-117">Número</span><span class="sxs-lookup"><span data-stu-id="179a5-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="179a5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="179a5-118">Remarks</span></span>

<span data-ttu-id="179a5-119">Se um mestre chamado _name_ estiver presente no estêncil do documento do documento, o padrão será aplicado como um padrão de linha, o padrão de preenchimento, uma seta inicial ou seta final.</span><span class="sxs-lookup"><span data-stu-id="179a5-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="179a5-120">Essa função sempre retornará 254.</span><span class="sxs-lookup"><span data-stu-id="179a5-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="179a5-121">Example</span><span class="sxs-lookup"><span data-stu-id="179a5-121">Example</span></span>

<span data-ttu-id="179a5-122">USE("Railroad Tracks")</span><span class="sxs-lookup"><span data-stu-id="179a5-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="179a5-123">Formata a forma aplicando o padrão de mestre nomeado Railroad Tracks à forma que contém a fórmula.</span><span class="sxs-lookup"><span data-stu-id="179a5-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

