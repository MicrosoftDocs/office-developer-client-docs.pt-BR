---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767659"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="a3b83-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="a3b83-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="a3b83-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3b83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3b83-105">Fornece acesso à tabela do provedor do serviço na mensagem, uma lista dos provedores de serviço no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3b83-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="a3b83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3b83-106">Parameters</span></span>

 <span data-ttu-id="a3b83-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3b83-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a3b83-108">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres retornada nas colunas da tabela provedor.</span><span class="sxs-lookup"><span data-stu-id="a3b83-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="a3b83-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="a3b83-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a3b83-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a3b83-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a3b83-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a3b83-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="a3b83-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas são no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a3b83-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="a3b83-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a3b83-113">_lppTable_</span></span>
  
> <span data-ttu-id="a3b83-114">[out] Um ponteiro para um ponteiro para a tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="a3b83-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3b83-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a3b83-115">Return value</span></span>

<span data-ttu-id="a3b83-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3b83-116">S_OK</span></span> 
  
> <span data-ttu-id="a3b83-117">A tabela de provedor foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="a3b83-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3b83-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3b83-118">Remarks</span></span>

<span data-ttu-id="a3b83-119">O método **IProviderAdmin::GetProviderTable** recupera um ponteiro para a tabela de provedor do serviço na mensagem, uma tabela que mantém o MAPI que contém informações sobre cada provedor de serviço no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3b83-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="a3b83-120">Ao contrário da tabela de provedor retornada pelo método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , a tabela de provedor retornada pela **IProviderAdmin::GetProviderTable** pode incluir linhas adicionais que representam informações associadas a um ou mais dos os provedores de serviço no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3b83-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="a3b83-121">Essas informações extras são adicionadas ao perfil com a palavra-chave "Seções" do arquivo Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="a3b83-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="a3b83-122">Quando um provedor tem seções perfil extra, ele armazena as estruturas de **MAPIUID** para estas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3b83-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="a3b83-123">**PR_SERVICE_EXTRA_UIDS** é salvo na seção de perfil de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a3b83-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="a3b83-124">Os provedores que forem excluídos, ou estiverem em uso, foram marcados para exclusão, mas não são incluídos na tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="a3b83-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="a3b83-125">As tabelas de provedor são estáticas, que significa subsequentes adições à ou exclusões do serviço de mensagem não serão refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="a3b83-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="a3b83-126">Se o serviço de mensagem não tiver nenhum provedor, **IProviderAdmin::GetProviderTable** retornará uma tabela com zero linhas e o valor de retorno S_OK.</span><span class="sxs-lookup"><span data-stu-id="a3b83-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="a3b83-127">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b83-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="a3b83-128">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b83-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="a3b83-129">Para obter uma lista completa das colunas da tabela de provedor, consulte a [Tabela de provedor](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a3b83-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3b83-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a3b83-130">Notes to callers</span></span>

<span data-ttu-id="a3b83-131">Para recuperar as linhas de uma tabela de provedor na ordem de transporte, classifica a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3b83-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="a3b83-132">Para recuperar apenas as linhas que representam os provedores de serviços (sem incluindo qualquer linha extra), limite sua recuperação às linhas que possuem um valor de PT_ERROR na sua coluna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a3b83-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a3b83-133">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a3b83-133">MFCMAPI reference</span></span>

<span data-ttu-id="a3b83-134">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3b83-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a3b83-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="a3b83-135">**File**</span></span>|<span data-ttu-id="a3b83-136">**Function**</span><span class="sxs-lookup"><span data-stu-id="a3b83-136">**Function**</span></span>|<span data-ttu-id="a3b83-137">**Comment**</span><span class="sxs-lookup"><span data-stu-id="a3b83-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a3b83-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a3b83-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="a3b83-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="a3b83-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="a3b83-140">MFCMAPI usa o método **IProviderAdmin::GetProviderTable** para obter a tabela de provedores para renderizar em uma nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a3b83-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3b83-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3b83-141">See also</span></span>



[<span data-ttu-id="a3b83-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a3b83-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a3b83-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a3b83-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a3b83-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a3b83-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a3b83-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a3b83-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a3b83-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="a3b83-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="a3b83-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3b83-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="a3b83-148">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="a3b83-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

