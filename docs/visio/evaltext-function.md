---
title: Função EVALTEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Avalia o texto no shapename como se fosse uma fórmula e retorna o resultado.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771819"
---
# <a name="evaltext-function"></a><span data-ttu-id="7a6a5-103">Função EVALTEXT</span><span class="sxs-lookup"><span data-stu-id="7a6a5-103">EVALTEXT Function</span></span>

<span data-ttu-id="7a6a5-104">Avalia o texto no _shapename_ como se fosse uma fórmula e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="7a6a5-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7a6a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a6a5-105">Syntax</span></span>

<span data-ttu-id="7a6a5-106">EVALTEXT (* * *shapename! theText* * *)</span><span class="sxs-lookup"><span data-stu-id="7a6a5-106">EVALTEXT(** *shapename!theText* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7a6a5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a6a5-107">Parameters</span></span>

|<span data-ttu-id="7a6a5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7a6a5-108">**Name**</span></span>|<span data-ttu-id="7a6a5-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="7a6a5-109">**Required/Optional**</span></span>|<span data-ttu-id="7a6a5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="7a6a5-110">**Data Type**</span></span>|<span data-ttu-id="7a6a5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7a6a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7a6a5-112">_shapename! theText_</span><span class="sxs-lookup"><span data-stu-id="7a6a5-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="7a6a5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7a6a5-113">Required</span></span>  <br/> |<span data-ttu-id="7a6a5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7a6a5-114">**String**</span></span> <br/> |<span data-ttu-id="7a6a5-115">Uma célula é disparada quando a composição do texto da forma associada é alterada.</span><span class="sxs-lookup"><span data-stu-id="7a6a5-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7a6a5-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7a6a5-116">Return value</span></span>

<span data-ttu-id="7a6a5-117">String</span><span class="sxs-lookup"><span data-stu-id="7a6a5-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a6a5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a6a5-118">Remarks</span></span>

 <span data-ttu-id="7a6a5-119">_shapename_ pode ser utilizada para fazer referência ao texto de uma forma que não seja a atual.</span><span class="sxs-lookup"><span data-stu-id="7a6a5-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="7a6a5-p101">Se não tiver texto, o resultado será zero. Se o texto não puder ser avaliado, a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7a6a5-p101">If there is no text, the result is zero. If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="7a6a5-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7a6a5-122">Example</span></span>

<span data-ttu-id="7a6a5-123">EVALTEXT(line.2!theText)</span><span class="sxs-lookup"><span data-stu-id="7a6a5-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="7a6a5-p102">Avalia o texto contido na forma Line.2. Por exemplo, se Line.2 contiver "4 pés + 0,5 pé", será retornado o valor 4,5 pés.</span><span class="sxs-lookup"><span data-stu-id="7a6a5-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

