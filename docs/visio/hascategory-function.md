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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433350"
---
# <a name="hascategory-function"></a><span data-ttu-id="475c6-103">Método HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="475c6-103">HASCATEGORY Function</span></span>

<span data-ttu-id="475c6-104">Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.</span><span class="sxs-lookup"><span data-stu-id="475c6-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="475c6-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="475c6-105">Version Information</span></span>

<span data-ttu-id="475c6-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="475c6-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="475c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="475c6-107">Syntax</span></span>

<span data-ttu-id="475c6-108">HASCATEGORY (\* \* *categoria* \* \*)</span><span class="sxs-lookup"><span data-stu-id="475c6-108">HASCATEGORY(\*\* *category* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="475c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="475c6-109">Parameters</span></span>

|<span data-ttu-id="475c6-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="475c6-110">**Name**</span></span>|<span data-ttu-id="475c6-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="475c6-111">**Required/Optional**</span></span>|<span data-ttu-id="475c6-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="475c6-112">**Data Type**</span></span>|<span data-ttu-id="475c6-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="475c6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="475c6-114">_Categorias_</span><span class="sxs-lookup"><span data-stu-id="475c6-114">_category_</span></span> <br/> |<span data-ttu-id="475c6-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="475c6-115">Required</span></span>  <br/> |<span data-ttu-id="475c6-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="475c6-116">**String**</span></span> <br/> |<span data-ttu-id="475c6-117">A categoria a ser procurada.</span><span class="sxs-lookup"><span data-stu-id="475c6-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="475c6-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="475c6-118">Return value</span></span>

 <span data-ttu-id="475c6-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="475c6-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="475c6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="475c6-120">Remarks</span></span>

 <span data-ttu-id="475c6-121">As *categorias* são cadeias de caracteres definidas pelo usuário que você pode usar para categorizar formas.</span><span class="sxs-lookup"><span data-stu-id="475c6-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="475c6-122">Você pode definir categorias na célula User.msvShapeCategories do ShapeSheet para uma forma.</span><span class="sxs-lookup"><span data-stu-id="475c6-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="475c6-123">Pode também definir várias categorias para uma forma separando-as com ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="475c6-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

