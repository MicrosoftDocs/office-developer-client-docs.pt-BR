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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4272edef5b1b72944d1d27f0e4dd99ee4956aa57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767467"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="410b3-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="410b3-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="410b3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="410b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="410b3-105">Fornece acesso à tabela de provedor, uma lista de provedores de serviços de perfil.</span><span class="sxs-lookup"><span data-stu-id="410b3-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="410b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="410b3-106">Parameters</span></span>

 <span data-ttu-id="410b3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="410b3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="410b3-108">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="410b3-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="410b3-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="410b3-109">_lppTable_</span></span>
  
> <span data-ttu-id="410b3-110">[out] Um ponteiro para um ponteiro para a tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="410b3-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="410b3-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="410b3-111">Return value</span></span>

<span data-ttu-id="410b3-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="410b3-112">S_OK</span></span> 
  
> <span data-ttu-id="410b3-113">A tabela de provedor foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="410b3-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="410b3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="410b3-114">Remarks</span></span>

<span data-ttu-id="410b3-115">O método **IMsgServiceAdmin::GetProviderTable** fornece acesso à tabela de provedor MAPI, uma tabela que lista todos os catálogos de endereços, armazenamento de mensagens e provedores de transporte instalados atualmente no perfil.</span><span class="sxs-lookup"><span data-stu-id="410b3-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="410b3-116">Ao contrário da tabela de provedor retornada por meio do método [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) , a tabela de provedor retornada por meio de **IMsgServiceAdmin::GetProviderTable** não é possível incluir linhas adicionais que representam informações associadas com um ou mais provedores de serviços no perfil.</span><span class="sxs-lookup"><span data-stu-id="410b3-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="410b3-117">Os provedores que forem excluídos, ou estiverem em uso, foram marcados para exclusão, mas não são incluídos na tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="410b3-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="410b3-118">As tabelas de provedor são estáticas, o que significa que subsequentes adições à ou exclusões do perfil não são refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="410b3-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="410b3-119">Se o perfil não tiver nenhum provedor, **GetProviderTable** retornará uma tabela com zero linhas e o valor de retorno S_OK.</span><span class="sxs-lookup"><span data-stu-id="410b3-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="410b3-120">Para obter uma lista completa das colunas da tabela de provedor, consulte a [Tabela de provedor](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="410b3-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="410b3-121">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="410b3-121">Notes to callers</span></span>

<span data-ttu-id="410b3-122">Para recuperar as linhas de uma tabela de provedor na ordem de transporte, use o procedimento a seguir:</span><span class="sxs-lookup"><span data-stu-id="410b3-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="410b3-123">Chame o método [IMAPITable:: Restrict](imapitable-restrict.md) para impor uma restrição de propriedade que corresponda a propriedade **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) com MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="410b3-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="410b3-124">Chame o método [IMAPITable:: SortTable](imapitable-sorttable.md) para classificar a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="410b3-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="410b3-125">Chame o método [IMAPITable:: QueryRows](imapitable-queryrows.md) para obter as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="410b3-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="410b3-126">Uma alternativa para essas chamadas é tornar uma única chamada para a função [HrQueryAllRows](hrqueryallrows.md) com todos os dados apropriados estruturas passadas.</span><span class="sxs-lookup"><span data-stu-id="410b3-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="410b3-127">Se você recuperar as colunas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) em cada uma das linhas, você pode usar essa matriz de estruturas **MAPIUID** para definir a ordem de transporte em uma chamada para [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span><span class="sxs-lookup"><span data-stu-id="410b3-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="410b3-128">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="410b3-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="410b3-129">Define o tipo de cadeia de caracteres para Unicode para os dados retornados para colunas ativas iniciais da tabela provedor pelo método [IMAPITable::QueryColumns](imapitable-querycolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="410b3-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="410b3-130">Colunas ativas iniciais para uma tabela de provedor são as colunas que o método **QueryColumns** retorna antes do provedor que contém as chamadas de tabela o método [IMAPITable::SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="410b3-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="410b3-131">Define o tipo de cadeia de caracteres para Unicode para os dados retornados para as linhas de ativas iniciais da tabela provedor por **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="410b3-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="410b3-132">As linhas de ativas iniciais para uma tabela de provedor são aquelas linhas **que QueryRows** retorna antes do provedor que contém as chamadas de tabela **SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="410b3-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="410b3-133">Controles os tipos de propriedade da ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) antes que o cliente que contém a tabela de provedor chama o método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="410b3-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="410b3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="410b3-134">See also</span></span>



[<span data-ttu-id="410b3-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="410b3-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="410b3-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="410b3-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="410b3-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="410b3-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="410b3-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="410b3-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

