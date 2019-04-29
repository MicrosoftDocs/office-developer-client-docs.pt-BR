---
title: Função NOW (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Retorna o valor atual de data e hora.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414078"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="574b2-103">Função NOW (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="574b2-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="574b2-104">Retorna o valor atual de data e hora.</span><span class="sxs-lookup"><span data-stu-id="574b2-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="574b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="574b2-105">Syntax</span></span>

<span data-ttu-id="574b2-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="574b2-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="574b2-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="574b2-107">Return value</span></span>

<span data-ttu-id="574b2-108">DateTime</span><span class="sxs-lookup"><span data-stu-id="574b2-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="574b2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="574b2-109">Remarks</span></span>

<span data-ttu-id="574b2-110">NOW é recalculado automaticamente a cada minuto.</span><span class="sxs-lookup"><span data-stu-id="574b2-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="574b2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="574b2-111">Example 1</span></span>

<span data-ttu-id="574b2-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="574b2-112">NOW( )</span></span>
  
<span data-ttu-id="574b2-113">Retornará a data e hora atuais, como 27/09/10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="574b2-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="574b2-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="574b2-114">Example 2</span></span>

<span data-ttu-id="574b2-115">FORMAT(NOW(),"dd MMM., aaaa hh:mm")</span><span class="sxs-lookup"><span data-stu-id="574b2-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="574b2-116">Retornará a data e a hora atuais formatadas como 27 de setembro de 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="574b2-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="574b2-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="574b2-117">Example 3</span></span>

<span data-ttu-id="574b2-118">NOW () + 2EW.</span><span class="sxs-lookup"><span data-stu-id="574b2-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="574b2-119">Retornará a data e a hora atuais, além de duas semanas decorridas, como 11/10/10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="574b2-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

