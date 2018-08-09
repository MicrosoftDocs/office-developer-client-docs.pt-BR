---
title: Função HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772011"
---
# <a name="hascategory-function"></a><span data-ttu-id="db94e-103">Método HASCATEGORY</span><span class="sxs-lookup"><span data-stu-id="db94e-103">HASCATEGORY Function</span></span>

<span data-ttu-id="db94e-104">Retornará TRUE se a cadeia de caracteres especificada for encontrada na lista de categorias da forma.</span><span class="sxs-lookup"><span data-stu-id="db94e-104">Returns TRUE if the specified string is found in the shape's category list.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="db94e-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="db94e-105">Version Information</span></span>

<span data-ttu-id="db94e-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="db94e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="db94e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db94e-107">Syntax</span></span>

<span data-ttu-id="db94e-108">HASCATEGORY (* * *categoria* * *)</span><span class="sxs-lookup"><span data-stu-id="db94e-108">HASCATEGORY(** *category* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="db94e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db94e-109">Parameters</span></span>

|<span data-ttu-id="db94e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="db94e-110">**Name**</span></span>|<span data-ttu-id="db94e-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="db94e-111">**Required/Optional**</span></span>|<span data-ttu-id="db94e-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="db94e-112">**Data Type**</span></span>|<span data-ttu-id="db94e-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="db94e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="db94e-114">_category_</span><span class="sxs-lookup"><span data-stu-id="db94e-114">_category_</span></span> <br/> |<span data-ttu-id="db94e-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="db94e-115">Required</span></span>  <br/> |<span data-ttu-id="db94e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="db94e-116">**String**</span></span> <br/> |<span data-ttu-id="db94e-117">A categoria a ser procurada.</span><span class="sxs-lookup"><span data-stu-id="db94e-117">The category to search for.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="db94e-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="db94e-118">Return value</span></span>

 <span data-ttu-id="db94e-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="db94e-119">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db94e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="db94e-120">Remarks</span></span>

 <span data-ttu-id="db94e-121">*Categorias* são cadeias de caracteres definidas pelo usuário que podem ser usados para categorizar as formas.</span><span class="sxs-lookup"><span data-stu-id="db94e-121">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="db94e-122">Você pode definir categorias na célula User.msvShapeCategories na ShapeSheet de uma forma.</span><span class="sxs-lookup"><span data-stu-id="db94e-122">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="db94e-123">Você pode definir várias categorias para uma forma, separando as categorias por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="db94e-123">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  

