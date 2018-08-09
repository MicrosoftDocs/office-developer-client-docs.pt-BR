---
title: Função MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica a cor reduzindo a luminosidade pelo percentual especificado.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772403"
---
# <a name="msoshade-function"></a><span data-ttu-id="7a6de-103">Função MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="7a6de-103">MSOSHADE Function</span></span>

<span data-ttu-id="7a6de-104">Modifica a cor reduzindo a luminosidade pelo percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="7a6de-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7a6de-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="7a6de-105">Version Information</span></span>

<span data-ttu-id="7a6de-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="7a6de-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7a6de-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a6de-107">Syntax</span></span>

<span data-ttu-id="7a6de-108">MSOSHADE (* * *cor* * *, * * *- deltaLum* * *)</span><span class="sxs-lookup"><span data-stu-id="7a6de-108">MSOSHADE(** *color* **, ** *-deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7a6de-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a6de-109">Parameters</span></span>

|<span data-ttu-id="7a6de-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="7a6de-110">**Name**</span></span>|<span data-ttu-id="7a6de-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="7a6de-111">**Required/Optional**</span></span>|<span data-ttu-id="7a6de-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="7a6de-112">**Data Type**</span></span>|<span data-ttu-id="7a6de-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7a6de-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7a6de-114">_color_</span><span class="sxs-lookup"><span data-stu-id="7a6de-114">_color_</span></span> <br/> |<span data-ttu-id="7a6de-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7a6de-115">Required</span></span>  <br/> |<span data-ttu-id="7a6de-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="7a6de-116">**RGB**</span></span> <br/> |<span data-ttu-id="7a6de-117">O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.</span><span class="sxs-lookup"><span data-stu-id="7a6de-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="7a6de-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="7a6de-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="7a6de-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7a6de-119">Required</span></span>  <br/> |<span data-ttu-id="7a6de-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7a6de-120">**Integer**</span></span> <br/> |<span data-ttu-id="7a6de-121">A alteração percentual entre branco (-100%) ou preto (100%) no valor _color_ .</span><span class="sxs-lookup"><span data-stu-id="7a6de-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a6de-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a6de-122">Remarks</span></span>

<span data-ttu-id="7a6de-123">Quanto mais perto o valor _color_ estiver de branco ou preto, menor será a alteração no sombreamento produzido por um valor específico _- deltaLum_ .</span><span class="sxs-lookup"><span data-stu-id="7a6de-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

