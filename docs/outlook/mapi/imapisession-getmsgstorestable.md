---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428134"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="6acdf-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="6acdf-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="6acdf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6acdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6acdf-105">Fornece acesso à tabela do armazenamento de mensagens que contém informações sobre todos os armazenamentos de mensagens no perfil de sessão.</span><span class="sxs-lookup"><span data-stu-id="6acdf-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6acdf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6acdf-106">Parameters</span></span>

 <span data-ttu-id="6acdf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6acdf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6acdf-108">[in] Uma bitmask de sinalizadores que determina o formato para colunas que são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6acdf-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="6acdf-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6acdf-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6acdf-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6acdf-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6acdf-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6acdf-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6acdf-112">Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6acdf-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="6acdf-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6acdf-113">_lppTable_</span></span>
  
> <span data-ttu-id="6acdf-114">[out] Um ponteiro para um ponteiro para a tabela do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6acdf-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6acdf-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6acdf-115">Return value</span></span>

<span data-ttu-id="6acdf-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6acdf-116">S_OK</span></span> 
  
> <span data-ttu-id="6acdf-117">A tabela foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6acdf-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="6acdf-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6acdf-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6acdf-119">O MAPI_UNICODE sinalizador foi definido e a sessão não dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="6acdf-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6acdf-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6acdf-120">Remarks</span></span>

<span data-ttu-id="6acdf-121">O método **IMAPISession::GetMsgStoresTable** recupera um ponteiro para a tabela de armazenamento de mensagens, uma tabela mantida por MAPI que contém informações sobre cada armazenamento de mensagens abertas no perfil.</span><span class="sxs-lookup"><span data-stu-id="6acdf-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="6acdf-122">Para uma lista completa das colunas necessárias e opcionais na tabela do armazenamento de mensagens, consulte [Tabelas do Armazenamento de Mensagens.](message-store-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6acdf-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6acdf-123">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6acdf-123">Notes to callers</span></span>

<span data-ttu-id="6acdf-124">Como o MAPI atualiza a tabela do armazenamento de mensagens durante a sessão sempre que ocorrem alterações, chame o método **Advise** da tabela de armazenamento de mensagens para registrar para ser notificado dessas alterações.</span><span class="sxs-lookup"><span data-stu-id="6acdf-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="6acdf-125">As alterações possíveis incluem a adição de novos armazenamentos de mensagens, remoção de armazenamentos existentes e alterações no armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="6acdf-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="6acdf-126">A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="6acdf-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="6acdf-127">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="6acdf-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6acdf-128">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6acdf-128">MFCMAPI reference</span></span>

<span data-ttu-id="6acdf-129">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6acdf-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6acdf-130">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6acdf-130">**File**</span></span>|<span data-ttu-id="6acdf-131">**Função**</span><span class="sxs-lookup"><span data-stu-id="6acdf-131">**Function**</span></span>|<span data-ttu-id="6acdf-132">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="6acdf-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6acdf-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6acdf-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6acdf-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="6acdf-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="6acdf-135">MFCMAPI usa o método **IMAPISession::GetMsgStoresTable** para obter a tabela de armazenamento de mensagens para que ela possa ser renderizada na caixa de diálogo principal de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="6acdf-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6acdf-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6acdf-136">See also</span></span>



[<span data-ttu-id="6acdf-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="6acdf-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="6acdf-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6acdf-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="6acdf-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="6acdf-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="6acdf-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="6acdf-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="6acdf-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="6acdf-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="6acdf-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6acdf-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6acdf-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="6acdf-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="6acdf-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6acdf-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6acdf-145">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="6acdf-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6acdf-146">Tabelas do Armazenamento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="6acdf-146">Message Store Tables</span></span>](message-store-tables.md)

