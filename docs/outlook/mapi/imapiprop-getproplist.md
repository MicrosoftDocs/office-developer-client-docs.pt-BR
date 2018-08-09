---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0457007334ad8cc69dade3abd5859dd0d5f7af7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767144"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="a6fac-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="a6fac-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="a6fac-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6fac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6fac-105">Retorna as marcas de propriedade para todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="a6fac-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="a6fac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6fac-106">Parameters</span></span>

 <span data-ttu-id="a6fac-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6fac-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a6fac-108">[in] Uma bitmask dos sinalizadores que controla o formato de cadeias de caracteres nas marcas de propriedade retornados.</span><span class="sxs-lookup"><span data-stu-id="a6fac-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="a6fac-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="a6fac-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a6fac-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6fac-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a6fac-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6fac-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a6fac-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a6fac-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a6fac-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="a6fac-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="a6fac-114">[out] Um ponteiro para um ponteiro para a matriz de marca de propriedade que contém marcas para todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="a6fac-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6fac-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a6fac-115">Return value</span></span>

<span data-ttu-id="a6fac-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6fac-116">S_OK</span></span> 
  
> <span data-ttu-id="a6fac-117">Todas as marcas de propriedade foram retornadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a6fac-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="a6fac-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a6fac-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a6fac-119">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="a6fac-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6fac-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6fac-120">Remarks</span></span>

<span data-ttu-id="a6fac-121">O método **IMAPIProp::GetPropList** recupera a marca de propriedade para cada propriedade suportada atualmente por um objeto.</span><span class="sxs-lookup"><span data-stu-id="a6fac-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="a6fac-122">Se o objeto não oferece suporte atualmente todas as propriedades, **GetPropList** retorna uma matriz de marca de propriedade com o membro **cValues** definido como 0.</span><span class="sxs-lookup"><span data-stu-id="a6fac-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="a6fac-123">O escopo das propriedades retornado pela **GetPropList** varia de provedor.</span><span class="sxs-lookup"><span data-stu-id="a6fac-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="a6fac-124">Alguns provedores de serviços excluir essas propriedades para o qual o chamador não tem acesso.</span><span class="sxs-lookup"><span data-stu-id="a6fac-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="a6fac-125">Todos os provedores de retornam as propriedades do tipo **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="a6fac-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="a6fac-126">Se o objeto não oferece suporte a Unicode, **GetPropList** retorna MAPI_E_BAD_CHARWIDTH, mesmo se não houver nenhuma propriedade de cadeia de caracteres definida para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a6fac-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6fac-127">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="a6fac-127">Notes to implementers</span></span>

<span data-ttu-id="a6fac-128">Provedores de transporte remoto implementam **GetPropList** exatamente conforme especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="a6fac-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="a6fac-129">Não há nenhuma preocupações especiais.</span><span class="sxs-lookup"><span data-stu-id="a6fac-129">There are no special concerns.</span></span> <span data-ttu-id="a6fac-130">A implementação deve, obviamente, retornar a mesma lista de propriedades como suportados pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a6fac-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6fac-131">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a6fac-131">Notes to callers</span></span>

<span data-ttu-id="a6fac-132">Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de marca de propriedade apontada pela _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="a6fac-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a6fac-133">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a6fac-133">MFCMAPI reference</span></span>

<span data-ttu-id="a6fac-134">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6fac-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a6fac-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a6fac-135">**File**</span></span>|<span data-ttu-id="a6fac-136">**Function**</span><span class="sxs-lookup"><span data-stu-id="a6fac-136">**Function**</span></span>|<span data-ttu-id="a6fac-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a6fac-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a6fac-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a6fac-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a6fac-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="a6fac-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="a6fac-140">MFCMAPI usa o método **IMAPIProp::GetPropList** para obter uma lista de propriedades a serem passados para **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="a6fac-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6fac-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6fac-141">See also</span></span>



[<span data-ttu-id="a6fac-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a6fac-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="a6fac-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a6fac-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a6fac-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6fac-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="a6fac-145">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a6fac-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

