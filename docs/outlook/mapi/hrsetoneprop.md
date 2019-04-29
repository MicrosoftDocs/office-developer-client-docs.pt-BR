---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417655"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="e20c7-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="e20c7-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="e20c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e20c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e20c7-105">Define ou altera o valor de uma única propriedade em uma interface de propriedade, ou seja, uma interface derivada de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="e20c7-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e20c7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e20c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="e20c7-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e20c7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e20c7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e20c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e20c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e20c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e20c7-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e20c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="e20c7-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="e20c7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="e20c7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e20c7-112">Parameters</span></span>

 <span data-ttu-id="e20c7-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="e20c7-113">_pmp_</span></span>
  
> <span data-ttu-id="e20c7-114">no Ponteiro para uma interface [IMAPIProp](imapipropiunknown.md) na qual o valor da propriedade deve ser definido ou alterado.</span><span class="sxs-lookup"><span data-stu-id="e20c7-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="e20c7-115">_pProp_</span><span class="sxs-lookup"><span data-stu-id="e20c7-115">_pprop_</span></span>
  
> <span data-ttu-id="e20c7-116">no Ponteiro para a estrutura [SPropValue](spropvalue.md) que define o valor a ser definido na propriedade _PMP_ .</span><span class="sxs-lookup"><span data-stu-id="e20c7-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e20c7-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e20c7-117">Return value</span></span>

<span data-ttu-id="e20c7-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e20c7-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e20c7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e20c7-119">Remarks</span></span>

<span data-ttu-id="e20c7-120">Diferentemente do método [IMAPIProp::](imapiprop-setprops.md) SetProps, a função **HrSetOneProp** nunca retorna quaisquer avisos.</span><span class="sxs-lookup"><span data-stu-id="e20c7-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="e20c7-121">Como ela define apenas uma propriedade, ela simplesmente sucede ou falha.</span><span class="sxs-lookup"><span data-stu-id="e20c7-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="e20c7-122">Para definir ou alterar várias propriedades, \*\*\*\* SetProps é mais rápido.</span><span class="sxs-lookup"><span data-stu-id="e20c7-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="e20c7-123">Você pode recuperar uma única propriedade com a função [HrGetOneProp](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="e20c7-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

