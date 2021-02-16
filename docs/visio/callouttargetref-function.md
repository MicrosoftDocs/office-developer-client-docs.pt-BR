---
title: Função CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423010"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="38303-103">Função CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="38303-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="38303-104">Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="38303-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="38303-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="38303-105">Version Information</span></span>

<span data-ttu-id="38303-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="38303-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="38303-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38303-107">Syntax</span></span>

<span data-ttu-id="38303-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="38303-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="38303-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="38303-109">Return value</span></span>

<span data-ttu-id="38303-110">Referência do ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="38303-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38303-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="38303-111">Remarks</span></span>

<span data-ttu-id="38303-112">Se a forma não for uma forma de explicação ou não estiver associada a uma forma de destino, CALLOUTTARGETREF retornará #REF.</span><span class="sxs-lookup"><span data-stu-id="38303-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="38303-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="38303-113">Example</span></span>

<span data-ttu-id="38303-114">CALLOUTTARGETREF()! Altura</span><span class="sxs-lookup"><span data-stu-id="38303-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="38303-115">Retorna o valor na célula Height da forma associada ao texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="38303-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

