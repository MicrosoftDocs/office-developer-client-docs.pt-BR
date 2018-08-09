---
title: Função MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica a cor aumentando a luminosidade pelo percentual especificado.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772432"
---
# <a name="msotint-function"></a><span data-ttu-id="15441-103">Função MSOTINT</span><span class="sxs-lookup"><span data-stu-id="15441-103">MSOTINT Function</span></span>

<span data-ttu-id="15441-104">Modifica a cor aumentando a luminosidade pelo percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="15441-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="15441-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="15441-105">Version Information</span></span>

<span data-ttu-id="15441-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="15441-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="15441-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15441-107">Syntax</span></span>

<span data-ttu-id="15441-108">MSOTINT (* * *cor* * *, * * *deltaLum* * *)</span><span class="sxs-lookup"><span data-stu-id="15441-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="15441-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15441-109">Parameters</span></span>

|<span data-ttu-id="15441-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="15441-110">**Name**</span></span>|<span data-ttu-id="15441-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="15441-111">**Required/Optional**</span></span>|<span data-ttu-id="15441-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="15441-112">**Data Type**</span></span>|<span data-ttu-id="15441-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="15441-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="15441-114">_color_</span><span class="sxs-lookup"><span data-stu-id="15441-114">_color_</span></span> <br/> |<span data-ttu-id="15441-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="15441-115">Required</span></span>  <br/> |<span data-ttu-id="15441-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="15441-116">**RGB**</span></span> <br/> |<span data-ttu-id="15441-117">O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.</span><span class="sxs-lookup"><span data-stu-id="15441-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="15441-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="15441-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="15441-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="15441-119">Required</span></span>  <br/> |<span data-ttu-id="15441-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="15441-120">**Integer**</span></span> <br/> |<span data-ttu-id="15441-121">A alteração percentual entre branco (-100%) ou preto (100%) no valor _color_ .</span><span class="sxs-lookup"><span data-stu-id="15441-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15441-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="15441-122">Remarks</span></span>

<span data-ttu-id="15441-123">Quanto mais perto o valor _color_ estiver de branco ou preto, menor será a alteração na tonalidade produzida por um valor específico _deltaLum_ .</span><span class="sxs-lookup"><span data-stu-id="15441-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

