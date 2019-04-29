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
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="bcf50-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="bcf50-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="bcf50-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcf50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcf50-105">Fornece acesso à tabela status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.</span><span class="sxs-lookup"><span data-stu-id="bcf50-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="bcf50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcf50-106">Parameters</span></span>

 <span data-ttu-id="bcf50-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bcf50-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bcf50-108">no Uma bitmask de sinalizadores que determina o formato das colunas que são cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bcf50-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="bcf50-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="bcf50-109">The following flag can be set:</span></span>
    
<span data-ttu-id="bcf50-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bcf50-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bcf50-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bcf50-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="bcf50-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas da cadeia de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bcf50-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="bcf50-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="bcf50-113">_lppTable_</span></span>
  
> <span data-ttu-id="bcf50-114">bota Um ponteiro para um ponteiro para a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="bcf50-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcf50-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bcf50-115">Return value</span></span>

<span data-ttu-id="bcf50-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcf50-116">S_OK</span></span> 
  
> <span data-ttu-id="bcf50-117">A tabela foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="bcf50-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bcf50-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcf50-118">Remarks</span></span>

<span data-ttu-id="bcf50-119">O método **IMAPISession::** getstatustable fornece acesso à tabela de status que contém informações sobre todos os recursos MAPI na sessão.</span><span class="sxs-lookup"><span data-stu-id="bcf50-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="bcf50-120">Há uma linha na tabela para obter informações sobre o subsistema MAPI, uma linha para o spooler MAPI, uma linha para o catálogo de endereços integrado e uma linha para cada provedor de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="bcf50-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="bcf50-121">Para obter uma lista completa de colunas obrigatórias e opcionais na tabela status, consulte [tabelas de status](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="bcf50-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="bcf50-122">Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="bcf50-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="bcf50-123">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="bcf50-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bcf50-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bcf50-124">MFCMAPI reference</span></span>

<span data-ttu-id="bcf50-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcf50-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bcf50-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="bcf50-126">**File**</span></span>|<span data-ttu-id="bcf50-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="bcf50-127">**Function**</span></span>|<span data-ttu-id="bcf50-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="bcf50-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcf50-129">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="bcf50-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="bcf50-130">CMainDlg:: onStatustable</span><span class="sxs-lookup"><span data-stu-id="bcf50-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="bcf50-131">MFCMAPI usa o método **IMAPISession::** getstatustable para obter a tabela de status a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="bcf50-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcf50-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcf50-132">See also</span></span>



[<span data-ttu-id="bcf50-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcf50-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="bcf50-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="bcf50-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="bcf50-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bcf50-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="bcf50-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="bcf50-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="bcf50-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="bcf50-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="bcf50-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="bcf50-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="bcf50-139">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bcf50-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="bcf50-140">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="bcf50-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bcf50-141">Tabelas de status</span><span class="sxs-lookup"><span data-stu-id="bcf50-141">Status Tables</span></span>](status-tables.md)

