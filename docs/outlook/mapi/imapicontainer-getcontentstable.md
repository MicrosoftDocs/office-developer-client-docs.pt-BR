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
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431103"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="6c671-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="6c671-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="6c671-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c671-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c671-105">Retorna um ponteiro para a tabela de conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="6c671-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6c671-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c671-106">Parameters</span></span>

 <span data-ttu-id="6c671-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c671-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6c671-108">[in] Uma bitmask de sinalizadores que controla como o conteúdo da tabela é retornado.</span><span class="sxs-lookup"><span data-stu-id="6c671-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="6c671-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6c671-109">The following flags can be set:</span></span>
    
<span data-ttu-id="6c671-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="6c671-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="6c671-111">A tabela de conteúdo associada do contêiner deve ser retornada em vez da tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="6c671-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="6c671-112">Esse sinalizador é usado somente com pastas.</span><span class="sxs-lookup"><span data-stu-id="6c671-112">This flag is used only with folders.</span></span> <span data-ttu-id="6c671-113">As mensagens incluídas na tabela de conteúdo associada foram criadas com o sinalizador MAPI_ASSOCIATED definido na chamada para o método [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="6c671-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="6c671-114">Os clientes normalmente usam a tabela de conteúdo associada para recuperar formulários, exibições e outras mensagens ocultas.</span><span class="sxs-lookup"><span data-stu-id="6c671-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="6c671-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="6c671-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="6c671-116">Permite o acesso aos direitos deFreeBusySimple e PR_MEMBER_RIGHTS **.**</span><span class="sxs-lookup"><span data-stu-id="6c671-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="6c671-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6c671-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6c671-118">**GetContentsTable** pode retornar com êxito, possivelmente antes que a tabela seja disponibilizada para o chamador.</span><span class="sxs-lookup"><span data-stu-id="6c671-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="6c671-119">Se a tabela não estiver disponível, fazer uma chamada de tabela subsequente poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="6c671-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="6c671-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6c671-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6c671-121">Solicita que as colunas que contêm dados de cadeia de caracteres sejam retornadas no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c671-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="6c671-122">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres deverão ser retornadas no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6c671-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="6c671-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="6c671-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="6c671-124">Mostra itens que estão marcados como excluídos de forma suave, ou seja, eles estão na fase de tempo de retenção de itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="6c671-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="6c671-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6c671-125">_lppTable_</span></span>
  
> <span data-ttu-id="6c671-126">[out] Um ponteiro para um ponteiro para a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c671-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c671-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6c671-127">Return value</span></span>

<span data-ttu-id="6c671-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c671-128">S_OK</span></span> 
  
> <span data-ttu-id="6c671-129">A tabela de conteúdo foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6c671-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="6c671-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6c671-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6c671-131">O sinalizador MAPI_UNICODE padrão foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c671-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="6c671-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6c671-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6c671-133">O contêiner não tem conteúdo e não pode fornecer um índice de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c671-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c671-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c671-134">Remarks</span></span>

<span data-ttu-id="6c671-135">O **método IMAPIContainer::GetContentsTable** retorna um ponteiro para o índice de conteúdo de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="6c671-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="6c671-136">Uma tabela de conteúdo contém informações resumidas sobre objetos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="6c671-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="6c671-137">Tabelas de conteúdo têm conjuntos de colunas longos.</span><span class="sxs-lookup"><span data-stu-id="6c671-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="6c671-138">Para uma lista completa das colunas necessárias e opcionais em tabelas de conteúdo, consulte [Tabelas de Conteúdo.](contents-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6c671-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="6c671-139">É possível que alguns contêineres não tenham conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c671-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="6c671-140">Esses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="6c671-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6c671-141">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="6c671-141">Notes to implementers</span></span>

<span data-ttu-id="6c671-142">Se você tiver suporte para uma tabela de conteúdo para seu contêiner, também deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6c671-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="6c671-143">Suporte a chamadas para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6c671-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="6c671-144">Retornar **PR_CONTAINER_CONTENTS** em resposta a uma chamada para o contêiner</span><span class="sxs-lookup"><span data-stu-id="6c671-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="6c671-145">[Métodos IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="6c671-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="6c671-146">A implementação desse método de um provedor de transporte remoto deve retornar um ponteiro para uma [IMAPITable : interface IUnknown](imapitableiunknown.md) no parâmetro _ppTable_ passado para o **método GetContentsTable.**</span><span class="sxs-lookup"><span data-stu-id="6c671-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="6c671-147">Se o provedor de transporte tiver um índice de conteúdo existente, será suficiente retornar um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="6c671-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="6c671-148">Se não estiver, este método deverá criar um novo [IMAPITable : objeto IUnknown,](imapitableiunknown.md) preencher a tabela com os headers de mensagem (se algum estiver disponível) e retornar um ponteiro para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="6c671-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="6c671-149">O [método ITableData::HrGetView](itabledata-hrgetview.md) é útil para gerar um valor de retorno e armazenar o ponteiro da tabela no _parâmetro ppTable._</span><span class="sxs-lookup"><span data-stu-id="6c671-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="6c671-150">A tabela de conteúdo deve suportar pelo menos as seguintes colunas de propriedades:</span><span class="sxs-lookup"><span data-stu-id="6c671-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="6c671-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="6c671-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6c671-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="6c671-169">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6c671-169">Notes to callers</span></span>

<span data-ttu-id="6c671-170">As colunas da tabela de cadeia de caracteres e conteúdo binário podem ser truncadas.</span><span class="sxs-lookup"><span data-stu-id="6c671-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="6c671-171">Normalmente, os provedores retornam 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6c671-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="6c671-172">Como não é possível saber antecipadamente se uma tabela inclui colunas truncadas, suponha que uma coluna seja truncada se o tamanho da coluna for de 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="6c671-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="6c671-173">Você sempre pode recuperar o valor completo de uma coluna truncada, se necessário, diretamente do objeto usando seu identificador de entrada para abri-la e, em seguida, chamando o método **IMAPIProp::GetProps.**</span><span class="sxs-lookup"><span data-stu-id="6c671-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="6c671-174">Dependendo da implementação do provedor, as restrições e as operações de classificação podem ser aplicadas a toda uma cadeia de caracteres ou à versão truncada dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6c671-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6c671-175">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6c671-175">MFCMAPI reference</span></span>

<span data-ttu-id="6c671-176">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c671-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6c671-177">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6c671-177">**File**</span></span>|<span data-ttu-id="6c671-178">**Função**</span><span class="sxs-lookup"><span data-stu-id="6c671-178">**Function**</span></span>|<span data-ttu-id="6c671-179">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="6c671-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6c671-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="6c671-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="6c671-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="6c671-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="6c671-182">A **classe CContentsTableDlg** usa **GetContentsTable** para obter as entradas em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6c671-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c671-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c671-183">See also</span></span>



[<span data-ttu-id="6c671-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="6c671-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="6c671-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="6c671-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="6c671-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="6c671-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="6c671-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c671-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="6c671-188">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="6c671-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="6c671-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6c671-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="6c671-190">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="6c671-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

