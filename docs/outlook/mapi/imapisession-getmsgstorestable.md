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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767168"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="0e5e7-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="0e5e7-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="0e5e7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e5e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e5e7-105">Fornece acesso à tabela do repositório de mensagem que contém informações sobre todos os repositórios de mensagem no perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="0e5e7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0e5e7-106">Parameters</span></span>

 <span data-ttu-id="0e5e7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0e5e7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0e5e7-108">[in] Uma bitmask dos sinalizadores que determina o formato de colunas que são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="0e5e7-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="0e5e7-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0e5e7-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e5e7-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0e5e7-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="0e5e7-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="0e5e7-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="0e5e7-113">_lppTable_</span></span>
  
> <span data-ttu-id="0e5e7-114">[out] Um ponteiro para um ponteiro para a tabela de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0e5e7-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0e5e7-115">Return value</span></span>

<span data-ttu-id="0e5e7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0e5e7-116">S_OK</span></span> 
  
> <span data-ttu-id="0e5e7-117">A tabela foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="0e5e7-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0e5e7-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0e5e7-119">O sinalizador MAPI_UNICODE foi definido e a sessão não dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0e5e7-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0e5e7-120">Remarks</span></span>

<span data-ttu-id="0e5e7-121">O método **IMAPISession::GetMsgStoresTable** recupera um ponteiro para a tabela de repositório de mensagens, uma tabela mantidas por MAPI que contém informações sobre cada repositório de mensagem aberta no perfil.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="0e5e7-122">Para obter uma lista completa das colunas obrigatórios e opcionais na mensagem repositório tabela, consulte [Tabelas de armazenar mensagens](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0e5e7-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0e5e7-123">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0e5e7-123">Notes to callers</span></span>

<span data-ttu-id="0e5e7-124">Como MAPI atualiza a tabela de repositório de mensagens durante a sessão sempre que ocorrerem alterações, chame o método **Advise** a tabela de repositório de mensagens para registrar para ser notificado sobre essas alterações.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="0e5e7-125">Alterações possíveis incluem a adição de novas lojas de mensagem, remoção de existentes armazena e altera para o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="0e5e7-126">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="0e5e7-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="0e5e7-127">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="0e5e7-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0e5e7-128">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0e5e7-128">MFCMAPI reference</span></span>

<span data-ttu-id="0e5e7-129">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0e5e7-130">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0e5e7-130">**File**</span></span>|<span data-ttu-id="0e5e7-131">**Function**</span><span class="sxs-lookup"><span data-stu-id="0e5e7-131">**Function**</span></span>|<span data-ttu-id="0e5e7-132">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0e5e7-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0e5e7-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0e5e7-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="0e5e7-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="0e5e7-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="0e5e7-135">MFCMAPI usa o método **IMAPISession::GetMsgStoresTable** para obter a tabela de repositório de mensagens, de modo que ele poderá ser renderizado da caixa de diálogo principal do MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="0e5e7-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e5e7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e5e7-136">See also</span></span>



[<span data-ttu-id="0e5e7-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="0e5e7-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="0e5e7-138">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e5e7-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="0e5e7-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="0e5e7-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="0e5e7-140">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="0e5e7-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="0e5e7-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="0e5e7-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="0e5e7-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="0e5e7-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="0e5e7-143">IMAPITable:: SortTable</span><span class="sxs-lookup"><span data-stu-id="0e5e7-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="0e5e7-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e5e7-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="0e5e7-145">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0e5e7-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0e5e7-146">Tabelas de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="0e5e7-146">Message Store Tables</span></span>](message-store-tables.md)

