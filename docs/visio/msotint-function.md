---
title: Função MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica a cor aumentando a luminosidade pelo percentual especificado.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335193"
---
# <a name="msotint-function"></a><span data-ttu-id="435dd-103">Função MSOTINT</span><span class="sxs-lookup"><span data-stu-id="435dd-103">MSOTINT Function</span></span>

<span data-ttu-id="435dd-104">Modifica a cor aumentando a luminosidade pelo percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="435dd-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="435dd-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="435dd-105">Version Information</span></span>

<span data-ttu-id="435dd-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="435dd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="435dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="435dd-107">Syntax</span></span>

<span data-ttu-id="435dd-108">MSOTINT (\* \* *cor* \* \*, \* \* *deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="435dd-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="435dd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="435dd-109">Parameters</span></span>

|<span data-ttu-id="435dd-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="435dd-110">**Name**</span></span>|<span data-ttu-id="435dd-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="435dd-111">**Required/Optional**</span></span>|<span data-ttu-id="435dd-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="435dd-112">**Data Type**</span></span>|<span data-ttu-id="435dd-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="435dd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="435dd-114">_color_</span><span class="sxs-lookup"><span data-stu-id="435dd-114">_color_</span></span> <br/> |<span data-ttu-id="435dd-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="435dd-115">Required</span></span>  <br/> |<span data-ttu-id="435dd-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="435dd-116">**RGB**</span></span> <br/> |<span data-ttu-id="435dd-117">O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.</span><span class="sxs-lookup"><span data-stu-id="435dd-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="435dd-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="435dd-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="435dd-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="435dd-119">Required</span></span>  <br/> |<span data-ttu-id="435dd-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="435dd-120">**Integer**</span></span> <br/> |<span data-ttu-id="435dd-121">A alteração percentual em direção ao branco (-100%) ou preto (100%) do valor de _cor_ .</span><span class="sxs-lookup"><span data-stu-id="435dd-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="435dd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="435dd-122">Remarks</span></span>

<span data-ttu-id="435dd-123">Quanto mais próximo o valor de _cor_ for branco ou preto, menor será a alteração na tonalidade produzida por um valor _deltaLum_ específico.</span><span class="sxs-lookup"><span data-stu-id="435dd-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

