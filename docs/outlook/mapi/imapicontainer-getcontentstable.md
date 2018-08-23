---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9fb8919287420038b5c9165bb14b7d33d1ad2fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578861"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="d9e44-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="d9e44-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="d9e44-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9e44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9e44-105">Retorna um ponteiro para a tabela de conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d9e44-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d9e44-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9e44-106">Parameters</span></span>

 <span data-ttu-id="d9e44-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9e44-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d9e44-108">[in] Uma bitmask dos sinalizadores que controla como a tabela de conteúdo é retornada.</span><span class="sxs-lookup"><span data-stu-id="d9e44-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="d9e44-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d9e44-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d9e44-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="d9e44-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="d9e44-111">Tabela de conteúdo associado do contêiner deve ser retornada no lugar do índice de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="d9e44-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="d9e44-112">Esse sinalizador é usado somente com as pastas.</span><span class="sxs-lookup"><span data-stu-id="d9e44-112">This flag is used only with folders.</span></span> <span data-ttu-id="d9e44-113">As mensagens que estão incluídas na tabela de conteúdo associado foram criadas com o sinalizador MAPI_ASSOCIATED definido na chamada para o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e44-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="d9e44-114">Clientes normalmente usam a tabela de conteúdo associado para recuperar a formulários, exibições e outras mensagens ocultas.</span><span class="sxs-lookup"><span data-stu-id="d9e44-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="d9e44-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="d9e44-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="d9e44-116">Permite o acesso aos direitos de frightsFreeBusySimple e frightsFreeBusyDetailed em **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="d9e44-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="d9e44-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d9e44-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d9e44-118">**GetContentsTable** pode retornar com êxito, possivelmente antes que a tabela é disponibilizada para o chamador.</span><span class="sxs-lookup"><span data-stu-id="d9e44-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="d9e44-119">Se a tabela não estiver disponível, fazendo uma chamada de tabela subsequentes pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="d9e44-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="d9e44-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9e44-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d9e44-121">Solicitações que as colunas que contêm dados de cadeia de caracteres a ser retornado no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9e44-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="d9e44-122">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem ser retornadas no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9e44-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="d9e44-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="d9e44-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="d9e44-124">Mostra os itens que estão marcados como suaves excluídos — ou seja, eles estão na retenção de item excluído fase de tempo.</span><span class="sxs-lookup"><span data-stu-id="d9e44-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="d9e44-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d9e44-125">_lppTable_</span></span>
  
> <span data-ttu-id="d9e44-126">[out] Um ponteiro para um ponteiro para a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9e44-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9e44-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d9e44-127">Return value</span></span>

<span data-ttu-id="d9e44-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9e44-128">S_OK</span></span> 
  
> <span data-ttu-id="d9e44-129">A tabela de conteúdo foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d9e44-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="d9e44-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d9e44-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d9e44-131">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9e44-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="d9e44-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d9e44-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d9e44-133">O contêiner não tiver conteúdo e não pode fornecer uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9e44-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9e44-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9e44-134">Remarks</span></span>

<span data-ttu-id="d9e44-135">O método **IMAPIContainer::GetContentsTable** retorna um ponteiro para o índice de conteúdo de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="d9e44-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="d9e44-136">Uma tabela de conteúdo contém informações de resumo sobre objetos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="d9e44-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="d9e44-137">Tabelas de conteúdo têm conjuntos de coluna longos.</span><span class="sxs-lookup"><span data-stu-id="d9e44-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="d9e44-138">Para obter uma lista completa das colunas obrigatórios e opcionais nas tabelas de conteúdo, consulte [As tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d9e44-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="d9e44-139">É possível que alguns contêineres ter nenhum conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9e44-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="d9e44-140">Desses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="d9e44-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d9e44-141">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="d9e44-141">Notes to implementers</span></span>

<span data-ttu-id="d9e44-142">Caso você ofereça suporte a uma tabela de conteúdo para seu contêiner, você deve também faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d9e44-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="d9e44-143">Suporte a chamadas para o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9e44-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d9e44-144">Retornar **PR_CONTAINER_CONTENTS** em resposta a uma chamada para o contêiner</span><span class="sxs-lookup"><span data-stu-id="d9e44-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="d9e44-145">Métodos [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e44-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="d9e44-146">Implementação de um provedor de transporte remoto deste método deve retornar um ponteiro para uma [IMAPITable: IUnknown](imapitableiunknown.md) interface no parâmetro _ppTable_ passado para o método **GetContentsTable** .</span><span class="sxs-lookup"><span data-stu-id="d9e44-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="d9e44-147">Se o seu provedor de transporte tem uma tabela de conteúdo existente, é suficiente para retornar um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="d9e44-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="d9e44-148">Se não, esse método deve criar um novo [IMAPITable: IUnknown](imapitableiunknown.md) do objeto, preenchem a tabela com cabeçalhos de mensagem (caso haja algum disponível) e retornar um ponteiro para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="d9e44-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="d9e44-149">O método [ITableData::HrGetView](itabledata-hrgetview.md) é útil para gerar um valor de retorno e armazenar o ponteiro de tabela no parâmetro _ppTable_ .</span><span class="sxs-lookup"><span data-stu-id="d9e44-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="d9e44-150">A tabela de conteúdo deve suportar pelo menos as seguintes colunas de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d9e44-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="d9e44-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="d9e44-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d9e44-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d9e44-169">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d9e44-169">Notes to callers</span></span>

<span data-ttu-id="d9e44-170">Cadeia de caracteres e binário colunas da tabela de conteúdo podem ser truncadas.</span><span class="sxs-lookup"><span data-stu-id="d9e44-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="d9e44-171">Normalmente, provedores retornam 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9e44-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="d9e44-172">Porque você não pode saber com antecedência se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna é 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="d9e44-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="d9e44-173">Você sempre pode recuperar o valor completo de uma coluna truncado, se necessário, diretamente do objeto utilizando seu identificador de entrada para abri-lo e, em seguida, chamando o método **IMAPIProp::GetProps** .</span><span class="sxs-lookup"><span data-stu-id="d9e44-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="d9e44-174">Dependendo da implementação do provedor, restrições e operações de classificação podem aplicar a todas de uma cadeia de caracteres ou para a versão truncada da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9e44-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9e44-175">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d9e44-175">MFCMAPI reference</span></span>

<span data-ttu-id="d9e44-176">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9e44-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9e44-177">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d9e44-177">**File**</span></span>|<span data-ttu-id="d9e44-178">**Function**</span><span class="sxs-lookup"><span data-stu-id="d9e44-178">**Function**</span></span>|<span data-ttu-id="d9e44-179">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d9e44-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9e44-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="d9e44-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="d9e44-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="d9e44-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="d9e44-182">A classe **CContentsTableDlg** usa **GetContentsTable** para obter as entradas em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d9e44-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9e44-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9e44-183">See also</span></span>



[<span data-ttu-id="d9e44-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="d9e44-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="d9e44-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d9e44-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d9e44-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="d9e44-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="d9e44-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9e44-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="d9e44-188">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="d9e44-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="d9e44-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d9e44-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="d9e44-190">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d9e44-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

