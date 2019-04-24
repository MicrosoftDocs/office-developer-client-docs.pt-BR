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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337244"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="68e14-103">Função CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="68e14-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="68e14-104">Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="68e14-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="68e14-105">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="68e14-105">Version Information</span></span>

<span data-ttu-id="68e14-106">Version Added: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="68e14-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="68e14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68e14-107">Syntax</span></span>

<span data-ttu-id="68e14-108">CALLOUTTARGETREF ()!</span><span class="sxs-lookup"><span data-stu-id="68e14-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="68e14-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="68e14-109">Return value</span></span>

<span data-ttu-id="68e14-110">Referência do ShapeSheet</span><span class="sxs-lookup"><span data-stu-id="68e14-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68e14-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="68e14-111">Remarks</span></span>

<span data-ttu-id="68e14-112">Se a forma não for uma forma de texto explicativo ou não estiver associada a uma forma de destino, CALLOUTTARGETREF retornará #REF.</span><span class="sxs-lookup"><span data-stu-id="68e14-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="68e14-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="68e14-113">Example</span></span>

<span data-ttu-id="68e14-114">CALLOUTTARGETREF ()! Height</span><span class="sxs-lookup"><span data-stu-id="68e14-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="68e14-115">Retorna o valor na célula Height da forma associada ao texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="68e14-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

