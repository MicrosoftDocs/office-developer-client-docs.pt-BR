---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6b64653aa87ff7ac983409978a69f59148251d7d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583411"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="aa97a-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="aa97a-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="aa97a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa97a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa97a-105">Retorna o identificador de entrada do objeto que fornece a identidade principal para a sessão.</span><span class="sxs-lookup"><span data-stu-id="aa97a-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="aa97a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa97a-106">Parameters</span></span>

 <span data-ttu-id="aa97a-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="aa97a-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="aa97a-108">[out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="aa97a-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="aa97a-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="aa97a-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="aa97a-110">[out] Um ponteiro para um ponteiro para o identificador de entrada do objeto que fornece a identidade principal.</span><span class="sxs-lookup"><span data-stu-id="aa97a-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa97a-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aa97a-111">Return value</span></span>

<span data-ttu-id="aa97a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa97a-112">S_OK</span></span> 
  
> <span data-ttu-id="aa97a-113">A identidade principal foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="aa97a-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="aa97a-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="aa97a-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="aa97a-115">A chamada foi bem-sucedida, mas não há nenhuma identidade primária para a sessão.</span><span class="sxs-lookup"><span data-stu-id="aa97a-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="aa97a-116">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="aa97a-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="aa97a-117">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="aa97a-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="aa97a-118">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="aa97a-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa97a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa97a-119">Remarks</span></span>

<span data-ttu-id="aa97a-120">O método **IMAPISession::QueryIdentity** recupera a identidade principal para a sessão atual e retorna o valor através do parâmetro _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="aa97a-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="aa97a-121">A identidade principal é um objeto, normalmente um usuário de mensagens, que represente o usuário de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="aa97a-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="aa97a-122">_lppEntryID_ retorna a identidade principal para um objeto [IMailUser](imailuserimapiprop.md) , que também é armazenado à propriedade [PidTagEntryID](pidtagentryid-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="aa97a-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="aa97a-123">Você pode usar o valor retornado nos _lppEntryID_ para abrir um objeto **IMailUser** usando [IMAPISession::OpenEntry](imapisession-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="aa97a-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="aa97a-124">Embora muitos provedores de serviço em vários serviços de mensagem podem fornecer a identidade principal para uma sessão, MAPI designa um provedor de serviços único.</span><span class="sxs-lookup"><span data-stu-id="aa97a-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="aa97a-125">O provedor de serviço que fornece a identidade principal define os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="aa97a-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="aa97a-126">O sinalizador STATUS_PRIMARY_IDENTITY na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa97a-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="aa97a-127">A propriedade **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa97a-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="aa97a-128">A propriedade **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa97a-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="aa97a-129">A propriedade **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aa97a-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="aa97a-130">Se o provedor de serviço que fornece a identidade principal pertencer a um serviço de mensagem, os outros provedores de serviço no serviço de mensagem também definir as propriedades PR_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="aa97a-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="aa97a-131">Essas propriedades são publicadas na tabela de status da sessão.</span><span class="sxs-lookup"><span data-stu-id="aa97a-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="aa97a-132">Se possível, **QueryIdentity** retornará o valor da propriedade **PR_IDENTITY_ENTRYID** da linha status marcada com STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="aa97a-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="aa97a-133">Se a propriedade **PR_IDENTITY_ENTRYID** estiver falta da linha principal de identidade, **QueryIdentity** retorna um identificador de entrada únicos criado com outras informações a partir dessa linha.</span><span class="sxs-lookup"><span data-stu-id="aa97a-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="aa97a-134">Se o sinalizador STATUS_PRIMARY_IDENTITY estiver faltando em todas as colunas **PR_RESOURCE_FLAG** na tabela de status, **QueryIdentity** retorna o primeiro identificador de entrada que encontrar.</span><span class="sxs-lookup"><span data-stu-id="aa97a-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="aa97a-135">Quando não houver nenhum identificador de entrada apropriada para retornar, **QueryIdentity** tiver êxito com o aviso MAPI_W_NO_SERVICE e aponta _lppEntryID_ para um identificador de entrada codificadas.</span><span class="sxs-lookup"><span data-stu-id="aa97a-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aa97a-136">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="aa97a-136">Notes to callers</span></span>

<span data-ttu-id="aa97a-137">Você pode chamar o método [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para atribuir a tarefa de fornecer a identidade de principal da sessão de um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="aa97a-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="aa97a-138">Outra maneira de recuperar a identidade principal é pesquisando a tabela de status da linha com as colunas **PR_RESOURCE_FLAGS** definidas como STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="aa97a-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="aa97a-139">Para obter mais informações sobre essa maneira alternativa de recuperar informações de identidade, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aa97a-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="aa97a-140">Quando tiver terminado de usar o identificador de entrada para a identidade principal retornada pela **QueryIdentity**, libere seu memória chamando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="aa97a-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="aa97a-141">Para obter mais informações sobre identidade em geral, consulte [Identidade primária de MAPI](mapi-primary-identity.md).</span><span class="sxs-lookup"><span data-stu-id="aa97a-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="aa97a-142">Para obter mais informações sobre como recuperar a identidade de sessão MAPI, consulte [Recuperando primário e o provedor de identidade](retrieving-primary-and-provider-identity.md).</span><span class="sxs-lookup"><span data-stu-id="aa97a-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aa97a-143">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aa97a-143">MFCMAPI reference</span></span>

<span data-ttu-id="aa97a-144">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa97a-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aa97a-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="aa97a-145">**File**</span></span>|<span data-ttu-id="aa97a-146">**Function**</span><span class="sxs-lookup"><span data-stu-id="aa97a-146">**Function**</span></span>|<span data-ttu-id="aa97a-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="aa97a-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa97a-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aa97a-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="aa97a-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="aa97a-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="aa97a-150">MFCMAPI usa o método **IMAPISession::QueryIdentity** para abrir a entrada do catálogo de endereços para a identidade principal da sessão.</span><span class="sxs-lookup"><span data-stu-id="aa97a-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa97a-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa97a-151">See also</span></span>



[<span data-ttu-id="aa97a-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="aa97a-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="aa97a-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="aa97a-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="aa97a-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="aa97a-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="aa97a-155">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa97a-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="aa97a-156">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="aa97a-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="aa97a-157">Identidade primária de MAPI</span><span class="sxs-lookup"><span data-stu-id="aa97a-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="aa97a-158">Recuperar identidade principal e do provedor</span><span class="sxs-lookup"><span data-stu-id="aa97a-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="aa97a-159">Usar macros para lidar com erros</span><span class="sxs-lookup"><span data-stu-id="aa97a-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="aa97a-160">Tabela de status e objetos de status</span><span class="sxs-lookup"><span data-stu-id="aa97a-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

