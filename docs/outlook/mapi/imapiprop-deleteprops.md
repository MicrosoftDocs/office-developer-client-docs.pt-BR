---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a0d86b9b0342beea6b33db0219cb5889d2e63f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592070"
---
# <a name="imapipropdeleteprops"></a><span data-ttu-id="73d22-103">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="73d22-103">IMAPIProp::DeleteProps</span></span>

  
  
<span data-ttu-id="73d22-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73d22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73d22-105">Exclui uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="73d22-105">Deletes one or more properties from an object.</span></span> 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="73d22-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="73d22-106">Parameters</span></span>

 <span data-ttu-id="73d22-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="73d22-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="73d22-108">[in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="73d22-108">[in] A pointer to an array of property tags that indicate the properties to delete.</span></span> <span data-ttu-id="73d22-109">O membro **cValues** da estrutura [SPropTagArray](sproptagarray.md) apontado pela _lpPropTagArray_ não deve ser zero e o parâmetro _lpPropTagArray_ em si não deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="73d22-109">The **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpPropTagArray_ must not be zero, and the  _lpPropTagArray_ parameter itself must not be NULL.</span></span> 
    
 <span data-ttu-id="73d22-110">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="73d22-110">_lppProblems_</span></span>
  
> <span data-ttu-id="73d22-111">[além, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; Caso contrário, NULL, que indica que não há nenhuma necessidade de informações de erro.</span><span class="sxs-lookup"><span data-stu-id="73d22-111">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates that there is no need for error information.</span></span> <span data-ttu-id="73d22-112">Se _lppProblems_ for um ponteiro válido na entrada, **DeleteProps** retorna informações detalhadas sobre erros ao excluir uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="73d22-112">If  _lppProblems_ is a valid pointer on input, **DeleteProps** returns detailed information about errors in deleting one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="73d22-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="73d22-113">Return value</span></span>

<span data-ttu-id="73d22-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="73d22-114">S_OK</span></span> 
  
> <span data-ttu-id="73d22-115">Propriedades foram excluídas com êxito.</span><span class="sxs-lookup"><span data-stu-id="73d22-115">Properties were successfully deleted.</span></span>
    
<span data-ttu-id="73d22-116">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="73d22-116">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="73d22-117">O chamador não tem permissões suficientes para excluir as propriedades.</span><span class="sxs-lookup"><span data-stu-id="73d22-117">The caller has insufficient permissions to delete properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73d22-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="73d22-118">Remarks</span></span>

<span data-ttu-id="73d22-119">O método **IMAPIProp::DeleteProps** remove uma ou mais propriedades do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="73d22-119">The **IMAPIProp::DeleteProps** method removes one or more properties from the current object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73d22-120">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="73d22-120">Notes to implementers</span></span>

<span data-ttu-id="73d22-121">Você não precisará permitir propriedades a ser excluído de todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="73d22-121">You do not have to allow properties to be deleted from all objects.</span></span> <span data-ttu-id="73d22-122">Se o objeto não é modificável, retorne MAPI_E_NO_ACCESS do método **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="73d22-122">If the object is not modifiable, return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="73d22-123">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="73d22-123">Notes to callers</span></span>

<span data-ttu-id="73d22-124">Você não precisará definir o tipo de propriedade para cada marca de propriedade da matriz de marca de propriedade apontado pelo parâmetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="73d22-124">You do not have to set the property type for each property tag in the property tag array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="73d22-125">Tipos de propriedade serão ignorados; somente os identificadores de propriedade são usados.</span><span class="sxs-lookup"><span data-stu-id="73d22-125">Property types are ignored; only the property identifiers are used.</span></span> 
  
<span data-ttu-id="73d22-126">Lembre-se de que alguns objetos não permita modificação e que esses objetos retornam MAPI_E_NO_ACCESS do método **DeleteProps** .</span><span class="sxs-lookup"><span data-stu-id="73d22-126">Be aware that some objects do not allow modification and that these objects return MAPI_E_NO_ACCESS from the **DeleteProps** method.</span></span> <span data-ttu-id="73d22-127">Permitir que outros objetos, algumas propriedades a ser excluído, mas não para outras.</span><span class="sxs-lookup"><span data-stu-id="73d22-127">Other objects allow some properties to be deleted, but not others.</span></span> <span data-ttu-id="73d22-128">Quando há um problema ao excluir apenas algumas das propriedades, **DeleteProps** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="73d22-128">When there is a problem deleting only some of the properties, **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="73d22-129">Se você tiver passado um ponteiro válido no parâmetro _lppProblems_ , **DeleteProps** definirá o ponteiro em uma estrutura de **SPropProblemArray** que contém informações detalhadas sobre os problemas com cada propriedade.</span><span class="sxs-lookup"><span data-stu-id="73d22-129">If you have passed a valid pointer in the  _lppProblems_ parameter, **DeleteProps** will set the pointer to an **SPropProblemArray** structure that contains detailed information about the problems with each property.</span></span> <span data-ttu-id="73d22-130">Por exemplo, se você estiver excluindo todas as propriedades de uma mensagem e há um problema com um ou mais dos seus respectivos anexos, a estrutura de **SPropProblemArray** irá conter uma entrada para o **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) propriedade.</span><span class="sxs-lookup"><span data-stu-id="73d22-130">For example, if you are deleting all of the properties of a message and there is a problem with one or more of its attachments, the **SPropProblemArray** structure will contain an entry for the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="73d22-131">A estrutura apontada pela _lppProblems_ só será válida se **DeleteProps** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="73d22-131">The structure pointed to by  _lppProblems_ is only valid if **DeleteProps** returns S_OK.</span></span> <span data-ttu-id="73d22-132">Se **DeleteProps** retornará um erro, não tente usar a estrutura **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="73d22-132">If **DeleteProps** returns an error, do not attempt to use the **SPropProblemArray** structure.</span></span> <span data-ttu-id="73d22-133">Em vez disso, chame o método do objeto [IMAPIProp::GetLastError](imapiprop-getlasterror.md) para obter mais informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="73d22-133">Instead, call the object's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to obtain more information about the error.</span></span> 
  
<span data-ttu-id="73d22-134">Libere a estrutura de **SPropProblemArray** retornada ao chamar a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="73d22-134">Free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="73d22-135">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="73d22-135">MFCMAPI reference</span></span>

<span data-ttu-id="73d22-136">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="73d22-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="73d22-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="73d22-137">**File**</span></span>|<span data-ttu-id="73d22-138">**Function**</span><span class="sxs-lookup"><span data-stu-id="73d22-138">**Function**</span></span>|<span data-ttu-id="73d22-139">**Comment**</span><span class="sxs-lookup"><span data-stu-id="73d22-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73d22-140">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="73d22-140">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="73d22-141">DeleteProperty</span><span class="sxs-lookup"><span data-stu-id="73d22-141">DeleteProperty</span></span>  <br/> |<span data-ttu-id="73d22-142">MFCMAPI usa o método **IMAPIProp::DeleteProps** para excluir uma propriedade de um objeto.</span><span class="sxs-lookup"><span data-stu-id="73d22-142">MFCMAPI uses the **IMAPIProp::DeleteProps** method to delete a property from an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73d22-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="73d22-143">See also</span></span>



[<span data-ttu-id="73d22-144">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="73d22-144">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="73d22-145">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="73d22-145">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="73d22-146">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="73d22-146">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="73d22-147">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="73d22-147">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="73d22-148">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="73d22-148">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="73d22-149">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="73d22-149">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="73d22-150">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73d22-150">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="73d22-151">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="73d22-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

