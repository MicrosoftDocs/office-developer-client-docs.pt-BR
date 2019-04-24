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
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279525"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="5f384-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="5f384-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="5f384-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f384-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f384-105">Fornece acesso à tabela do provedor do serviço de mensagens, uma lista dos provedores de serviços no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f384-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5f384-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f384-106">Parameters</span></span>

 <span data-ttu-id="5f384-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5f384-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5f384-108">no Uma bitmask de sinalizadores que controla o tipo das cadeias de caracteres retornadas nas colunas da tabela do provedor.</span><span class="sxs-lookup"><span data-stu-id="5f384-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="5f384-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="5f384-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5f384-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5f384-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5f384-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5f384-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="5f384-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5f384-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="5f384-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5f384-113">_lppTable_</span></span>
  
> <span data-ttu-id="5f384-114">bota Um ponteiro para um ponteiro para a tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="5f384-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f384-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5f384-115">Return value</span></span>

<span data-ttu-id="5f384-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f384-116">S_OK</span></span> 
  
> <span data-ttu-id="5f384-117">A tabela do provedor foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="5f384-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f384-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f384-118">Remarks</span></span>

<span data-ttu-id="5f384-119">O método **IProviderAdmin::** getprovidertable recupera um ponteiro para a tabela do provedor do serviço de mensagens, uma tabela que o MAPI mantém que contém informações sobre cada provedor de serviços no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f384-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="5f384-120">Diferente da tabela de provedor retornada pelo método [IMsgServiceAdmin::](imsgserviceadmin-getprovidertable.md) getprovidertable, a tabela de provedor retornada por **IProviderAdmin::** getprovidertable pode incluir linhas adicionais que representam informações associadas a um ou mais dos os provedores de serviços no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f384-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="5f384-121">Essas informações extras são adicionadas ao perfil com a palavra-chave "seções" do arquivo MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="5f384-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="5f384-122">Quando um provedor tem seções de perfil extra, ele armazena as estruturas **MAPIUID** para essas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f384-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="5f384-123">**PR_SERVICE_EXTRA_UIDS** é salvo na seção perfil de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5f384-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="5f384-124">Os provedores que foram excluídos ou estão em uso, mas que foram marcados para exclusão, não estão incluídos na tabela do provedor.</span><span class="sxs-lookup"><span data-stu-id="5f384-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="5f384-125">As tabelas de provedor são estáticas, o que significa que adições ou exclusões subsequentes do serviço de mensagens não são refletidas na tabela.</span><span class="sxs-lookup"><span data-stu-id="5f384-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="5f384-126">Se o serviço de mensagens não tiver provedores, **IProviderAdmin::** getprovidertable retornará uma tabela com zero linhas e o valor de retorno de S_OK.</span><span class="sxs-lookup"><span data-stu-id="5f384-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="5f384-127">Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="5f384-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="5f384-128">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="5f384-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="5f384-129">Para obter uma lista completa das colunas na tabela do provedor, consulte [tabela do provedor](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5f384-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5f384-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5f384-130">Notes to callers</span></span>

<span data-ttu-id="5f384-131">Para recuperar as linhas de uma tabela de provedor em ordem de transporte, classifique a tabela pela coluna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f384-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="5f384-132">Para recuperar somente as linhas que representam provedores de serviço (sem incluir nenhuma linha extra), limite a recuperação às linhas que têm um valor de PT_ERROR na coluna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5f384-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5f384-133">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5f384-133">MFCMAPI reference</span></span>

<span data-ttu-id="5f384-134">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f384-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5f384-135">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="5f384-135">**File**</span></span>|<span data-ttu-id="5f384-136">**Função**</span><span class="sxs-lookup"><span data-stu-id="5f384-136">**Function**</span></span>|<span data-ttu-id="5f384-137">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="5f384-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5f384-138">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="5f384-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="5f384-139">CMsgServiceTableDlg:: OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="5f384-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="5f384-140">MFCMAPI usa o método **IProviderAdmin::** getprovidertable para obter a tabela de provedores para renderizar em uma nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5f384-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f384-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f384-141">See also</span></span>



[<span data-ttu-id="5f384-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="5f384-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="5f384-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="5f384-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="5f384-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="5f384-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="5f384-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="5f384-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="5f384-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="5f384-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="5f384-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f384-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="5f384-148">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="5f384-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

