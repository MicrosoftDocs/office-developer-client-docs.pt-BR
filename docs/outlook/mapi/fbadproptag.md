---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340996"
---
# <a name="fbadproptag"></a><span data-ttu-id="2aa11-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="2aa11-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="2aa11-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aa11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aa11-105">Valida uma marca de propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="2aa11-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aa11-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2aa11-106">Header file:</span></span>  <br/> |<span data-ttu-id="2aa11-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2aa11-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2aa11-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2aa11-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2aa11-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2aa11-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2aa11-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2aa11-110">Called by:</span></span>  <br/> |<span data-ttu-id="2aa11-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2aa11-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="2aa11-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2aa11-112">Parameters</span></span>

 <span data-ttu-id="2aa11-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="2aa11-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="2aa11-114">no A marca de propriedade a ser validada.</span><span class="sxs-lookup"><span data-stu-id="2aa11-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2aa11-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2aa11-115">Return value</span></span>

<span data-ttu-id="2aa11-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="2aa11-116">TRUE</span></span> 
  
> <span data-ttu-id="2aa11-117">A marca de propriedade especificada não é uma marca de propriedade MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="2aa11-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="2aa11-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="2aa11-118">FALSE</span></span> 
  
> <span data-ttu-id="2aa11-119">A marca de propriedade especificada é uma marca de propriedade MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="2aa11-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2aa11-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aa11-120">Remarks</span></span>

<span data-ttu-id="2aa11-121">A função **FBadPropTag** valida a marca de propriedade especificada com base nas definições de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2aa11-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="2aa11-122">Ele garante que o tipo de propriedade é um dos tipos definidos por MAPI e que o identificador de propriedade é definido para ser daquele tipo.</span><span class="sxs-lookup"><span data-stu-id="2aa11-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2aa11-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2aa11-123">See also</span></span>



[<span data-ttu-id="2aa11-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="2aa11-124">FBadProp</span></span>](fbadprop.md)

