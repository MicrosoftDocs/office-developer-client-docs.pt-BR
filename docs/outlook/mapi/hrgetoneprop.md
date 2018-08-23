---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 99b63e7b0b31a603bf372b1d52e83af39784b628
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564154"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="36cdc-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="36cdc-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="36cdc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36cdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36cdc-105">Recupera o valor de uma única propriedade de uma interface de propriedade, ou seja, uma interface derivada [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="36cdc-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36cdc-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="36cdc-106">Header file:</span></span>  <br/> |<span data-ttu-id="36cdc-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="36cdc-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="36cdc-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="36cdc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36cdc-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36cdc-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36cdc-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="36cdc-110">Called by:</span></span>  <br/> |<span data-ttu-id="36cdc-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="36cdc-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="36cdc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36cdc-112">Parameters</span></span>

 <span data-ttu-id="36cdc-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="36cdc-113">_pmp_</span></span>
  
> <span data-ttu-id="36cdc-114">[in] Ponteiro para a interface de [IMAPIProp](imapipropiunknown.md) do qual o valor da propriedade deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="36cdc-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="36cdc-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="36cdc-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="36cdc-116">[in] Marca de propriedade da propriedade a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="36cdc-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="36cdc-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="36cdc-117">_ppprop_</span></span>
  
> <span data-ttu-id="36cdc-118">[out] Ponteiro para um ponteiro para a estrutura [SPropValue](spropvalue.md) retornada, definindo o valor da propriedade recuperadas.</span><span class="sxs-lookup"><span data-stu-id="36cdc-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36cdc-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="36cdc-119">Return value</span></span>

<span data-ttu-id="36cdc-120">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="36cdc-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="36cdc-121">A propriedade solicitada não está disponível da interface especificada.</span><span class="sxs-lookup"><span data-stu-id="36cdc-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36cdc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="36cdc-122">Remarks</span></span>

<span data-ttu-id="36cdc-123">Ao contrário do método [IMAPIProp::GetProps](imapiprop-getprops.md) , a função **HrGetOneProp** nunca retorna qualquer aviso.</span><span class="sxs-lookup"><span data-stu-id="36cdc-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="36cdc-124">Porque ele recupera apenas uma propriedade, ele simplesmente for bem-sucedido ou falha.</span><span class="sxs-lookup"><span data-stu-id="36cdc-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="36cdc-125">Para recuperar as várias propriedades, **GetProps** é mais rápido.</span><span class="sxs-lookup"><span data-stu-id="36cdc-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="36cdc-126">Você pode definir ou alterar uma única propriedade com a função [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="36cdc-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36cdc-127">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36cdc-127">MFCMAPI reference</span></span>

<span data-ttu-id="36cdc-128">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="36cdc-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36cdc-129">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="36cdc-129">**File**</span></span>|<span data-ttu-id="36cdc-130">**Function**</span><span class="sxs-lookup"><span data-stu-id="36cdc-130">**Function**</span></span>|<span data-ttu-id="36cdc-131">**Comment**</span><span class="sxs-lookup"><span data-stu-id="36cdc-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36cdc-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="36cdc-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="36cdc-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="36cdc-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="36cdc-134">MFCMAPI usa o método **HrGetOneProp** para recuperar o tipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="36cdc-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36cdc-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="36cdc-135">See also</span></span>



[<span data-ttu-id="36cdc-136">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="36cdc-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

