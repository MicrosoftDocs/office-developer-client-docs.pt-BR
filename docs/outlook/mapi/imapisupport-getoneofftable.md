---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412755"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="20703-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="20703-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="20703-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20703-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20703-105">Retorna um ponteiro para a tabela única MAPI (uma lista de modelos que todos os provedores de agenda de endereços suportam para criar novos destinatários).</span><span class="sxs-lookup"><span data-stu-id="20703-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="20703-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20703-106">Parameters</span></span>

 <span data-ttu-id="20703-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20703-107">_ulFlags_</span></span>
  
> <span data-ttu-id="20703-108">[in] Uma máscara de bits de sinalizadores que controla o tipo das colunas de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="20703-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="20703-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="20703-109">The following flag can be set:</span></span>
    
<span data-ttu-id="20703-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="20703-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="20703-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="20703-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="20703-112">Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="20703-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="20703-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="20703-113">_lppTable_</span></span>
  
> <span data-ttu-id="20703-114">[out] Um ponteiro para um ponteiro para a tabela um-off.</span><span class="sxs-lookup"><span data-stu-id="20703-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20703-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20703-115">Return value</span></span>

<span data-ttu-id="20703-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="20703-116">S_OK</span></span> 
  
> <span data-ttu-id="20703-117">A tabela única foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="20703-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20703-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="20703-118">Remarks</span></span>

<span data-ttu-id="20703-119">O **método IMAPISupport::GetOneOffTable** é implementado para objetos de suporte do provedor de agendas de endereços.</span><span class="sxs-lookup"><span data-stu-id="20703-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="20703-120">Os provedores de agendamento de endereço chamam **GetOneOffTable** para recuperar a lista completa de modelos para criar novos destinatários.</span><span class="sxs-lookup"><span data-stu-id="20703-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="20703-121">Esta tabela inclui modelos que abordam provedores de livro de endereços que estão ativos no suporte à sessão, bem como modelos compatíveis com MAPI.</span><span class="sxs-lookup"><span data-stu-id="20703-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="20703-122">Os destinatários recém-criados podem ser usados para lidar com uma mensagem ou podem ser adicionados a um contêiner de um livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="20703-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="20703-123">Para uma lista das propriedades que com o conjunto de colunas necessários em tabelas únicas, consulte [Tabelas Únicas.](one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="20703-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="20703-124">A definição MAPI_UNICODE sinalizador de texto no parâmetro _ulFlags_ afeta o formato das colunas retornadas dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="20703-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="20703-125">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="20703-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="20703-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="20703-126">Notes to callers</span></span>

<span data-ttu-id="20703-127">Se você estiver registrado para receber notificações de alterações nesta tabela única, também receberá notificações de alterações nas tabelas one-off de outros provedores.</span><span class="sxs-lookup"><span data-stu-id="20703-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="20703-128">Com base nessas notificações, você pode dar suporte a novos tipos de endereços adicionados durante a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="20703-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20703-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="20703-129">See also</span></span>



[<span data-ttu-id="20703-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="20703-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="20703-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="20703-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="20703-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20703-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="20703-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="20703-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="20703-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="20703-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="20703-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="20703-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="20703-136">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="20703-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="20703-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="20703-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="20703-138">Tabelas One-Off</span><span class="sxs-lookup"><span data-stu-id="20703-138">One-Off Tables</span></span>](one-off-tables.md)

