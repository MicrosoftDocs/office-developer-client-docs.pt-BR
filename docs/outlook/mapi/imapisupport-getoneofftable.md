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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316573"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="32f7e-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="32f7e-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="32f7e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32f7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32f7e-105">Retorna um ponteiro para a tabela única de MAPI (uma lista de modelos que todos os provedores de catálogo de endereços dão suporte à criação de novos destinatários).</span><span class="sxs-lookup"><span data-stu-id="32f7e-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="32f7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32f7e-106">Parameters</span></span>

 <span data-ttu-id="32f7e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32f7e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="32f7e-108">no Uma bitmask de sinalizadores que controla o tipo das colunas de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32f7e-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="32f7e-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="32f7e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="32f7e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="32f7e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="32f7e-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="32f7e-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="32f7e-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas da cadeia de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="32f7e-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="32f7e-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="32f7e-113">_lppTable_</span></span>
  
> <span data-ttu-id="32f7e-114">bota Um ponteiro para um ponteiro para a tabela única.</span><span class="sxs-lookup"><span data-stu-id="32f7e-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32f7e-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="32f7e-115">Return value</span></span>

<span data-ttu-id="32f7e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="32f7e-116">S_OK</span></span> 
  
> <span data-ttu-id="32f7e-117">A tabela única foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="32f7e-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32f7e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="32f7e-118">Remarks</span></span>

<span data-ttu-id="32f7e-119">O método **IMAPISupport:: GetOneOffTable** é implementado para objetos de suporte do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="32f7e-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="32f7e-120">Os provedores de catálogo de endereços chamam **GetOneOffTable** para recuperar a lista completa de modelos para a criação de novos destinatários.</span><span class="sxs-lookup"><span data-stu-id="32f7e-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="32f7e-121">Esta tabela inclui modelos que os provedores de catálogo de endereços estão ativos no suporte de sessão, bem como os modelos suportados por MAPI.</span><span class="sxs-lookup"><span data-stu-id="32f7e-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="32f7e-122">Os destinatários recém-criados podem ser usados para endereçar uma mensagem ou podem ser adicionados a um contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="32f7e-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="32f7e-123">Para obter uma lista das propriedades que compõem o conjunto de colunas obrigatórios em tabelas únicas, consulte [one-off Tables](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="32f7e-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="32f7e-124">Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta o formato das colunas retornadas dos métodos IMAPITable [:: QueryColumns](imapitable-querycolumns.md) e IMAPITable [:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="32f7e-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="32f7e-125">Esse sinalizador também controla os tipos de propriedade na ordem de classificação retornada pelo método imApitable [:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="32f7e-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="32f7e-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="32f7e-126">Notes to callers</span></span>

<span data-ttu-id="32f7e-127">Se você estiver registrado para receber notificações de alterações para esta tabela única, você também receberá notificações de alterações para as tabelas únicas de outros provedores.</span><span class="sxs-lookup"><span data-stu-id="32f7e-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="32f7e-128">Com base nessas notificações, você pode dar suporte a novos tipos de endereço que são adicionados durante a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="32f7e-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="32f7e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="32f7e-129">See also</span></span>



[<span data-ttu-id="32f7e-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="32f7e-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="32f7e-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="32f7e-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="32f7e-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="32f7e-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="32f7e-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="32f7e-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="32f7e-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="32f7e-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="32f7e-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="32f7e-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="32f7e-136">Propriedade canônica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="32f7e-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="32f7e-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="32f7e-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="32f7e-138">Tabelas únicas</span><span class="sxs-lookup"><span data-stu-id="32f7e-138">One-Off Tables</span></span>](one-off-tables.md)

