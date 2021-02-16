---
title: Função CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Retorna uma referência de planilha para o contêiner especificado que contém a forma.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437263"
---
# <a name="containersheetref-function"></a><span data-ttu-id="8d528-103">Função CONTAINERSHEETREF</span><span class="sxs-lookup"><span data-stu-id="8d528-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="8d528-104">Retorna uma referência de planilha para o contêiner especificado que contém a forma.</span><span class="sxs-lookup"><span data-stu-id="8d528-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="8d528-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="8d528-105">Version Information</span></span>

<span data-ttu-id="8d528-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="8d528-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d528-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d528-107">Syntax</span></span>

<span data-ttu-id="8d528-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8d528-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d528-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d528-109">Parameters</span></span>

|<span data-ttu-id="8d528-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d528-110">**Name**</span></span>|<span data-ttu-id="8d528-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="8d528-111">**Required/Optional**</span></span>|<span data-ttu-id="8d528-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8d528-112">**Data Type**</span></span>|<span data-ttu-id="8d528-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8d528-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d528-114">_índice_</span><span class="sxs-lookup"><span data-stu-id="8d528-114">_index_</span></span> <br/> |<span data-ttu-id="8d528-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8d528-115">Required</span></span>  <br/> |<span data-ttu-id="8d528-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8d528-116">**Integer**</span></span> <br/> |<span data-ttu-id="8d528-117">O índice baseado em 1 do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8d528-117">The 1-based index of the container.</span></span> <span data-ttu-id="8d528-118">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8d528-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="8d528-119">_category_</span><span class="sxs-lookup"><span data-stu-id="8d528-119">_category_</span></span> <br/> |<span data-ttu-id="8d528-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="8d528-120">Optional</span></span>  <br/> |<span data-ttu-id="8d528-121">**String**</span><span class="sxs-lookup"><span data-stu-id="8d528-121">**String**</span></span> <br/> |<span data-ttu-id="8d528-122">A categoria do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8d528-122">The category of the container.</span></span> <span data-ttu-id="8d528-123">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8d528-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d528-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8d528-124">Return value</span></span>

<span data-ttu-id="8d528-125">Referência do ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="8d528-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d528-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d528-126">Remarks</span></span>

<span data-ttu-id="8d528-127">O índice de um contêiner é calculado com base na ordem Z dos contêineres, de frente para trás.</span><span class="sxs-lookup"><span data-stu-id="8d528-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="8d528-128">*As*  categorias são cadeias de caracteres definidas pelo usuário que você pode usar para categorizar formas.</span><span class="sxs-lookup"><span data-stu-id="8d528-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="8d528-129">Você pode definir categorias na célula User.msvShapeCategories do ShapeSheet para uma forma.</span><span class="sxs-lookup"><span data-stu-id="8d528-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="8d528-130">Pode também definir várias categorias para uma forma separando-as com ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="8d528-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="8d528-131">Se a forma não for membro de um contêiner ou não houver nenhum contêiner que corresponda tanto à categoria como ao número de índice especificado, CONTAINERSHEETREF retornará #REF!.</span><span class="sxs-lookup"><span data-stu-id="8d528-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="8d528-132">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8d528-132">Example</span></span>

<span data-ttu-id="8d528-133">CONTAINERSHEETREF(1)! Altura</span><span class="sxs-lookup"><span data-stu-id="8d528-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="8d528-134">Retorna o valor na célula Height do contêiner que está mais à frente na página à qual a forma pertence.</span><span class="sxs-lookup"><span data-stu-id="8d528-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

