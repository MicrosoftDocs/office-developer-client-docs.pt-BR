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
description: Aplica o padrão de linha, o padrão de preenchimento ou o nome de fim de linha chamado à forma quando colocado na célula LinePattern, FillPattern, BeginArrow ou endArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422821"
---
# <a name="use-function"></a><span data-ttu-id="54ed8-103">Função USE</span><span class="sxs-lookup"><span data-stu-id="54ed8-103">USE Function</span></span>

<span data-ttu-id="54ed8-104">Aplica o padrão de linha, o padrão de preenchimento ou o _nome_ de fim de linha chamado à forma quando colocado na célula LinePattern, FillPattern, BeginArrow ou endarrow.</span><span class="sxs-lookup"><span data-stu-id="54ed8-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="54ed8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54ed8-105">Syntax</span></span>

<span data-ttu-id="54ed8-106">USE ("\* \* *nome* \* \*")</span><span class="sxs-lookup"><span data-stu-id="54ed8-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="54ed8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54ed8-107">Parameters</span></span>

|<span data-ttu-id="54ed8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="54ed8-108">**Name**</span></span>|<span data-ttu-id="54ed8-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="54ed8-109">**Required/Optional**</span></span>|<span data-ttu-id="54ed8-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="54ed8-110">**Data Type**</span></span>|<span data-ttu-id="54ed8-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="54ed8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="54ed8-112">_name_</span><span class="sxs-lookup"><span data-stu-id="54ed8-112">_name_</span></span> <br/> |<span data-ttu-id="54ed8-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="54ed8-113">Required</span></span>  <br/> |<span data-ttu-id="54ed8-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="54ed8-114">**String**</span></span> <br/> |<span data-ttu-id="54ed8-115">Qualquer cadeia de caracteres que seja um nome de mestre válido.</span><span class="sxs-lookup"><span data-stu-id="54ed8-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="54ed8-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="54ed8-116">Return value</span></span>

<span data-ttu-id="54ed8-117">Número</span><span class="sxs-lookup"><span data-stu-id="54ed8-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54ed8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="54ed8-118">Remarks</span></span>

<span data-ttu-id="54ed8-119">Se um _nome_ mestre nomeado estiver presente no estêncil de documento do documento, o padrão será aplicado como um padrão de linha, padrão de preenchimento, seta de início ou seta de fim.</span><span class="sxs-lookup"><span data-stu-id="54ed8-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="54ed8-120">Essa função sempre retornará 254.</span><span class="sxs-lookup"><span data-stu-id="54ed8-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="54ed8-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="54ed8-121">Example</span></span>

<span data-ttu-id="54ed8-122">USE("Railroad Tracks")</span><span class="sxs-lookup"><span data-stu-id="54ed8-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="54ed8-123">Formata a forma aplicando o padrão de mestre nomeado Railroad Tracks à forma que contém a fórmula.</span><span class="sxs-lookup"><span data-stu-id="54ed8-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

