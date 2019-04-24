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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349284"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="5089d-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="5089d-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="5089d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5089d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5089d-105">Retorna um ponteiro para a tabela de conteúdo do contêiner.</span><span class="sxs-lookup"><span data-stu-id="5089d-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5089d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5089d-106">Parameters</span></span>

 <span data-ttu-id="5089d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5089d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5089d-108">no Uma bitmask de sinalizadores que controla como a tabela de conteúdo é retornada.</span><span class="sxs-lookup"><span data-stu-id="5089d-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="5089d-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="5089d-109">The following flags can be set:</span></span>
    
<span data-ttu-id="5089d-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="5089d-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="5089d-111">A tabela de conteúdo associado do contêiner deve ser retornada em vez da tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="5089d-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="5089d-112">Este sinalizador é usado somente com pastas.</span><span class="sxs-lookup"><span data-stu-id="5089d-112">This flag is used only with folders.</span></span> <span data-ttu-id="5089d-113">As mensagens incluídas na tabela de conteúdo associado foram criadas com o sinalizador MAPI_ASSOCIATED definido na chamada para o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="5089d-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="5089d-114">Normalmente, os clientes usam a tabela de conteúdo associado para recuperar formulários, exibições e outras mensagens ocultas.</span><span class="sxs-lookup"><span data-stu-id="5089d-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="5089d-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="5089d-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="5089d-116">Permite o acesso aos direitos frightsFreeBusySimple e frightsFreeBusyDetailed no **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="5089d-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="5089d-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5089d-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5089d-118">\*\*\*\* Getcontenttable pode ser retornado com êxito, possivelmente antes de a tabela ser disponibilizada para o chamador.</span><span class="sxs-lookup"><span data-stu-id="5089d-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="5089d-119">Se a tabela não estiver disponível, fazer uma chamada de tabela subsequente poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="5089d-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="5089d-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5089d-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5089d-121">Solicita que as colunas que contêm dados de cadeia de caracteres sejam retornadas no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5089d-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="5089d-122">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres deverão ser retornadas no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5089d-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="5089d-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="5089d-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="5089d-124">Mostra os itens atualmente marcados como excluídos por software, ou seja, estão na fase de tempo de retenção de item excluído.</span><span class="sxs-lookup"><span data-stu-id="5089d-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="5089d-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5089d-125">_lppTable_</span></span>
  
> <span data-ttu-id="5089d-126">bota Um ponteiro para um ponteiro para a tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5089d-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5089d-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5089d-127">Return value</span></span>

<span data-ttu-id="5089d-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="5089d-128">S_OK</span></span> 
  
> <span data-ttu-id="5089d-129">A tabela de conteúdo foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="5089d-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="5089d-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5089d-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5089d-131">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="5089d-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="5089d-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5089d-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5089d-133">O contêiner não tem conteúdo e não pode fornecer uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5089d-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5089d-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="5089d-134">Remarks</span></span>

<span data-ttu-id="5089d-135">O método **IMAPIContainer::** getcontenttable retorna um ponteiro para a tabela de conteúdo de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="5089d-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="5089d-136">Uma tabela de conteúdo contém informações de resumo sobre objetos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="5089d-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="5089d-137">As tabelas de conteúdo têm conjuntos de colunas longos.</span><span class="sxs-lookup"><span data-stu-id="5089d-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="5089d-138">Para obter uma lista completa das colunas obrigatórias e opcionais nas tabelas de conteúdo, consulte [tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5089d-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="5089d-139">É possível que alguns contêineres não tenham conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5089d-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="5089d-140">Esses contêineres retornam MAPI_E_NO_SUPPORT de suas \*\*\*\* implementações de getcontenttable.</span><span class="sxs-lookup"><span data-stu-id="5089d-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5089d-141">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="5089d-141">Notes to implementers</span></span>

<span data-ttu-id="5089d-142">Se você oferecer suporte a uma tabela de conteúdo para seu contêiner, também deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5089d-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="5089d-143">Suporte a chamadas para o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5089d-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="5089d-144">Retornar **PR_CONTAINER_CONTENTS** em resposta a uma chamada para o contêiner do</span><span class="sxs-lookup"><span data-stu-id="5089d-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="5089d-145">[IMAPIProp::](imapiprop-getprops.md) GetProps e [IMAPIProp::](imapiprop-getproplist.md) getproplist métodos.</span><span class="sxs-lookup"><span data-stu-id="5089d-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="5089d-146">A implementação de um provedor de transporte remoto desse método deve retornar um ponteiro para uma interface imApitable [: IUnknown](imapitableiunknown.md) no parâmetro _ppTable_ passado para o método getcontenttable. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5089d-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="5089d-147">Se o seu provedor de transporte tiver uma tabela de conteúdo existente, será suficiente retornar um ponteiro para ela.</span><span class="sxs-lookup"><span data-stu-id="5089d-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="5089d-148">Caso contrário, esse método deve criar um novo objeto imApitable [: IUnknown](imapitableiunknown.md) , preencher a tabela com cabeçalhos de mensagem (se houver algum disponível) e retornar um ponteiro para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="5089d-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="5089d-149">O método [ITableData:: HrGetView](itabledata-hrgetview.md) é útil para gerar um valor de retorno e armazenar o ponteiro de tabela no parâmetro _ppTable_ .</span><span class="sxs-lookup"><span data-stu-id="5089d-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="5089d-150">A tabela de conteúdo deve suportar pelo menos as seguintes colunas de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5089d-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="5089d-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="5089d-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5089d-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="5089d-169">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5089d-169">Notes to callers</span></span>

<span data-ttu-id="5089d-170">As colunas da tabela de conteúdo binário e cadeia de caracteres podem ser truncadas.</span><span class="sxs-lookup"><span data-stu-id="5089d-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="5089d-171">Normalmente, os provedores retornam 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5089d-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="5089d-172">Como você não pode saber antecipadamente se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna for 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="5089d-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="5089d-173">Você sempre pode recuperar o valor completo de uma coluna truncada, se necessário, diretamente do objeto usando seu identificador de entrada para abri-lo e, em seguida, chamando o método **IMAPIProp::** GetProps.</span><span class="sxs-lookup"><span data-stu-id="5089d-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="5089d-174">Dependendo da implementação do provedor, as operações de classificação e restrições podem ser aplicadas a todas as cadeias de caracteres ou à versão truncada dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5089d-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5089d-175">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5089d-175">MFCMAPI reference</span></span>

<span data-ttu-id="5089d-176">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5089d-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5089d-177">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5089d-177">**File**</span></span>|<span data-ttu-id="5089d-178">**Função**</span><span class="sxs-lookup"><span data-stu-id="5089d-178">**Function**</span></span>|<span data-ttu-id="5089d-179">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="5089d-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5089d-180">ContentsTableDialog. cpp</span><span class="sxs-lookup"><span data-stu-id="5089d-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="5089d-181">CContentsTableDlg:: CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="5089d-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="5089d-182">A classe **CContentsTableDlg** usa \*\*\*\* getcontenttable para obter as entradas em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5089d-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5089d-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="5089d-183">See also</span></span>



[<span data-ttu-id="5089d-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="5089d-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="5089d-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="5089d-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="5089d-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="5089d-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="5089d-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5089d-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="5089d-188">Propriedade canônica PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="5089d-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="5089d-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5089d-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="5089d-190">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5089d-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

