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
ms.openlocfilehash: 31d2be027ef3b58fdd44e71c922677164d352feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569124"
---
# <a name="hrsetoneprop"></a><span data-ttu-id="fccb0-103">HrSetOneProp</span><span class="sxs-lookup"><span data-stu-id="fccb0-103">HrSetOneProp</span></span>

  
  
<span data-ttu-id="fccb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fccb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fccb0-105">Define ou altera o valor de uma única propriedade em uma interface de propriedade, ou seja, uma interface derivada [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="fccb0-105">Sets or changes the value of a single property on a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fccb0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fccb0-106">Header file:</span></span>  <br/> |<span data-ttu-id="fccb0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fccb0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fccb0-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="fccb0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fccb0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fccb0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fccb0-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="fccb0-110">Called by:</span></span>  <br/> |<span data-ttu-id="fccb0-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="fccb0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a><span data-ttu-id="fccb0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fccb0-112">Parameters</span></span>

 <span data-ttu-id="fccb0-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="fccb0-113">_pmp_</span></span>
  
> <span data-ttu-id="fccb0-114">[in] Ponteiro para uma interface de [IMAPIProp](imapipropiunknown.md) em que o valor da propriedade deve ser definida ou alterada.</span><span class="sxs-lookup"><span data-stu-id="fccb0-114">[in] Pointer to an [IMAPIProp](imapipropiunknown.md) interface on which the property value is to be set or changed.</span></span> 
    
 <span data-ttu-id="fccb0-115">_pprop_</span><span class="sxs-lookup"><span data-stu-id="fccb0-115">_pprop_</span></span>
  
> <span data-ttu-id="fccb0-116">[in] Ponteiro para a estrutura de [SPropValue](spropvalue.md) definindo o valor a ser definido na propriedade _pmp_ .</span><span class="sxs-lookup"><span data-stu-id="fccb0-116">[in] Pointer to the [SPropValue](spropvalue.md) structure defining the value to be set on the  _pmp_ property.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fccb0-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fccb0-117">Return value</span></span>

<span data-ttu-id="fccb0-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fccb0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fccb0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fccb0-119">Remarks</span></span>

<span data-ttu-id="fccb0-120">Ao contrário do método [IMAPIProp::SetProps](imapiprop-setprops.md) , a função **HrSetOneProp** nunca retorna todos os avisos.</span><span class="sxs-lookup"><span data-stu-id="fccb0-120">Unlike the [IMAPIProp::SetProps](imapiprop-setprops.md) method, the **HrSetOneProp** function never returns any warnings.</span></span> <span data-ttu-id="fccb0-121">Porque ele define apenas uma propriedade, ele simplesmente for bem-sucedido ou falha.</span><span class="sxs-lookup"><span data-stu-id="fccb0-121">Because it sets only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="fccb0-122">Para definir ou alterar várias propriedades, **SetProps** é mais rápido.</span><span class="sxs-lookup"><span data-stu-id="fccb0-122">For setting or changing multiple properties, **SetProps** is faster.</span></span> 
  
<span data-ttu-id="fccb0-123">É possível recuperar uma única propriedade com a função [HrGetOneProp](hrgetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="fccb0-123">You can retrieve a single property with the [HrGetOneProp](hrgetoneprop.md) function.</span></span> 
  

