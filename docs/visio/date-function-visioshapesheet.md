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
description: Retorna a data representada por ano, mês e dia formatados de acordo com o estilo de data abreviada das Configurações Regionais do sistema. Os valores de ano, mês e dia refletem o calendário gregoriano.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360330"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="41ed7-104">Função DATE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="41ed7-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="41ed7-105">Retorna a data representada por *ano, mês* e *dia* formatados de acordo com o estilo de data abreviada das Configurações Regionais do sistema.</span><span class="sxs-lookup"><span data-stu-id="41ed7-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="41ed7-106">Os valores de *ano*, *mês* e *dia*  refletem o calendário gregoriano.</span><span class="sxs-lookup"><span data-stu-id="41ed7-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="41ed7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41ed7-107">Syntax</span></span>

<span data-ttu-id="41ed7-108">DATE(\*\* *ano* \*\*, \*\* *mês* \*\*, \*\* *dia* \*\* )</span><span class="sxs-lookup"><span data-stu-id="41ed7-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="41ed7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41ed7-109">Parameters</span></span>

|<span data-ttu-id="41ed7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="41ed7-110">**Name**</span></span>|<span data-ttu-id="41ed7-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="41ed7-111">**Required/Optional**</span></span>|<span data-ttu-id="41ed7-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="41ed7-112">**Data Type**</span></span>|<span data-ttu-id="41ed7-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41ed7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="41ed7-114">_ano_</span><span class="sxs-lookup"><span data-stu-id="41ed7-114">_year_</span></span> <br/> |<span data-ttu-id="41ed7-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="41ed7-115">Required</span></span>  <br/> |<span data-ttu-id="41ed7-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="41ed7-116">**Integer**</span></span> <br/> |<span data-ttu-id="41ed7-117">O ano.</span><span class="sxs-lookup"><span data-stu-id="41ed7-117">The year.</span></span>  <br/> |
| <span data-ttu-id="41ed7-118">_mês_</span><span class="sxs-lookup"><span data-stu-id="41ed7-118">_month_</span></span> <br/> |<span data-ttu-id="41ed7-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="41ed7-119">Required</span></span>  <br/> |<span data-ttu-id="41ed7-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="41ed7-120">**Integer**</span></span> <br/> |<span data-ttu-id="41ed7-121">O mês.</span><span class="sxs-lookup"><span data-stu-id="41ed7-121">The month.</span></span>  <br/> |
| <span data-ttu-id="41ed7-122">_dia_</span><span class="sxs-lookup"><span data-stu-id="41ed7-122">_day_</span></span> <br/> |<span data-ttu-id="41ed7-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="41ed7-123">Required</span></span>  <br/> |<span data-ttu-id="41ed7-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="41ed7-124">**Integer**</span></span> <br/> |<span data-ttu-id="41ed7-125">O dia.</span><span class="sxs-lookup"><span data-stu-id="41ed7-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="41ed7-126">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41ed7-126">Example 1</span></span>

<span data-ttu-id="41ed7-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="41ed7-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="41ed7-128">Retornará o valor que representa 07/06/1999.</span><span class="sxs-lookup"><span data-stu-id="41ed7-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="41ed7-129">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="41ed7-129">Example 2</span></span>

<span data-ttu-id="41ed7-130">DATE(1999,6,7) + 4 ed.</span><span class="sxs-lookup"><span data-stu-id="41ed7-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="41ed7-131">Retornará o valor que representa 11/06/99.</span><span class="sxs-lookup"><span data-stu-id="41ed7-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="41ed7-132">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="41ed7-132">Example 3</span></span>

<span data-ttu-id="41ed7-133">FORMAT(DATE(1999,10,14),"C")</span><span class="sxs-lookup"><span data-stu-id="41ed7-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="41ed7-134">Retornará o valor que representa terça-feira, 14 de outubro de 1999.</span><span class="sxs-lookup"><span data-stu-id="41ed7-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

