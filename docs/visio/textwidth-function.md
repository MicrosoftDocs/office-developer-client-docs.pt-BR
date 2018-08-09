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
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773119"
---
# <a name="textwidth-function"></a><span data-ttu-id="76058-103">Função TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="76058-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="76058-104">Retorna a largura do texto redigido em uma forma.</span><span class="sxs-lookup"><span data-stu-id="76058-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76058-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76058-105">Syntax</span></span>

<span data-ttu-id="76058-106">TEXTWIDTH (* * *shapename! TheText* * * * * *[, largura máxima]* * *)</span><span class="sxs-lookup"><span data-stu-id="76058-106">TEXTWIDTH(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76058-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76058-107">Parameters</span></span>

|<span data-ttu-id="76058-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="76058-108">**Name**</span></span>|<span data-ttu-id="76058-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="76058-109">**Required/Optional**</span></span>|<span data-ttu-id="76058-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="76058-110">**Data Type**</span></span>|<span data-ttu-id="76058-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="76058-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76058-112">_shapename! theText_</span><span class="sxs-lookup"><span data-stu-id="76058-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="76058-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="76058-113">Required</span></span>  <br/> |<span data-ttu-id="76058-114">**String**</span><span class="sxs-lookup"><span data-stu-id="76058-114">**String**</span></span> <br/> |<span data-ttu-id="76058-115">Uma referência à célula nomeada TheText na forma de destino.</span><span class="sxs-lookup"><span data-stu-id="76058-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="76058-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="76058-116">_shapename!_</span></span> <span data-ttu-id="76058-117">é o nome da forma do qual você deseja recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="76058-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="76058-118">_largura máxima_</span><span class="sxs-lookup"><span data-stu-id="76058-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="76058-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="76058-119">Optional</span></span>  <br/> |<span data-ttu-id="76058-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="76058-120">**Numeric**</span></span> <br/> |<span data-ttu-id="76058-121">A largura máxima de um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="76058-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="76058-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="76058-122">Return value</span></span>

<span data-ttu-id="76058-123">String</span><span class="sxs-lookup"><span data-stu-id="76058-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76058-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="76058-124">Remarks</span></span>

<span data-ttu-id="76058-125">Essa função é normalmente usada para ajustar a largura de uma forma para ajustar o texto nela contido.</span><span class="sxs-lookup"><span data-stu-id="76058-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="76058-126">Se _sheetN!_</span><span class="sxs-lookup"><span data-stu-id="76058-126">If  _sheetN!_</span></span> <span data-ttu-id="76058-127">for omitido, a forma padrão será a forma atual.</span><span class="sxs-lookup"><span data-stu-id="76058-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="76058-128">Se a _largura máxima_ for especificado, o resultado é a linha mais longa do texto que caiba na _largura máxima_.</span><span class="sxs-lookup"><span data-stu-id="76058-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="76058-129">Se a _largura máxima_ for omitido, o resultado é a largura total do texto.</span><span class="sxs-lookup"><span data-stu-id="76058-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="76058-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76058-130">Example</span></span>

<span data-ttu-id="76058-131">TextWidth(TheText)</span><span class="sxs-lookup"><span data-stu-id="76058-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="76058-132">Retorna o comprimento total do texto na forma atual.</span><span class="sxs-lookup"><span data-stu-id="76058-132">Returns the total length of the text in the current shape.</span></span> 
  

