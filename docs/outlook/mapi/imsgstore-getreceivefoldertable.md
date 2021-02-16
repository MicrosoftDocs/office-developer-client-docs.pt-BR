---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421351"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="ac8f8-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="ac8f8-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="ac8f8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac8f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac8f8-105">Fornece acesso à tabela de pastas de recebimento, uma tabela que inclui informações sobre todas as pastas de recebimento para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="ac8f8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac8f8-106">Parameters</span></span>

 <span data-ttu-id="ac8f8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac8f8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ac8f8-108">[in] Uma máscara de bits de sinalizadores que controla o acesso à tabela.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="ac8f8-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ac8f8-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ac8f8-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ac8f8-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ac8f8-111">Permite que **GetReceiveFolderTable** retorne com êxito, possivelmente antes que a tabela fique totalmente disponível para o chamador.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="ac8f8-112">Se a tabela não estiver totalmente disponível, fazer uma chamada de tabela subsequente poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="ac8f8-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac8f8-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ac8f8-114">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="ac8f8-115">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ac8f8-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ac8f8-116">_lppTable_</span></span>
  
> <span data-ttu-id="ac8f8-117">[out] Um ponteiro para um ponteiro para a tabela de pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac8f8-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ac8f8-118">Return value</span></span>

<span data-ttu-id="ac8f8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac8f8-119">S_OK</span></span> 
  
> <span data-ttu-id="ac8f8-120">A tabela de pasta de recebimento foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac8f8-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac8f8-121">Remarks</span></span>

<span data-ttu-id="ac8f8-122">O **método IMsgStore::GetReceiveFolderTable** fornece acesso a uma tabela que mostra as configurações de propriedade para todas as pastas de recebimento do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ac8f8-123">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="ac8f8-123">Notes to implementers</span></span>

<span data-ttu-id="ac8f8-124">Para uma lista de colunas necessárias em uma tabela de pasta de recebimento, consulte [Receive Folder Tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ac8f8-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="ac8f8-125">Implemente suas tabelas de pasta de recebimento para dar suporte à definição de restrições de propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) propriedade.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="ac8f8-126">Isso permite acesso fácil a pastas de recebimento específicas.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac8f8-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ac8f8-127">Notes to callers</span></span>

<span data-ttu-id="ac8f8-128">A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="ac8f8-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="ac8f8-129">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="ac8f8-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac8f8-130">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ac8f8-130">MFCMAPI reference</span></span>

<span data-ttu-id="ac8f8-131">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac8f8-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ac8f8-132">**File**</span></span>|<span data-ttu-id="ac8f8-133">**Função**</span><span class="sxs-lookup"><span data-stu-id="ac8f8-133">**Function**</span></span>|<span data-ttu-id="ac8f8-134">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ac8f8-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac8f8-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ac8f8-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="ac8f8-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="ac8f8-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="ac8f8-137">MFCMAPI usa o **método IMsgStore::GetReceiveFolderTable** para obter a tabela de pasta de recebimento a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="ac8f8-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac8f8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac8f8-138">See also</span></span>



[<span data-ttu-id="ac8f8-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ac8f8-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="ac8f8-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ac8f8-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ac8f8-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ac8f8-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="ac8f8-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="ac8f8-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="ac8f8-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac8f8-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="ac8f8-144">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ac8f8-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

