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
# <a name="hrgetoneprop"></a><span data-ttu-id="2f97c-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="2f97c-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="2f97c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f97c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f97c-105">Recupera o valor de uma única propriedade de uma interface de propriedade, ou seja, uma interface derivada de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2f97c-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f97c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2f97c-106">Header file:</span></span>  <br/> |<span data-ttu-id="2f97c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2f97c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2f97c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2f97c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2f97c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2f97c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2f97c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2f97c-110">Called by:</span></span>  <br/> |<span data-ttu-id="2f97c-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="2f97c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="2f97c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f97c-112">Parameters</span></span>

 <span data-ttu-id="2f97c-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="2f97c-113">_pmp_</span></span>
  
> <span data-ttu-id="2f97c-114">[in] Ponteiro para a interface [IMAPIProp](imapipropiunknown.md) da qual o valor da propriedade deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="2f97c-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="2f97c-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="2f97c-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="2f97c-116">[in] Marca de propriedade da propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="2f97c-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="2f97c-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="2f97c-117">_ppprop_</span></span>
  
> <span data-ttu-id="2f97c-118">[out] Ponteiro para um ponteiro para a estrutura [SPropValue](spropvalue.md) retornada definindo o valor da propriedade recuperada.</span><span class="sxs-lookup"><span data-stu-id="2f97c-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2f97c-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2f97c-119">Return value</span></span>

<span data-ttu-id="2f97c-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2f97c-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2f97c-121">A propriedade solicitada não está disponível na interface especificada.</span><span class="sxs-lookup"><span data-stu-id="2f97c-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f97c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f97c-122">Remarks</span></span>

<span data-ttu-id="2f97c-123">Ao contrário [do método IMAPIProp::GetProps,](imapiprop-getprops.md) **a função HrGetOneProp** nunca retorna nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="2f97c-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="2f97c-124">Como recupera apenas uma propriedade, ela simplesmente é bem-sucedida ou falha.</span><span class="sxs-lookup"><span data-stu-id="2f97c-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="2f97c-125">Para recuperar várias propriedades, **GetProps** é mais rápido.</span><span class="sxs-lookup"><span data-stu-id="2f97c-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="2f97c-126">Você pode definir ou alterar uma única propriedade com a [função HrSetOneProp.](hrsetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="2f97c-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2f97c-127">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2f97c-127">MFCMAPI reference</span></span>

<span data-ttu-id="2f97c-128">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f97c-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2f97c-129">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2f97c-129">**File**</span></span>|<span data-ttu-id="2f97c-130">**Função**</span><span class="sxs-lookup"><span data-stu-id="2f97c-130">**Function**</span></span>|<span data-ttu-id="2f97c-131">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="2f97c-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f97c-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="2f97c-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2f97c-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="2f97c-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="2f97c-134">MFCMAPI usa o **método HrGetOneProp** para recuperar o tipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2f97c-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f97c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f97c-135">See also</span></span>



[<span data-ttu-id="2f97c-136">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="2f97c-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

