---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407134"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="ec7fa-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="ec7fa-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="ec7fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec7fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec7fa-105">Fornece acesso à tabela de status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ec7fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec7fa-106">Parameters</span></span>

 <span data-ttu-id="ec7fa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec7fa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ec7fa-108">[in] Uma bitmask de sinalizadores que determina o formato para colunas que são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="ec7fa-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="ec7fa-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ec7fa-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ec7fa-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ec7fa-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="ec7fa-112">Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="ec7fa-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ec7fa-113">_lppTable_</span></span>
  
> <span data-ttu-id="ec7fa-114">[out] Um ponteiro para um ponteiro para a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec7fa-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ec7fa-115">Return value</span></span>

<span data-ttu-id="ec7fa-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec7fa-116">S_OK</span></span> 
  
> <span data-ttu-id="ec7fa-117">A tabela foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec7fa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec7fa-118">Remarks</span></span>

<span data-ttu-id="ec7fa-119">O **método IMAPISession::GetStatusTable** fornece acesso à tabela de status que contém informações sobre todos os recursos MAPI na sessão.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="ec7fa-120">Há uma linha na tabela para obter informações sobre o subsistema MAPI, uma linha para o spooler MAPI, uma linha para o livro de endereços integrado e uma linha para cada provedor de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="ec7fa-121">Para uma lista completa das colunas necessárias e opcionais na tabela de status, consulte [Tabelas de Status.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="ec7fa-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="ec7fa-122">A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="ec7fa-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="ec7fa-123">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="ec7fa-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec7fa-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ec7fa-124">MFCMAPI reference</span></span>

<span data-ttu-id="ec7fa-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec7fa-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ec7fa-126">**File**</span></span>|<span data-ttu-id="ec7fa-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="ec7fa-127">**Function**</span></span>|<span data-ttu-id="ec7fa-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="ec7fa-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec7fa-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ec7fa-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="ec7fa-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="ec7fa-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="ec7fa-131">MFCMAPI usa o **método IMAPISession::GetStatusTable** para obter a tabela de status a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="ec7fa-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec7fa-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec7fa-132">See also</span></span>



[<span data-ttu-id="ec7fa-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec7fa-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="ec7fa-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ec7fa-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="ec7fa-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ec7fa-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ec7fa-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ec7fa-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="ec7fa-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="ec7fa-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="ec7fa-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="ec7fa-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="ec7fa-139">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec7fa-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="ec7fa-140">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ec7fa-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ec7fa-141">Tabelas de Status</span><span class="sxs-lookup"><span data-stu-id="ec7fa-141">Status Tables</span></span>](status-tables.md)

