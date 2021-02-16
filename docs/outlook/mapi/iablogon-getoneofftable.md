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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411873"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="af128-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="af128-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="af128-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af128-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af128-105">Retorna uma tabela de modelos one-off para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="af128-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="af128-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af128-106">Parameters</span></span>

 <span data-ttu-id="af128-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af128-107">_ulFlags_</span></span>
  
> <span data-ttu-id="af128-108">[in] Uma bitmask de sinalizadores que controla o tipo de colunas de cadeia de caracteres incluídas na tabela.</span><span class="sxs-lookup"><span data-stu-id="af128-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="af128-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="af128-109">The following flag can be set:</span></span>
    
<span data-ttu-id="af128-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af128-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af128-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="af128-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="af128-112">Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="af128-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="af128-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="af128-113">_lppTable_</span></span>
  
> <span data-ttu-id="af128-114">[out] Um ponteiro para um ponteiro para a tabela um-off.</span><span class="sxs-lookup"><span data-stu-id="af128-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af128-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="af128-115">Return value</span></span>

<span data-ttu-id="af128-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="af128-116">S_OK</span></span> 
  
> <span data-ttu-id="af128-117">A tabela única foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="af128-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="af128-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="af128-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="af128-119">O sinalizador MAPI_UNICODE de endereços foi definido e o provedor de agendas não oferece suporte a Unicode ou MAPI_UNICODE não foi definido e o provedor de livro de endereços oferece suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="af128-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="af128-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="af128-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="af128-121">O provedor de agendas não fornece modelos one-off.</span><span class="sxs-lookup"><span data-stu-id="af128-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af128-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="af128-122">Remarks</span></span>

<span data-ttu-id="af128-123">O MAPI chama **o método GetOneOffTable** para disponibilizar modelos one-off para criar destinatários.</span><span class="sxs-lookup"><span data-stu-id="af128-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="af128-124">Os novos destinatários são adicionados à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="af128-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="af128-125">Os provedores de agenda devem dar suporte à notificação em sua tabela única para informar o MAPI sobre modificações de modelo.</span><span class="sxs-lookup"><span data-stu-id="af128-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="af128-126">O MAPI mantém a tabela única aberta para habilitar a atualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="af128-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="af128-127">Os provedores de agendas também podem dar suporte a uma tabela única para cada um de seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="af128-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="af128-128">Os chamadores recuperam essa tabela única chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner e solicitando a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="af128-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="af128-129">Os modelos disponíveis por meio desta tabela são usados para adicionar destinatários ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="af128-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="af128-130">Para uma discussão sobre as diferenças entre os dois tipos de tabelas um-off, consulte Implementando One-Off [tabelas](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="af128-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="af128-131">Para uma lista das colunas necessárias na tabela única de um provedor de agendas, consulte [Tabelas One-Off.](one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="af128-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af128-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="af128-132">See also</span></span>



[<span data-ttu-id="af128-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="af128-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="af128-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="af128-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="af128-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="af128-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="af128-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af128-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

