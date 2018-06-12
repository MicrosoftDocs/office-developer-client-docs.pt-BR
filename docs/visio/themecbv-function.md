---
title: Função THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor especificado tonalidade armazenado nas configurações do gradientes do tema ativo.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773141"
---
# <a name="themecbv-function"></a><span data-ttu-id="bd6c1-103">Função THEMECBV</span><span class="sxs-lookup"><span data-stu-id="bd6c1-103">THEMECBV Function</span></span>

<span data-ttu-id="bd6c1-104">Retorna um valor RGB ou um inteiro que representa um índice na paleta de cores do documento, onde a cor (número) passada como um argumento foi modificada pelo valor especificado tonalidade armazenado nas configurações do gradientes do tema ativo.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="bd6c1-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="bd6c1-105">Version Information</span></span>

<span data-ttu-id="bd6c1-106">Versão adicionada: Visio 2013</span><span class="sxs-lookup"><span data-stu-id="bd6c1-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bd6c1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd6c1-107">Syntax</span></span>

 <span data-ttu-id="bd6c1-108">**THEMECBV** ( _cor_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="bd6c1-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="bd6c1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd6c1-109">Parameters</span></span>

|<span data-ttu-id="bd6c1-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-110">**Name**</span></span>|<span data-ttu-id="bd6c1-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-111">**Required/Optional**</span></span>|<span data-ttu-id="bd6c1-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-112">**Data Type**</span></span>|<span data-ttu-id="bd6c1-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bd6c1-114">_color_</span><span class="sxs-lookup"><span data-stu-id="bd6c1-114">_color_</span></span> <br/> |<span data-ttu-id="bd6c1-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd6c1-115">Required</span></span>  <br/> |<span data-ttu-id="bd6c1-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-116">**Number**</span></span> <br/> |<span data-ttu-id="bd6c1-117">Um número representando um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="bd6c1-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="bd6c1-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="bd6c1-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd6c1-119">Required</span></span>  <br/> |<span data-ttu-id="bd6c1-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-120">**Number**</span></span> <br/> |<span data-ttu-id="bd6c1-121">Parada de gradiente (tonalidade ou sombreamento) armazenada nas configurações do gradientes do tema ativo a ser aplicado à cor.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="bd6c1-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd6c1-122">Return value</span></span>

 <span data-ttu-id="bd6c1-123">**Número**</span><span class="sxs-lookup"><span data-stu-id="bd6c1-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd6c1-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="bd6c1-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="bd6c1-125">A função THEMECBV não faz nada à cor passada como um argumento se a propriedade QuickStyle que é atribuída à forma não tiver um preenchimento gradiente.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="bd6c1-126">As configurações de gradiente em um tema são uma série de paradas de gradiente numeradas que correspondem a um (tonalidade) "iluminação" ou "escurecimento" (sombra).</span><span class="sxs-lookup"><span data-stu-id="bd6c1-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="bd6c1-127">Esses tons e matizes são aplicados a uma cor base para criar um efeito de gradiente de cores.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="bd6c1-128">A função **THEMECBV** recebe uma entrada de cor e a cor de saídas depois que ele tiver sido modificado pela tonalidade ou o sombreamento da parada do gradiente especificado.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="bd6c1-129">Os matizes e tons vêm de definição do tema, se o estilo rápido atual contiver um preenchimento de gradiente.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="bd6c1-130">Se o estilo rápido ativo não especificar que um preenchimento gradual ou a forma estiver definida como Nenhum tema, esta fórmula simplesmente retorna a cor que é passada para o primeiro argumento.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bd6c1-131">Example</span><span class="sxs-lookup"><span data-stu-id="bd6c1-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="bd6c1-132">Retorna a cor criada aplicando a tonalidade ou o sombreamento do quinto parada de gradiente do gradiente da cor especificada na célula **FillForegnd** .</span><span class="sxs-lookup"><span data-stu-id="bd6c1-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="bd6c1-133">Retorna um sombreamento ou tonalidade de vermelho criada aplicando-a segunda parada de gradiente com uma cor base de vermelho.</span><span class="sxs-lookup"><span data-stu-id="bd6c1-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

