---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 39e10e9139036cc86ec93ea24a89b98125ea6e83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766519"
---
# <a name="fbadprop"></a><span data-ttu-id="417db-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="417db-103">FBadProp</span></span>

  
  
<span data-ttu-id="417db-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="417db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="417db-105">Valida uma propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="417db-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="417db-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="417db-106">Header file:</span></span>  <br/> |<span data-ttu-id="417db-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="417db-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="417db-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="417db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="417db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="417db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="417db-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="417db-110">Called by:</span></span>  <br/> |<span data-ttu-id="417db-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="417db-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="417db-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="417db-112">Parameters</span></span>

 <span data-ttu-id="417db-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="417db-113">_lpprop_</span></span>
  
> <span data-ttu-id="417db-114">[in] Uma estrutura de [SPropValue](spropvalue.md) definindo a propriedade a ser validado.</span><span class="sxs-lookup"><span data-stu-id="417db-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="417db-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="417db-115">Return value</span></span>

<span data-ttu-id="417db-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="417db-116">TRUE</span></span> 
  
> <span data-ttu-id="417db-117">A propriedade especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="417db-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="417db-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="417db-118">FALSE</span></span> 
  
> <span data-ttu-id="417db-119">A propriedade especificada é válida.</span><span class="sxs-lookup"><span data-stu-id="417db-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="417db-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="417db-120">Remarks</span></span>

<span data-ttu-id="417db-121">Um provedor de serviços pode chamar a função **FBadProp** por vários motivos, por exemplo, para se preparar para uma chamada ao método [IMAPIProp::SetProps](imapiprop-setprops.md) a definição de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="417db-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="417db-122">**FBadProp** valida a propriedade especificada, dependendo do tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="417db-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="417db-123">Por exemplo, se a propriedade for Boolean, **FBadProp** disponibilizar sures que seu valor é TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="417db-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="417db-124">Se a propriedade for binária, **FBadProp** verifica o ponteiro e o tamanho e certifica-se de que ele está alocado corretamente.</span><span class="sxs-lookup"><span data-stu-id="417db-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="417db-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="417db-125">See also</span></span>



[<span data-ttu-id="417db-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="417db-126">FBadPropTag</span></span>](fbadproptag.md)

