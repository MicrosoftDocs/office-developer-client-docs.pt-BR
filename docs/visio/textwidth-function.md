---
title: Função TEXTWIDTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Retorna a largura do texto redigido em uma forma.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422030"
---
# <a name="textwidth-function"></a><span data-ttu-id="3e3df-103">Função TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="3e3df-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="3e3df-104">Retorna a largura do texto redigido em uma forma.</span><span class="sxs-lookup"><span data-stu-id="3e3df-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3e3df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e3df-105">Syntax</span></span>

<span data-ttu-id="3e3df-106">TextWIDTH (\* \* *shapename! O texto* \* \* \* \* *[, MaximumWidth]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3e3df-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3e3df-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e3df-107">Parameters</span></span>

|<span data-ttu-id="3e3df-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3e3df-108">**Name**</span></span>|<span data-ttu-id="3e3df-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="3e3df-109">**Required/Optional**</span></span>|<span data-ttu-id="3e3df-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="3e3df-110">**Data Type**</span></span>|<span data-ttu-id="3e3df-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3e3df-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3e3df-112">_shapename! o texto_</span><span class="sxs-lookup"><span data-stu-id="3e3df-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="3e3df-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3e3df-113">Required</span></span>  <br/> |<span data-ttu-id="3e3df-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e3df-114">**String**</span></span> <br/> |<span data-ttu-id="3e3df-115">Uma referência à célula chamada TheText na forma de destino.</span><span class="sxs-lookup"><span data-stu-id="3e3df-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="3e3df-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="3e3df-116">_shapename!_</span></span> <span data-ttu-id="3e3df-117">é o nome da forma da qual você deseja recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="3e3df-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="3e3df-118">_MaximumWidth_</span><span class="sxs-lookup"><span data-stu-id="3e3df-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="3e3df-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="3e3df-119">Optional</span></span>  <br/> |<span data-ttu-id="3e3df-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="3e3df-120">**Numeric**</span></span> <br/> |<span data-ttu-id="3e3df-121">A largura máxima de um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="3e3df-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3e3df-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3e3df-122">Return value</span></span>

<span data-ttu-id="3e3df-123">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="3e3df-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e3df-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e3df-124">Remarks</span></span>

<span data-ttu-id="3e3df-125">Essa função é normalmente usada para ajustar a largura de uma forma para ajustar o texto nela contido.</span><span class="sxs-lookup"><span data-stu-id="3e3df-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="3e3df-126">Se for _Sheetn!_</span><span class="sxs-lookup"><span data-stu-id="3e3df-126">If  _sheetN!_</span></span> <span data-ttu-id="3e3df-127">for omitido, a forma padrão será a forma atual.</span><span class="sxs-lookup"><span data-stu-id="3e3df-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="3e3df-128">Se _MaximumWidth_ for especificado, o resultado será a linha mais longa de texto que se ajusta dentro de _MaximumWidth_.</span><span class="sxs-lookup"><span data-stu-id="3e3df-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="3e3df-129">Se _MaximumWidth_ for omitido, o resultado será a largura total do texto.</span><span class="sxs-lookup"><span data-stu-id="3e3df-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3e3df-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3e3df-130">Example</span></span>

<span data-ttu-id="3e3df-131">TextWIDTH (o texto)</span><span class="sxs-lookup"><span data-stu-id="3e3df-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="3e3df-132">Retorna o comprimento total do texto na forma atual.</span><span class="sxs-lookup"><span data-stu-id="3e3df-132">Returns the total length of the text in the current shape.</span></span> 
  

