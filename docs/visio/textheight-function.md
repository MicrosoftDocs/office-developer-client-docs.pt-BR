---
title: Função TEXTHEIGHT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Retorna a altura do texto redigido em uma forma em que nenhuma linha de texto excede a largura máxima.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773121"
---
# <a name="textheight-function"></a><span data-ttu-id="caddd-103">Função TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="caddd-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="caddd-104">Retorna a altura do texto redigido em uma forma em que nenhuma linha de texto excede a _largura máxima_.</span><span class="sxs-lookup"><span data-stu-id="caddd-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="caddd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caddd-105">Syntax</span></span>

<span data-ttu-id="caddd-106">TEXTHEIGHT (* * *shapename! TheText* * * * * *[, largura máxima]* * *)</span><span class="sxs-lookup"><span data-stu-id="caddd-106">TEXTHEIGHT(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="caddd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caddd-107">Parameters</span></span>

|<span data-ttu-id="caddd-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="caddd-108">**Name**</span></span>|<span data-ttu-id="caddd-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="caddd-109">**Required/Optional**</span></span>|<span data-ttu-id="caddd-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="caddd-110">**Data Type**</span></span>|<span data-ttu-id="caddd-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="caddd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="caddd-112">_shapename! theText_</span><span class="sxs-lookup"><span data-stu-id="caddd-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="caddd-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="caddd-113">Required</span></span>  <br/> |<span data-ttu-id="caddd-114">**String**</span><span class="sxs-lookup"><span data-stu-id="caddd-114">**String**</span></span> <br/> |<span data-ttu-id="caddd-115">Uma referência à célula nomeada TheText na forma de destino.</span><span class="sxs-lookup"><span data-stu-id="caddd-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="caddd-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="caddd-116">_shapename!_</span></span> <span data-ttu-id="caddd-117">é o nome da forma do qual você deseja recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="caddd-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="caddd-118">_largura máxima_</span><span class="sxs-lookup"><span data-stu-id="caddd-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="caddd-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="caddd-119">Optional</span></span>  <br/> |<span data-ttu-id="caddd-120">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="caddd-120">**Numeric**</span></span> <br/> |<span data-ttu-id="caddd-121">A largura máxima de um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="caddd-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="caddd-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="caddd-122">Return value</span></span>

<span data-ttu-id="caddd-123">String</span><span class="sxs-lookup"><span data-stu-id="caddd-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="caddd-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="caddd-124">Remarks</span></span>

<span data-ttu-id="caddd-p102">O valor retornado inclui a altura do texto incluindo o espaço antes e após o texto, o espaçamento de linha no texto e as margens do bloco de texto superiores e inferiores. Essa função é normalmente usada para ajustar a altura de uma forma para ajustar o texto nela contido.</span><span class="sxs-lookup"><span data-stu-id="caddd-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="caddd-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="caddd-127">Example</span></span>

<span data-ttu-id="caddd-128">TEXTHEIGHT(TheText,(Largura - 0,5 pol))</span><span class="sxs-lookup"><span data-stu-id="caddd-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="caddd-129">Retorna a altura do texto quando contido na largura da forma menos 0,5 polegadas.</span><span class="sxs-lookup"><span data-stu-id="caddd-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

