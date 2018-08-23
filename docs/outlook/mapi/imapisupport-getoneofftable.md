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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d54487928abcc889441ec9bf89ab6a10e5290062
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570832"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="03840-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="03840-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="03840-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03840-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03840-105">Retorna um ponteiro para a tabela MAPI único (uma lista de modelos que todos no catálogo de endereços provedores de suporte para a criação de novos destinatários).</span><span class="sxs-lookup"><span data-stu-id="03840-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="03840-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03840-106">Parameters</span></span>

 <span data-ttu-id="03840-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03840-107">_ulFlags_</span></span>
  
> <span data-ttu-id="03840-108">[in] Uma bitmask dos sinalizadores que controla o tipo das colunas de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="03840-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="03840-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="03840-109">The following flag can be set:</span></span>
    
<span data-ttu-id="03840-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="03840-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="03840-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="03840-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="03840-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="03840-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="03840-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="03840-113">_lppTable_</span></span>
  
> <span data-ttu-id="03840-114">[out] Um ponteiro para um ponteiro para a tabela único.</span><span class="sxs-lookup"><span data-stu-id="03840-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="03840-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="03840-115">Return value</span></span>

<span data-ttu-id="03840-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="03840-116">S_OK</span></span> 
  
> <span data-ttu-id="03840-117">A tabela único foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="03840-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03840-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="03840-118">Remarks</span></span>

<span data-ttu-id="03840-119">O método **IMAPISupport::GetOneOffTable** é implementado para objetos de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="03840-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="03840-120">Provedores de catálogo de endereço chamarem **GetOneOffTable** para recuperar a lista completa de modelos para a criação de novos destinatários.</span><span class="sxs-lookup"><span data-stu-id="03840-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="03840-121">Esta tabela inclui modelos que oferecem suporte a provedores de catálogo de endereços que estão ativos na sessão, bem como modelos que ofereça suporte a MAPI.</span><span class="sxs-lookup"><span data-stu-id="03840-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="03840-122">Os destinatários recém-criado podem ser usados para endereçar uma mensagem ou podem ser adicionados a um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="03840-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="03840-123">Para obter uma lista das propriedades que compõem a coluna necessária definida nas tabelas únicas, consulte [Tabelas únicos](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="03840-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="03840-124">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta o formato das colunas retornado dos métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="03840-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="03840-125">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornadas pelo método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="03840-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="03840-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="03840-126">Notes to callers</span></span>

<span data-ttu-id="03840-127">Se você estiver registrado para receber notificações de alterações para esta tabela único, você também receberá notificações de alterações nas tabelas de únicos dos outros provedores.</span><span class="sxs-lookup"><span data-stu-id="03840-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="03840-128">Com base nessas notificações, você pode suportar novos tipos de endereço que são adicionados durante a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="03840-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03840-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="03840-129">See also</span></span>



[<span data-ttu-id="03840-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="03840-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="03840-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="03840-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="03840-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03840-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="03840-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="03840-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="03840-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="03840-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="03840-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="03840-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="03840-136">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="03840-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="03840-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="03840-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="03840-138">Tabelas únicas</span><span class="sxs-lookup"><span data-stu-id="03840-138">One-Off Tables</span></span>](one-off-tables.md)

