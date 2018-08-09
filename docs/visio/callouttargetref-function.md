---
title: Função CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771419"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="06d3a-103">Função CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="06d3a-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="06d3a-104">Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="06d3a-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="06d3a-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="06d3a-105">Version Information</span></span>

<span data-ttu-id="06d3a-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="06d3a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="06d3a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06d3a-107">Syntax</span></span>

<span data-ttu-id="06d3a-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="06d3a-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="06d3a-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="06d3a-109">Return value</span></span>

<span data-ttu-id="06d3a-110">Referência do ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="06d3a-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06d3a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="06d3a-111">Remarks</span></span>

<span data-ttu-id="06d3a-112">Se a forma não for uma forma de texto explicativo, ou se ele não estiver associado uma forma de destino, CALLOUTTARGETREF retornará #REF.</span><span class="sxs-lookup"><span data-stu-id="06d3a-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="06d3a-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="06d3a-113">Example</span></span>

<span data-ttu-id="06d3a-114">CALLOUTTARGETREF()!Height</span><span class="sxs-lookup"><span data-stu-id="06d3a-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="06d3a-115">Retorna o valor na célula Height da forma associada ao texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="06d3a-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

