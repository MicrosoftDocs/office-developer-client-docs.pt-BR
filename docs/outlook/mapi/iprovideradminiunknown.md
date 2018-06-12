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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767645"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="948d5-103">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="948d5-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="948d5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="948d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="948d5-105">Funciona com provedores de serviço em um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="948d5-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="948d5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="948d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="948d5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="948d5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="948d5-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="948d5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="948d5-109">Objetos de administração do provedor</span><span class="sxs-lookup"><span data-stu-id="948d5-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="948d5-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="948d5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="948d5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="948d5-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="948d5-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="948d5-112">Called by:</span></span>  <br/> |<span data-ttu-id="948d5-113">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="948d5-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="948d5-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="948d5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="948d5-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="948d5-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="948d5-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="948d5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="948d5-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="948d5-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="948d5-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="948d5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="948d5-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="948d5-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="948d5-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com o objeto de administração do provedor.</span><span class="sxs-lookup"><span data-stu-id="948d5-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="948d5-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="948d5-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="948d5-122">Fornece acesso à tabela do provedor do serviço na mensagem, uma lista dos provedores de serviço no serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="948d5-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="948d5-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="948d5-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="948d5-124">Adiciona um provedor de serviço para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="948d5-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="948d5-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="948d5-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="948d5-126">Exclui um provedor de serviço do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="948d5-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="948d5-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="948d5-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="948d5-128">Abre uma seção de perfil do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="948d5-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="948d5-129">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="948d5-129">Remarks</span></span>

<span data-ttu-id="948d5-130">Os clientes podem obter um ponteiro para uma interface **IProviderAdmin** chamando o método [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; provedores de serviços são passados um ponteiro **IProviderAdmin** quando a função de ponto de entrada do seu serviço de mensagem é chamada.</span><span class="sxs-lookup"><span data-stu-id="948d5-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="948d5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="948d5-131">See also</span></span>



[<span data-ttu-id="948d5-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="948d5-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

