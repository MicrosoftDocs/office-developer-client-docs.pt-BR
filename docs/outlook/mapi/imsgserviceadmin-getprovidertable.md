---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428764"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="05574-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="05574-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="05574-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05574-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05574-105">Fornece acesso à tabela do provedor, uma lista dos provedores de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="05574-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="05574-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05574-106">Parameters</span></span>

 <span data-ttu-id="05574-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05574-107">_ulFlags_</span></span>
  
> <span data-ttu-id="05574-108">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="05574-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="05574-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="05574-109">_lppTable_</span></span>
  
> <span data-ttu-id="05574-110">bota Um ponteiro para um ponteiro para a tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="05574-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05574-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="05574-111">Return value</span></span>

<span data-ttu-id="05574-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="05574-112">S_OK</span></span> 
  
> <span data-ttu-id="05574-113">A tabela do provedor foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="05574-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05574-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="05574-114">Remarks</span></span>

<span data-ttu-id="05574-115">O método **IMsgServiceAdmin::** getprovidertable fornece acesso à tabela de provedor MAPI, uma tabela que lista todo o catálogo de endereços, o repositório de mensagens e os provedores de transporte atualmente instalados no perfil.</span><span class="sxs-lookup"><span data-stu-id="05574-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="05574-116">Diferente da tabela de provedor retornada por meio do método [IProviderAdmin::](iprovideradmin-getprovidertable.md) getprovidertable, a tabela de provedor retornada através de **IMsgServiceAdmin::** getprovidertable não pode incluir linhas adicionais que representam informações associadas com um ou mais provedores de serviço no perfil.</span><span class="sxs-lookup"><span data-stu-id="05574-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="05574-117">Os provedores que foram excluídos ou estão em uso, mas que foram marcados para exclusão, não estão incluídos na tabela do provedor.</span><span class="sxs-lookup"><span data-stu-id="05574-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="05574-118">As tabelas de provedor são estáticas, o que significa que adições ou exclusões subsequentes do perfil não são refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="05574-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="05574-119">Se o perfil não tiver provedores, \*\*\*\* getprovidertable retornará uma tabela com zero linhas e o valor de retorno de S_OK.</span><span class="sxs-lookup"><span data-stu-id="05574-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="05574-120">Para obter uma lista completa das colunas na tabela do provedor, consulte [tabela do provedor](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="05574-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="05574-121">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="05574-121">Notes to callers</span></span>

<span data-ttu-id="05574-122">Para recuperar as linhas de uma tabela de provedor em ordem de transporte, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="05574-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="05574-123">Chame o método imApitable [:: Restrict](imapitable-restrict.md) para impor uma restrição de propriedade que corresponda à propriedade **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) com MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="05574-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="05574-124">Chame o método imApitable [:: SortTable](imapitable-sorttable.md) para classificar a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="05574-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="05574-125">Chame o método imApitable [:: QueryRows](imapitable-queryrows.md) para obter as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="05574-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="05574-126">Uma alternativa para essas chamadas é fazer uma única chamada para a função [HrQueryAllRows](hrqueryallrows.md) com todas as estruturas de dados apropriadas passadas.</span><span class="sxs-lookup"><span data-stu-id="05574-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="05574-127">Se você recuperar as colunas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) em cada uma das linhas, poderá usar essa matriz de estruturas do **MAPIUID** para definir a ordem de transporte em uma chamada para [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span><span class="sxs-lookup"><span data-stu-id="05574-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="05574-128">Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="05574-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="05574-129">Define o tipo de cadeia de caracteres como Unicode para dados retornados para as colunas iniciais ativas da tabela do provedor pelo método imApitable [:: QueryColumns](imapitable-querycolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="05574-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="05574-130">As colunas iniciais ativas de uma tabela de provedor são aquelas colunas que o método **QueryColumns** retorna antes de o provedor que contém a tabela chamar o método IMAPITable [::](imapitable-setcolumns.md) SetColumns.</span><span class="sxs-lookup"><span data-stu-id="05574-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="05574-131">Define o tipo de cadeia de caracteres como Unicode para dados retornados para as linhas iniciais ativas da tabela do provedor por **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="05574-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="05574-132">As linhas iniciais ativas de uma tabela de provedor são as linhas que **QueryRows** retorna antes do provedor que contém \*\*\*\* SetColumns de chamadas de tabela.</span><span class="sxs-lookup"><span data-stu-id="05574-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="05574-133">Controla os tipos de propriedade da ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) antes de o cliente que contém a tabela do provedor chamar o método IMAPITable [:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="05574-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="05574-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="05574-134">See also</span></span>



[<span data-ttu-id="05574-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="05574-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="05574-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="05574-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="05574-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="05574-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="05574-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05574-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

