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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416052"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="42907-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="42907-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="42907-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42907-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42907-105">Recupera o valor de uma única propriedade de uma interface de propriedade, ou seja, uma interface derivada de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="42907-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42907-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="42907-106">Header file:</span></span>  <br/> |<span data-ttu-id="42907-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="42907-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="42907-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="42907-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="42907-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="42907-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="42907-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="42907-110">Called by:</span></span>  <br/> |<span data-ttu-id="42907-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="42907-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="42907-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42907-112">Parameters</span></span>

 <span data-ttu-id="42907-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="42907-113">_pmp_</span></span>
  
> <span data-ttu-id="42907-114">no Ponteiro para a interface [IMAPIProp](imapipropiunknown.md) da qual o valor da propriedade deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="42907-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="42907-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="42907-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="42907-116">no Marca de propriedade da propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="42907-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="42907-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="42907-117">_ppprop_</span></span>
  
> <span data-ttu-id="42907-118">bota Ponteiro para um ponteiro para a estrutura [SPropValue](spropvalue.md) retornada que define o valor da propriedade recuperado.</span><span class="sxs-lookup"><span data-stu-id="42907-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42907-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="42907-119">Return value</span></span>

<span data-ttu-id="42907-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="42907-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="42907-121">A propriedade solicitada não está disponível na interface especificada.</span><span class="sxs-lookup"><span data-stu-id="42907-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42907-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="42907-122">Remarks</span></span>

<span data-ttu-id="42907-123">Diferentemente do método [IMAPIProp::](imapiprop-getprops.md) GetProps, a função **HrGetOneProp** nunca retorna qualquer aviso.</span><span class="sxs-lookup"><span data-stu-id="42907-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="42907-124">Como ele recupera apenas uma propriedade, ele simplesmente Obtém ou falha.</span><span class="sxs-lookup"><span data-stu-id="42907-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="42907-125">Para recuperar várias propriedades, getProps é mais rápido. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="42907-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="42907-126">Você pode definir ou alterar uma única propriedade com a função [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="42907-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="42907-127">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="42907-127">MFCMAPI reference</span></span>

<span data-ttu-id="42907-128">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="42907-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="42907-129">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="42907-129">**File**</span></span>|<span data-ttu-id="42907-130">**Função**</span><span class="sxs-lookup"><span data-stu-id="42907-130">**Function**</span></span>|<span data-ttu-id="42907-131">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="42907-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="42907-132">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="42907-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="42907-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="42907-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="42907-134">MFCMAPI usa o método **HrGetOneProp** para recuperar o tipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="42907-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42907-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="42907-135">See also</span></span>



[<span data-ttu-id="42907-136">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="42907-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

