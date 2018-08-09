---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766837"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="1be2a-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="1be2a-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="1be2a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1be2a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1be2a-105">Retorna uma tabela de modelos únicos para a criação de destinatários a ser adicionado à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="1be2a-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1be2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1be2a-106">Parameters</span></span>

 <span data-ttu-id="1be2a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1be2a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1be2a-108">[in] Uma bitmask dos sinalizadores que controla o tipo das colunas de cadeia de caracteres incluídos na tabela.</span><span class="sxs-lookup"><span data-stu-id="1be2a-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="1be2a-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1be2a-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1be2a-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1be2a-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1be2a-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1be2a-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="1be2a-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1be2a-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="1be2a-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="1be2a-113">_lppTable_</span></span>
  
> <span data-ttu-id="1be2a-114">[out] Um ponteiro para um ponteiro para a tabela único.</span><span class="sxs-lookup"><span data-stu-id="1be2a-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1be2a-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1be2a-115">Return value</span></span>

<span data-ttu-id="1be2a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1be2a-116">S_OK</span></span> 
  
> <span data-ttu-id="1be2a-117">A tabela único foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1be2a-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="1be2a-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1be2a-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1be2a-119">Tanto o sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e o provedor de catálogo de endereços suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="1be2a-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="1be2a-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1be2a-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1be2a-121">O provedor de catálogo de endereços não fornecer quaisquer modelos únicos.</span><span class="sxs-lookup"><span data-stu-id="1be2a-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1be2a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1be2a-122">Remarks</span></span>

<span data-ttu-id="1be2a-123">MAPI chama o método **GetOneOffTable** para tornar modelos únicos disponíveis para criar os destinatários.</span><span class="sxs-lookup"><span data-stu-id="1be2a-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="1be2a-124">Os destinatários novos são adicionados à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="1be2a-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="1be2a-125">Provedores de catálogo de endereços devem oferecer suporte a notificação em seu tabela único para informar MAPI de modificações em modelos.</span><span class="sxs-lookup"><span data-stu-id="1be2a-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="1be2a-126">MAPI mantém a tabela único abertas para habilitar a atualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="1be2a-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="1be2a-127">Provedores de catálogo de endereços também podem oferecer suporte uma tabela único para cada um dos seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="1be2a-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="1be2a-128">Os chamadores recuperar esta tabela único chamando o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner e solicitar a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1be2a-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="1be2a-129">Os modelos disponíveis por meio de nesta tabela são usados para adicionar destinatários ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be2a-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="1be2a-130">Para uma discussão das diferenças entre os dois tipos de tabelas únicos, consulte [Implementando únicos Tables](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1be2a-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="1be2a-131">Para obter uma lista das colunas na tabela de um provedor catálogo de endereços únicos necessárias, consulte [Tabelas únicos](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1be2a-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1be2a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be2a-132">See also</span></span>



[<span data-ttu-id="1be2a-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="1be2a-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="1be2a-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="1be2a-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="1be2a-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="1be2a-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="1be2a-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1be2a-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

