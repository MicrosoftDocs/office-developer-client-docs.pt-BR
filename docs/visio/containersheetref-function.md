---
title: Função CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Retorna uma referência de planilha para o contêiner especificado que contém a forma.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771603"
---
# <a name="containersheetref-function"></a><span data-ttu-id="a050f-103">Função CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="a050f-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="a050f-104">Retorna uma referência de planilha para o contêiner especificado que contém a forma.</span><span class="sxs-lookup"><span data-stu-id="a050f-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a050f-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="a050f-105">Version Information</span></span>

<span data-ttu-id="a050f-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a050f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a050f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a050f-107">Syntax</span></span>

<span data-ttu-id="a050f-108">CONTAINERSHEETREF (* * *índice* * * * * *[, categoria]* * *)</span><span class="sxs-lookup"><span data-stu-id="a050f-108">CONTAINERSHEETREF(** *index* ** ** *[, category]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a050f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a050f-109">Parameters</span></span>

|<span data-ttu-id="a050f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a050f-110">**Name**</span></span>|<span data-ttu-id="a050f-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="a050f-111">**Required/Optional**</span></span>|<span data-ttu-id="a050f-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a050f-112">**Data Type**</span></span>|<span data-ttu-id="a050f-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a050f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a050f-114">_índice_</span><span class="sxs-lookup"><span data-stu-id="a050f-114">_index_</span></span> <br/> |<span data-ttu-id="a050f-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a050f-115">Required</span></span>  <br/> |<span data-ttu-id="a050f-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a050f-116">**Integer**</span></span> <br/> |<span data-ttu-id="a050f-p101">O índice baseado em 1 do contêiner. Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a050f-p101">The 1-based index of the container. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="a050f-119">_category_</span><span class="sxs-lookup"><span data-stu-id="a050f-119">_category_</span></span> <br/> |<span data-ttu-id="a050f-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="a050f-120">Optional</span></span>  <br/> |<span data-ttu-id="a050f-121">**String**</span><span class="sxs-lookup"><span data-stu-id="a050f-121">**String**</span></span> <br/> |<span data-ttu-id="a050f-p102">A categoria do contêiner. Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a050f-p102">The category of the container. See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a050f-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a050f-124">Return value</span></span>

<span data-ttu-id="a050f-125">Referência do ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="a050f-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a050f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="a050f-126">Remarks</span></span>

<span data-ttu-id="a050f-127">O índice de um contêiner é calculado com base na ordem Z dos contêineres, de frente para trás.</span><span class="sxs-lookup"><span data-stu-id="a050f-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="a050f-128">*Categorias* são cadeias de caracteres definidas pelo usuário que podem ser usados para categorizar as formas.</span><span class="sxs-lookup"><span data-stu-id="a050f-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="a050f-129">Você pode definir categorias na célula User.msvShapeCategories na ShapeSheet de uma forma.</span><span class="sxs-lookup"><span data-stu-id="a050f-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="a050f-130">Você pode definir várias categorias para uma forma, separando as categorias por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="a050f-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="a050f-131">Se a forma não for membro de um contêiner ou não houver nenhum contêiner que corresponda tanto à categoria como ao número de índice especificado, CONTAINERSHEETREF retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="a050f-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="a050f-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a050f-132">Example</span></span>

<span data-ttu-id="a050f-133">CONTAINERSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="a050f-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="a050f-134">Retorna o valor na célula Height do contêiner que está mais à frente na página à qual a forma pertence.</span><span class="sxs-lookup"><span data-stu-id="a050f-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

