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
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341038"
---
# <a name="fbadprop"></a><span data-ttu-id="0096e-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="0096e-103">FBadProp</span></span>

  
  
<span data-ttu-id="0096e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0096e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0096e-105">Valida uma propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="0096e-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0096e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0096e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0096e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="0096e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="0096e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0096e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0096e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0096e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0096e-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="0096e-110">Called by:</span></span>  <br/> |<span data-ttu-id="0096e-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="0096e-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="0096e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0096e-112">Parameters</span></span>

 <span data-ttu-id="0096e-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="0096e-113">_lpprop_</span></span>
  
> <span data-ttu-id="0096e-114">[in] Uma estrutura [SPropValue](spropvalue.md) que define a propriedade a ser validada.</span><span class="sxs-lookup"><span data-stu-id="0096e-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0096e-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0096e-115">Return value</span></span>

<span data-ttu-id="0096e-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="0096e-116">TRUE</span></span> 
  
> <span data-ttu-id="0096e-117">A propriedade especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="0096e-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="0096e-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="0096e-118">FALSE</span></span> 
  
> <span data-ttu-id="0096e-119">A propriedade especificada é válida.</span><span class="sxs-lookup"><span data-stu-id="0096e-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0096e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0096e-120">Remarks</span></span>

<span data-ttu-id="0096e-121">Um provedor de serviços pode chamar a função **FBadProp** por diversos motivos; por exemplo, para se preparar para uma chamada para o método [IMAPIProp::SetProps](imapiprop-setprops.md) configurando uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="0096e-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="0096e-122">**FBadProp** valida a propriedade especificada, dependendo do tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0096e-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="0096e-123">Por exemplo, se a propriedade é booliana, **FBadProp** garante que o respectivo valor seja TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="0096e-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="0096e-124">Quado a propriedade é binária, **FBadProp** verifica o ponteiro e o tamanho e garante que ela seja alocada corretamente.</span><span class="sxs-lookup"><span data-stu-id="0096e-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0096e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0096e-125">See also</span></span>



[<span data-ttu-id="0096e-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="0096e-126">FBadPropTag</span></span>](fbadproptag.md)

