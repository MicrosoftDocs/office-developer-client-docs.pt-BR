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
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578847"
---
# <a name="fbadprop"></a><span data-ttu-id="dab88-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="dab88-103">FBadProp</span></span>

  
  
<span data-ttu-id="dab88-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab88-105">Valida uma propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="dab88-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dab88-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dab88-106">Header File</span></span>  <br/> |<span data-ttu-id="dab88-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="dab88-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="dab88-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dab88-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dab88-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dab88-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dab88-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="dab88-110">Called by:</span></span>  <br/> |<span data-ttu-id="dab88-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="dab88-111">Service Providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="dab88-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dab88-112">Parameters</span></span>

 <span data-ttu-id="dab88-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="dab88-113">_lpprop_</span></span>
  
> <span data-ttu-id="dab88-114">[in] Uma estrutura [SPropValue](spropvalue.md) que define a propriedade a ser validada.</span><span class="sxs-lookup"><span data-stu-id="dab88-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dab88-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dab88-115">Return value</span></span>

<span data-ttu-id="dab88-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="dab88-116">TRUE</span></span> 
  
> <span data-ttu-id="dab88-117">A propriedade especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="dab88-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="dab88-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="dab88-118">FALSE</span></span> 
  
> <span data-ttu-id="dab88-119">A propriedade especificada é válida.</span><span class="sxs-lookup"><span data-stu-id="dab88-119">The specified unit is not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dab88-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dab88-120">Remarks</span></span>

<span data-ttu-id="dab88-121">Um provedor de serviços pode chamar a função **FBadProp** por diversos motivos; por exemplo, para se preparar para uma chamada para o método [IMAPIProp::SetProps](imapiprop-setprops.md) configurando uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="dab88-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="dab88-122">**FBadProp** valida a propriedade especificada, dependendo do tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="dab88-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="dab88-123">Por exemplo, se a propriedade é booliana, **FBadProp** garante que o respectivo valor seja TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="dab88-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="dab88-124">Quado a propriedade é binária, **FBadProp** verifica o ponteiro e o tamanho e garante que ela seja alocada corretamente.</span><span class="sxs-lookup"><span data-stu-id="dab88-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dab88-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dab88-125">See also</span></span>



[<span data-ttu-id="dab88-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="dab88-126">FBadPropTag</span></span>](fbadproptag.md)

