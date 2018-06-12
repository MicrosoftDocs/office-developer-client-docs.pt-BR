---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767634"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="ac96c-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="ac96c-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="ac96c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac96c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac96c-105">Exclui um provedor de serviço do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac96c-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="ac96c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ac96c-106">Parameters</span></span>

 <span data-ttu-id="ac96c-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="ac96c-107">_lpUID_</span></span>
  
> <span data-ttu-id="ac96c-108">[além, out] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ac96c-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ac96c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ac96c-109">Return value</span></span>

<span data-ttu-id="ac96c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac96c-110">S_OK</span></span> 
  
> <span data-ttu-id="ac96c-111">O provedor foi excluído com êxito do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac96c-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="ac96c-112">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac96c-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ac96c-113">**MAPIUID** apontado pelo parâmetro _lpUID_ não foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="ac96c-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ac96c-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ac96c-114">Remarks</span></span>

<span data-ttu-id="ac96c-115">O método **IProviderAdmin::DeleteProvider** exclui um provedor de serviço do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ac96c-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="ac96c-116">**DeleteProvider** determina o provedor de serviços para excluir combinando a estrutura **MAPIUID** apontada pela _lpUID_ com o conjunto de identificadores registrados pelos provedores de serviço ativo.</span><span class="sxs-lookup"><span data-stu-id="ac96c-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="ac96c-117">A maioria dos serviços de mensagem não permita provedores a ser excluída enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="ac96c-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="ac96c-118">Se o provedor para excluir estiver em uso, **DeleteProvider** marca para exclusão, em vez de removê-lo imediatamente e retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="ac96c-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="ac96c-119">Quando o provedor não está sendo usado, ela é excluída.</span><span class="sxs-lookup"><span data-stu-id="ac96c-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="ac96c-120">**DeleteProvider** chama a função de ponto de entrada do serviço de mensagem antes que o provedor é removido do serviço de.</span><span class="sxs-lookup"><span data-stu-id="ac96c-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="ac96c-121">O parâmetro _ulContext_ é definido como MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="ac96c-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="ac96c-122">A função de ponto de entrada de serviço de mensagem executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="ac96c-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="ac96c-123">Exclui o provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="ac96c-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="ac96c-124">Exclui a seção de perfil do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="ac96c-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="ac96c-125">A função de ponto de entrada de serviço de mensagem não é chamada novamente após o provedor ter sido excluído.</span><span class="sxs-lookup"><span data-stu-id="ac96c-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac96c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac96c-126">See also</span></span>



[<span data-ttu-id="ac96c-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ac96c-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ac96c-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="ac96c-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="ac96c-129">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac96c-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

