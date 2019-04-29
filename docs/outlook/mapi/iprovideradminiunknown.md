---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437529"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="b496f-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b496f-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="b496f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b496f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b496f-105">Funciona com provedores de serviços em um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b496f-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b496f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b496f-106">Header file:</span></span>  <br/> |<span data-ttu-id="b496f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b496f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b496f-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="b496f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b496f-109">Objetos de administração de provedor</span><span class="sxs-lookup"><span data-stu-id="b496f-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="b496f-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b496f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b496f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b496f-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b496f-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b496f-112">Called by:</span></span>  <br/> |<span data-ttu-id="b496f-113">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b496f-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="b496f-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="b496f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b496f-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="b496f-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="b496f-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="b496f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b496f-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="b496f-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b496f-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="b496f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b496f-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b496f-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="b496f-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu com o objeto de administração de provedor.</span><span class="sxs-lookup"><span data-stu-id="b496f-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="b496f-121">GetProvidertable</span><span class="sxs-lookup"><span data-stu-id="b496f-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="b496f-122">Fornece acesso à tabela do provedor do serviço de mensagens, uma lista dos provedores de serviços no serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b496f-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="b496f-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="b496f-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="b496f-124">Adiciona um provedor de serviços ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b496f-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="b496f-125">Deleteprovider</span><span class="sxs-lookup"><span data-stu-id="b496f-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="b496f-126">Exclui um provedor de serviços do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b496f-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="b496f-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="b496f-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="b496f-128">Abre uma seção de perfil do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="b496f-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b496f-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b496f-129">Remarks</span></span>

<span data-ttu-id="b496f-130">Os clientes podem obter um ponteiro para uma interface **IProviderAdmin** chamando o método [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) ; os provedores de serviços recebem um ponteiro **IProviderAdmin** quando a função de ponto de entrada do serviço de mensagens é chamada.</span><span class="sxs-lookup"><span data-stu-id="b496f-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b496f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b496f-131">See also</span></span>



[<span data-ttu-id="b496f-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b496f-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

