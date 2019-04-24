---
title: Função GOTOPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Exibe a página que tem o nome PageName na janela ativa no momento.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302965"
---
# <a name="gotopage-function"></a><span data-ttu-id="a69d7-103">Função GOTOPAGE</span><span class="sxs-lookup"><span data-stu-id="a69d7-103">GOTOPAGE Function</span></span>

<span data-ttu-id="a69d7-104">Exibe a página que tem o nome *PageName* na janela ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="a69d7-104">Displays the page that has the name  *pagename*  in the currently active window.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a69d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a69d7-105">Syntax</span></span>

<span data-ttu-id="a69d7-106">IRPARAPÁGINA ("\* \* *PageName* \* \*")</span><span class="sxs-lookup"><span data-stu-id="a69d7-106">GOTOPAGE(" \*\* *pagename* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a69d7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a69d7-107">Parameters</span></span>

|<span data-ttu-id="a69d7-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a69d7-108">**Name**</span></span>|<span data-ttu-id="a69d7-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a69d7-109">**Required/Optional**</span></span>|<span data-ttu-id="a69d7-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a69d7-110">**Data Type**</span></span>|<span data-ttu-id="a69d7-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a69d7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a69d7-112">_pagename_</span><span class="sxs-lookup"><span data-stu-id="a69d7-112">_pagename_</span></span> <br/> |<span data-ttu-id="a69d7-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a69d7-113">Required</span></span>  <br/> |<span data-ttu-id="a69d7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a69d7-114">**String**</span></span> <br/> |<span data-ttu-id="a69d7-115">O nome da página a ser acessada.</span><span class="sxs-lookup"><span data-stu-id="a69d7-115">The name of the page to go to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a69d7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a69d7-116">Remarks</span></span>

<span data-ttu-id="a69d7-117">Se uma janela já estiver exibindo a página, essa janela ficará ativa.</span><span class="sxs-lookup"><span data-stu-id="a69d7-117">If a window is already displaying the page, that window becomes active.</span></span> <span data-ttu-id="a69d7-118">Se *PageName* não existir, o aplicativo tentará navegar para https:// *PageName* /.</span><span class="sxs-lookup"><span data-stu-id="a69d7-118">If  *pagename*  does not exist, the application attempts to navigate to https://  *pagename*  /.</span></span> <span data-ttu-id="a69d7-119">Se o Visio estiver agindo como um servidor in-loco, a função GOTOPAGE não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="a69d7-119">If Visio is acting as an in-place server, the GOTOPAGE function has no effect.</span></span> 
  
<span data-ttu-id="a69d7-120">É possível utilizar a função HYPERLINK para navegar por qualquer caminho DOS, UNC ou URL.</span><span class="sxs-lookup"><span data-stu-id="a69d7-120">You can use the HYPERLINK function to navigate to any DOS, UNC, or URL path.</span></span> 
  
<span data-ttu-id="a69d7-p102">Em versões anteriores dos produtos Visio, essa função aparece como _GOTOPAGE. As versões 4.0 e posteriores do Visio aceitam os dois estilos.</span><span class="sxs-lookup"><span data-stu-id="a69d7-p102">In earlier versions of Visio products, this function appears as _GOTOPAGE. Visio versions 4.0 and later accept either style.</span></span> 
  

