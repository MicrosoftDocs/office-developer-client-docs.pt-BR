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
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767510"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="1592c-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="1592c-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="1592c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1592c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1592c-105">Fornece acesso à tabela de pasta de recebimento, uma tabela que inclui informações sobre todas as pastas de recebimento para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1592c-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="1592c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1592c-106">Parameters</span></span>

 <span data-ttu-id="1592c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1592c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1592c-108">[in] Uma bitmask dos sinalizadores que controles tabela acesso.</span><span class="sxs-lookup"><span data-stu-id="1592c-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="1592c-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1592c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="1592c-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1592c-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1592c-111">Permite que **GetReceiveFolderTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o chamador.</span><span class="sxs-lookup"><span data-stu-id="1592c-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="1592c-112">Se a tabela não estiver totalmente disponível, fazendo uma chamada de tabela subsequentes pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="1592c-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="1592c-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1592c-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1592c-114">As cadeias de caracteres retornadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1592c-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="1592c-115">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1592c-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1592c-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1592c-116">_lppTable_</span></span>
  
> <span data-ttu-id="1592c-117">[out] Um ponteiro para um ponteiro para a tabela de pasta de recebimento.</span><span class="sxs-lookup"><span data-stu-id="1592c-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1592c-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1592c-118">Return value</span></span>

<span data-ttu-id="1592c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1592c-119">S_OK</span></span> 
  
> <span data-ttu-id="1592c-120">A tabela de pasta de recebimento foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1592c-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1592c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1592c-121">Remarks</span></span>

<span data-ttu-id="1592c-122">O método **IMsgStore::GetReceiveFolderTable** fornece acesso a uma tabela que mostra que as configurações de propriedade para o armazenamento de mensagens todos recebem pastas.</span><span class="sxs-lookup"><span data-stu-id="1592c-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1592c-123">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="1592c-123">Notes to implementers</span></span>

<span data-ttu-id="1592c-124">Para obter uma lista das colunas obrigatórias em uma tabela de pasta de recebimento, consulte as [Tabelas de pasta de recebimento](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1592c-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="1592c-125">Implementar sua receber tabelas de pasta para oferecer suporte a restrições de propriedades de configuração na propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1592c-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="1592c-126">Este permite o acesso fácil a determinado receber pastas.</span><span class="sxs-lookup"><span data-stu-id="1592c-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1592c-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1592c-127">Notes to callers</span></span>

<span data-ttu-id="1592c-128">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="1592c-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="1592c-129">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="1592c-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1592c-130">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1592c-130">MFCMAPI reference</span></span>

<span data-ttu-id="1592c-131">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1592c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1592c-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1592c-132">**File**</span></span>|<span data-ttu-id="1592c-133">**Function**</span><span class="sxs-lookup"><span data-stu-id="1592c-133">**Function**</span></span>|<span data-ttu-id="1592c-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1592c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1592c-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1592c-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="1592c-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="1592c-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="1592c-137">MFCMAPI usa o método **IMsgStore::GetReceiveFolderTable** para obter a tabela de pasta de recebimento para exibir.</span><span class="sxs-lookup"><span data-stu-id="1592c-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1592c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1592c-138">See also</span></span>



[<span data-ttu-id="1592c-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1592c-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="1592c-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1592c-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1592c-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="1592c-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="1592c-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1592c-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="1592c-143">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1592c-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="1592c-144">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1592c-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

