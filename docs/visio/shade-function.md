---
title: Função SHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica a cor reduzindo a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382978"
---
# <a name="shade-function"></a><span data-ttu-id="9b7ab-103">Função SHADE</span><span class="sxs-lookup"><span data-stu-id="9b7ab-103">SHADE Function</span></span>

<span data-ttu-id="9b7ab-104">Modifica a cor reduzindo a luminosidade pelo valor (positivo ou negativo) especificado no parâmetro _int_ .</span><span class="sxs-lookup"><span data-stu-id="9b7ab-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9b7ab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b7ab-105">Syntax</span></span>

<span data-ttu-id="9b7ab-106">SOMBREAMENTO (\* \* *cor* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9b7ab-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9b7ab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b7ab-107">Parameters</span></span>

|<span data-ttu-id="9b7ab-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-108">**Name**</span></span>|<span data-ttu-id="9b7ab-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-109">**Required/Optional**</span></span>|<span data-ttu-id="9b7ab-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-110">**Data Type**</span></span>|<span data-ttu-id="9b7ab-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9b7ab-112">_color_</span><span class="sxs-lookup"><span data-stu-id="9b7ab-112">_color_</span></span> <br/> |<span data-ttu-id="9b7ab-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9b7ab-113">Required</span></span>  <br/> |<span data-ttu-id="9b7ab-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9b7ab-115">O índice de cores do Microsoft Visio ou o valor RGB da cor.</span><span class="sxs-lookup"><span data-stu-id="9b7ab-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="9b7ab-116">_int_</span><span class="sxs-lookup"><span data-stu-id="9b7ab-116">_int_</span></span> <br/> |<span data-ttu-id="9b7ab-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9b7ab-117">Required</span></span>  <br/> |<span data-ttu-id="9b7ab-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-118">**Integer**</span></span> <br/> |<span data-ttu-id="9b7ab-p101">O valor pelo qual a luminosidade da cor será reduzida. Pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="9b7ab-p101">The amount by which to decrease the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9b7ab-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9b7ab-121">Return value</span></span>

 <span data-ttu-id="9b7ab-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="9b7ab-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b7ab-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b7ab-123">Remarks</span></span>

<span data-ttu-id="9b7ab-124">Os limites superiores e inferiores de luminosidade são 0 e 240, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9b7ab-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="9b7ab-125">Não há nenhum limite do tamanho do inteiro, que você pode passar para o parâmetro _int_ , mas luminosidade nunca excede esses limites.</span><span class="sxs-lookup"><span data-stu-id="9b7ab-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Limites superiores e inferiores de luminosidade](media/image199_ZA10173627.gif)
  

