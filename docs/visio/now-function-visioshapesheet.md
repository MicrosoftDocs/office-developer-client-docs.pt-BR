---
title: Agora a função (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Retorna o valor de data e hora atual.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772446"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="1bbbd-103">Agora a função (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="1bbbd-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="1bbbd-104">Retorna o valor de data e hora atual.</span><span class="sxs-lookup"><span data-stu-id="1bbbd-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1bbbd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bbbd-105">Syntax</span></span>

<span data-ttu-id="1bbbd-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="1bbbd-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="1bbbd-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1bbbd-107">Return value</span></span>

<span data-ttu-id="1bbbd-108">Datetime</span><span class="sxs-lookup"><span data-stu-id="1bbbd-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1bbbd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bbbd-109">Remarks</span></span>

<span data-ttu-id="1bbbd-110">NOW é recalculado automaticamente a cada minuto.</span><span class="sxs-lookup"><span data-stu-id="1bbbd-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="1bbbd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bbbd-111">Example 1</span></span>

<span data-ttu-id="1bbbd-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="1bbbd-112">NOW( )</span></span>
  
<span data-ttu-id="1bbbd-113">Retornará a data e hora atuais, como 27/09/10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="1bbbd-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1bbbd-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1bbbd-114">Example 2</span></span>

<span data-ttu-id="1bbbd-115">FORMAT(NOW(),"dd MMM., aaaa hh:mm")</span><span class="sxs-lookup"><span data-stu-id="1bbbd-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="1bbbd-116">Retornará a data e a hora atuais formatadas como 27 de setembro de 2010 12:03.</span><span class="sxs-lookup"><span data-stu-id="1bbbd-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="1bbbd-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1bbbd-117">Example 3</span></span>

<span data-ttu-id="1bbbd-118">NOW()+2EW.</span><span class="sxs-lookup"><span data-stu-id="1bbbd-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="1bbbd-119">Retornará a data e a hora atuais, além de duas semanas decorridas, como 11/10/10 12:03:30.</span><span class="sxs-lookup"><span data-stu-id="1bbbd-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

