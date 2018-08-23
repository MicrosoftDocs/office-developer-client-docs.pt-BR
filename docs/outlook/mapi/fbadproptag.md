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
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582879"
---
# <a name="fbadproptag"></a><span data-ttu-id="01073-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="01073-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="01073-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01073-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01073-105">Valida uma marca de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="01073-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01073-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="01073-106">Header file:</span></span>  <br/> |<span data-ttu-id="01073-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="01073-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="01073-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="01073-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01073-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01073-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01073-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="01073-110">Called by:</span></span>  <br/> |<span data-ttu-id="01073-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="01073-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="01073-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01073-112">Parameters</span></span>

 <span data-ttu-id="01073-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="01073-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="01073-114">[in] A marca de propriedade a ser validado.</span><span class="sxs-lookup"><span data-stu-id="01073-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01073-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="01073-115">Return value</span></span>

<span data-ttu-id="01073-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="01073-116">TRUE</span></span> 
  
> <span data-ttu-id="01073-117">A marca de propriedade especificado não é uma marca de propriedade MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="01073-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="01073-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="01073-118">FALSE</span></span> 
  
> <span data-ttu-id="01073-119">A marca de propriedade especificado é uma marca de propriedade MAPI válida.</span><span class="sxs-lookup"><span data-stu-id="01073-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01073-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="01073-120">Remarks</span></span>

<span data-ttu-id="01073-121">A função **FBadPropTag** valida a marca de propriedade especificado com base nas definições de MAPI.</span><span class="sxs-lookup"><span data-stu-id="01073-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="01073-122">Ele faz sures que o tipo de propriedade é um dos tipos definidos pelo MAPI e que o identificador de propriedade é definido para ser desse tipo.</span><span class="sxs-lookup"><span data-stu-id="01073-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01073-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="01073-123">See also</span></span>



[<span data-ttu-id="01073-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="01073-124">FBadProp</span></span>](fbadprop.md)

