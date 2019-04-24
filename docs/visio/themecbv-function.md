---
title: Função THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado, armazenado nas configurações de gradiente do tema ativo.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332260"
---
# <a name="themecbv-function"></a><span data-ttu-id="854cf-103">Função THEMECBV</span><span class="sxs-lookup"><span data-stu-id="854cf-103">THEMECBV Function</span></span>

<span data-ttu-id="854cf-104">Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor de tonalidade ou sombreamento especificado, armazenado nas configurações de gradiente do tema ativo.</span><span class="sxs-lookup"><span data-stu-id="854cf-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="854cf-105">Informações sobre a versão</span><span class="sxs-lookup"><span data-stu-id="854cf-105">Version Information</span></span>

<span data-ttu-id="854cf-106">Version Added: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="854cf-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="854cf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="854cf-107">Syntax</span></span>

 <span data-ttu-id="854cf-108">**THEMECBV** ( _Color_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="854cf-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="854cf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="854cf-109">Parameters</span></span>

|<span data-ttu-id="854cf-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="854cf-110">**Name**</span></span>|<span data-ttu-id="854cf-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="854cf-111">**Required/Optional**</span></span>|<span data-ttu-id="854cf-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="854cf-112">**Data Type**</span></span>|<span data-ttu-id="854cf-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="854cf-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="854cf-114">_color_</span><span class="sxs-lookup"><span data-stu-id="854cf-114">_color_</span></span> <br/> |<span data-ttu-id="854cf-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="854cf-115">Required</span></span>  <br/> |<span data-ttu-id="854cf-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="854cf-116">**Number**</span></span> <br/> |<span data-ttu-id="854cf-117">Um número que representa um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="854cf-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="854cf-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="854cf-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="854cf-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="854cf-119">Required</span></span>  <br/> |<span data-ttu-id="854cf-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="854cf-120">**Number**</span></span> <br/> |<span data-ttu-id="854cf-121">O limite de gradiente (tonalidade ou sombreamento) armazenado nas configurações de gradiente do tema ativo a ser aplicado à cor.</span><span class="sxs-lookup"><span data-stu-id="854cf-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="854cf-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="854cf-122">Return value</span></span>

 <span data-ttu-id="854cf-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="854cf-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="854cf-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="854cf-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="854cf-125">A função THEMECBV não fará nada com a cor passada como um argumento se o modo rápido atribuído à forma não tiver um gradiente.</span><span class="sxs-lookup"><span data-stu-id="854cf-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="854cf-126">As configurações de gradiente em um tema são uma série de interrupções de gradiente numeradas que correspondem a uma "luminosidade" (tonalidade) ou "escurecer" (sombreamento).</span><span class="sxs-lookup"><span data-stu-id="854cf-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="854cf-127">Esses tons e matizes são aplicados a uma cor de base para criar um efeito de cor de gradiente.</span><span class="sxs-lookup"><span data-stu-id="854cf-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="854cf-128">A função **THEMECBV** tem uma entrada de cor e gera a cor após ela ter sido modificada pela tonalidade ou sombra da parada de gradiente especificada.</span><span class="sxs-lookup"><span data-stu-id="854cf-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="854cf-129">As tonalidades e graduais vêm da definição do tema, se o estilo rápido atual contiver um preenchimento gradual.</span><span class="sxs-lookup"><span data-stu-id="854cf-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="854cf-130">Se o estilo rápido ativo não especificar um preenchimento de gradiente ou a forma for definida como nenhum tema, essa fórmula simplesmente retornará a cor que foi passada para o primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="854cf-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="854cf-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="854cf-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="854cf-132">Retorna a cor criada por meio da aplicação da tonalidade ou do sombreamento na quinta parada de gradiente para a cor especificada na célula **FillForegnd** .</span><span class="sxs-lookup"><span data-stu-id="854cf-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="854cf-133">Retorna um sombreamento ou tonalidade de vermelho criado aplicando a segunda parada de gradiente a uma cor de base vermelha.</span><span class="sxs-lookup"><span data-stu-id="854cf-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

