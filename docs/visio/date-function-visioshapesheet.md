---
title: Função DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Retorna a data representada por dia, mês e ano formatada de acordo com o estilo de data curta em configurações regionais do sistema. Os valores para o ano, mês e dia refletem o calendário gregoriano.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771681"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="0a3bb-104">Função DATE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0a3bb-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0a3bb-105">Retorna a data representada por *ano, mês,* *dia* e formatada de acordo com o estilo de data curta em configurações regionais do sistema.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="0a3bb-106">Os valores para o *ano*, *mês* e *dia* refletem o calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0a3bb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a3bb-107">Syntax</span></span>

<span data-ttu-id="0a3bb-108">Data (* * *ano* * *, * * *mês* * *, * * *dia* * *)</span><span class="sxs-lookup"><span data-stu-id="0a3bb-108">DATE(** *year* **, ** *month* **, ** *day* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a3bb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a3bb-109">Parameters</span></span>

|<span data-ttu-id="0a3bb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-110">**Name**</span></span>|<span data-ttu-id="0a3bb-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-111">**Required/Optional**</span></span>|<span data-ttu-id="0a3bb-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-112">**Data Type**</span></span>|<span data-ttu-id="0a3bb-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a3bb-114">_year_</span><span class="sxs-lookup"><span data-stu-id="0a3bb-114">_year_</span></span> <br/> |<span data-ttu-id="0a3bb-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a3bb-115">Required</span></span>  <br/> |<span data-ttu-id="0a3bb-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-116">**Integer**</span></span> <br/> |<span data-ttu-id="0a3bb-117">O ano.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-117">The year.</span></span>  <br/> |
| <span data-ttu-id="0a3bb-118">_Mês_</span><span class="sxs-lookup"><span data-stu-id="0a3bb-118">_month_</span></span> <br/> |<span data-ttu-id="0a3bb-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a3bb-119">Required</span></span>  <br/> |<span data-ttu-id="0a3bb-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-120">**Integer**</span></span> <br/> |<span data-ttu-id="0a3bb-121">O mês.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-121">The month.</span></span>  <br/> |
| <span data-ttu-id="0a3bb-122">_day_</span><span class="sxs-lookup"><span data-stu-id="0a3bb-122">_day_</span></span> <br/> |<span data-ttu-id="0a3bb-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0a3bb-123">Required</span></span>  <br/> |<span data-ttu-id="0a3bb-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a3bb-124">**Integer**</span></span> <br/> |<span data-ttu-id="0a3bb-125">O dia.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="0a3bb-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a3bb-126">Example 1</span></span>

<span data-ttu-id="0a3bb-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="0a3bb-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="0a3bb-128">Retornará o valor que representa 07/06/1999.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0a3bb-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0a3bb-129">Example 2</span></span>

<span data-ttu-id="0a3bb-130">DATE(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="0a3bb-131">Retornará o valor que representa 11/06/99.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0a3bb-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0a3bb-132">Example 3</span></span>

<span data-ttu-id="0a3bb-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="0a3bb-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="0a3bb-134">Retornará o valor que representa terça-feira, 14 de outubro de 1999.</span><span class="sxs-lookup"><span data-stu-id="0a3bb-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

