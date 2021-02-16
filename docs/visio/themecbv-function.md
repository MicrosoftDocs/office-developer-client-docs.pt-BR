---
title: Função THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado armazenado nas configurações de gradiente do tema ativo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429135"
---
# <a name="themecbv-function"></a><span data-ttu-id="efccc-103">Função THEMECBV</span><span class="sxs-lookup"><span data-stu-id="efccc-103">THEMECBV Function</span></span>

<span data-ttu-id="efccc-104">Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado armazenado nas configurações de gradiente do tema ativo.</span><span class="sxs-lookup"><span data-stu-id="efccc-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="efccc-105">Informações sobre a versão</span><span class="sxs-lookup"><span data-stu-id="efccc-105">Version Information</span></span>

<span data-ttu-id="efccc-106">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="efccc-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="efccc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efccc-107">Syntax</span></span>

 <span data-ttu-id="efccc-108">**THEMECBV**( _cor_,  _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="efccc-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="efccc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efccc-109">Parameters</span></span>

|<span data-ttu-id="efccc-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="efccc-110">**Name**</span></span>|<span data-ttu-id="efccc-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="efccc-111">**Required/Optional**</span></span>|<span data-ttu-id="efccc-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="efccc-112">**Data Type**</span></span>|<span data-ttu-id="efccc-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="efccc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="efccc-114">_color_</span><span class="sxs-lookup"><span data-stu-id="efccc-114">_color_</span></span> <br/> |<span data-ttu-id="efccc-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="efccc-115">Required</span></span>  <br/> |<span data-ttu-id="efccc-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="efccc-116">**Number**</span></span> <br/> |<span data-ttu-id="efccc-117">Um número que representa um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="efccc-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="efccc-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="efccc-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="efccc-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="efccc-119">Required</span></span>  <br/> |<span data-ttu-id="efccc-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="efccc-120">**Number**</span></span> <br/> |<span data-ttu-id="efccc-121">A marca de gradiente (tonalidade ou sombreamento) armazenada nas configurações de gradiente do tema ativo a ser aplicada à cor.</span><span class="sxs-lookup"><span data-stu-id="efccc-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="efccc-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="efccc-122">Return value</span></span>

 <span data-ttu-id="efccc-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="efccc-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="efccc-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="efccc-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="efccc-125">A função THEMECBV não faz nada com a cor passada como um argumento se o Estilo Rápido atribuído à forma não tiver um gradiente.</span><span class="sxs-lookup"><span data-stu-id="efccc-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="efccc-126">As configurações de gradiente em um tema são uma série de paradas de gradiente numeradas que correspondem a uma "tonalidade" (tonalidade) ou "escurecer" (sombreamento).</span><span class="sxs-lookup"><span data-stu-id="efccc-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="efccc-127">Esses tons e tonalidades são aplicados a uma cor base para criar um efeito de cor gradiente.</span><span class="sxs-lookup"><span data-stu-id="efccc-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="efccc-128">A **função THEMECBV** recebe uma entrada de cor e em saída a cor depois de ter sido modificada pela tonalidade ou sombreamento da parada de gradiente especificada.</span><span class="sxs-lookup"><span data-stu-id="efccc-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="efccc-129">Os tons e tonalidades vêm da definição do tema, se o estilo rápido atual contiver um preenchimento de gradiente.</span><span class="sxs-lookup"><span data-stu-id="efccc-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="efccc-130">Se o Estilo Rápido ativo não especificar um preenchimento de gradiente ou a forma estiver definida como Sem Tema, essa fórmula simplesmente retornará a cor passada para o primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="efccc-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="efccc-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="efccc-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="efccc-132">Retorna a cor criada aplicando a tonalidade ou sombreamento na quinta parada de gradiente do gradiente à cor especificada na **célula FillForegnd.**</span><span class="sxs-lookup"><span data-stu-id="efccc-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="efccc-133">Retorna um sombreamento ou tonalidade de vermelho criado aplicando a segunda parada de gradiente a uma cor base de vermelho.</span><span class="sxs-lookup"><span data-stu-id="efccc-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

