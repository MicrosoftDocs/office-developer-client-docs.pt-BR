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
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414785"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="f0dbc-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="f0dbc-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="f0dbc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0dbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0dbc-105">Retorna as marcas de propriedade de todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="f0dbc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0dbc-106">Parameters</span></span>

 <span data-ttu-id="f0dbc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0dbc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f0dbc-108">no Uma bitmask de sinalizadores que controla o formato das cadeias de caracteres nas marcas de propriedade retornadas.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="f0dbc-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f0dbc-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f0dbc-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0dbc-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f0dbc-111">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="f0dbc-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f0dbc-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="f0dbc-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="f0dbc-114">bota Um ponteiro para um ponteiro para a matriz de marca de propriedade que contém marcas para todas as propriedades do objeto.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0dbc-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f0dbc-115">Return value</span></span>

<span data-ttu-id="f0dbc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0dbc-116">S_OK</span></span> 
  
> <span data-ttu-id="f0dbc-117">Todas as marcas de propriedade foram retornadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="f0dbc-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f0dbc-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f0dbc-119">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0dbc-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0dbc-120">Remarks</span></span>

<span data-ttu-id="f0dbc-121">O método **IMAPIProp::** getproplist recupera a marca de propriedade para cada propriedade atualmente aceita por um objeto.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="f0dbc-122">Se o objeto não suportar nenhuma propriedade no momento, \*\*\*\* getproplist retornará uma matriz de marca de propriedade com o membro **cValues** definido como 0.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="f0dbc-123">O escopo de propriedades retornado por \*\*\*\* getproplist varia de provedor para provedor.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="f0dbc-124">Alguns provedores de serviços excluem as propriedades para as quais o chamador não tem acesso.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="f0dbc-125">Todos os provedores retornam propriedades do tipo **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="f0dbc-126">Se o objeto não oferecer suporte a Unicode \*\*\*\* , getproplist retornará MAPI_E_BAD_CHARWIDTH, mesmo se não houver propriedades de cadeia de caracteres definidas para o objeto.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f0dbc-127">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="f0dbc-127">Notes to implementers</span></span>

<span data-ttu-id="f0dbc-128">Os provedores de transporte \*\*\*\* remotos implementam getproplist exatamente como especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="f0dbc-129">Não há preocupações especiais.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-129">There are no special concerns.</span></span> <span data-ttu-id="f0dbc-130">A implementação deve, naturalmente, retornar a mesma lista de propriedades que é suportada pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f0dbc-131">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f0dbc-131">Notes to callers</span></span>

<span data-ttu-id="f0dbc-132">Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de marca de propriedade apontada por _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f0dbc-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f0dbc-133">MFCMAPI reference</span></span>

<span data-ttu-id="f0dbc-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f0dbc-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f0dbc-135">**File**</span></span>|<span data-ttu-id="f0dbc-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="f0dbc-136">**Function**</span></span>|<span data-ttu-id="f0dbc-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f0dbc-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0dbc-138">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f0dbc-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f0dbc-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="f0dbc-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="f0dbc-140">MFCMAPI usa o método **IMAPIProp::** getproplist para obter uma lista de propriedades a ser \*\*\*\* passada para GetProps.</span><span class="sxs-lookup"><span data-stu-id="f0dbc-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0dbc-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0dbc-141">See also</span></span>



[<span data-ttu-id="f0dbc-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f0dbc-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f0dbc-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f0dbc-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f0dbc-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0dbc-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="f0dbc-145">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f0dbc-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

