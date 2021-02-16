---
title: Função MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica a cor reduzindo a luminosidade pelo percentual especificado.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414491"
---
# <a name="msoshade-function"></a><span data-ttu-id="4e5a6-103">Função MSOSHADE</span><span class="sxs-lookup"><span data-stu-id="4e5a6-103">MSOSHADE Function</span></span>

<span data-ttu-id="4e5a6-104">Modifica a cor reduzindo a luminosidade pelo percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4e5a6-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="4e5a6-105">Version Information</span></span>

<span data-ttu-id="4e5a6-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="4e5a6-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4e5a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e5a6-107">Syntax</span></span>

<span data-ttu-id="4e5a6-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4e5a6-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e5a6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e5a6-109">Parameters</span></span>

|<span data-ttu-id="4e5a6-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="4e5a6-110">**Name**</span></span>|<span data-ttu-id="4e5a6-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="4e5a6-111">**Required/Optional**</span></span>|<span data-ttu-id="4e5a6-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4e5a6-112">**Data Type**</span></span>|<span data-ttu-id="4e5a6-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4e5a6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e5a6-114">_color_</span><span class="sxs-lookup"><span data-stu-id="4e5a6-114">_color_</span></span> <br/> |<span data-ttu-id="4e5a6-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4e5a6-115">Required</span></span>  <br/> |<span data-ttu-id="4e5a6-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="4e5a6-116">**RGB**</span></span> <br/> |<span data-ttu-id="4e5a6-117">O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="4e5a6-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="4e5a6-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="4e5a6-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4e5a6-119">Required</span></span>  <br/> |<span data-ttu-id="4e5a6-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="4e5a6-120">**Integer**</span></span> <br/> |<span data-ttu-id="4e5a6-121">A porcentagem de alteração em relação ao branco (-100%) ou preto (100%) do valor  _de_ cor.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e5a6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e5a6-122">Remarks</span></span>

<span data-ttu-id="4e5a6-123">Quanto mais próximo  _o valor_ de cor for branco ou preto, menor será a alteração no sombreado produzido por um  _valor -deltaLum_ específico.</span><span class="sxs-lookup"><span data-stu-id="4e5a6-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

