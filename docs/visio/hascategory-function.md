---
title: Função HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360162"
---
# <a name="hascategory-function"></a><span data-ttu-id="4738e-103">Método HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="4738e-103">HASCATEGORY Function</span></span>

<span data-ttu-id="4738e-104">Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.</span><span class="sxs-lookup"><span data-stu-id="4738e-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4738e-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="4738e-105">Version Information</span></span>

<span data-ttu-id="4738e-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="4738e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4738e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4738e-107">Syntax</span></span>

<span data-ttu-id="4738e-108">HASCATEGORY (\* \* *categoria* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4738e-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4738e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4738e-109">Parameters</span></span>

|<span data-ttu-id="4738e-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4738e-110">**Name**</span></span>|<span data-ttu-id="4738e-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="4738e-111">**Required/Optional**</span></span>|<span data-ttu-id="4738e-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4738e-112">**Data Type**</span></span>|<span data-ttu-id="4738e-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4738e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4738e-114">_Categorias_</span><span class="sxs-lookup"><span data-stu-id="4738e-114">_category_</span></span> <br/> |<span data-ttu-id="4738e-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4738e-115">Required</span></span>  <br/> |<span data-ttu-id="4738e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="4738e-116">**String**</span></span> <br/> |<span data-ttu-id="4738e-117">A categoria a ser procurada.</span><span class="sxs-lookup"><span data-stu-id="4738e-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4738e-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4738e-118">Return value</span></span>

 <span data-ttu-id="4738e-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4738e-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4738e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4738e-120">Remarks</span></span>

 <span data-ttu-id="4738e-121">As *categorias* são cadeias de caracteres definidas pelo usuário que você pode usar para categorizar formas.</span><span class="sxs-lookup"><span data-stu-id="4738e-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="4738e-122">Você pode definir categorias na célula User.msvShapeCategories do ShapeSheet para uma forma.</span><span class="sxs-lookup"><span data-stu-id="4738e-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="4738e-123">Pode também definir várias categorias para uma forma separando-as com ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="4738e-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

