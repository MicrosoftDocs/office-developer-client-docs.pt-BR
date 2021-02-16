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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404859"
---
# <a name="iprovideradmindeleteprovider"></a><span data-ttu-id="c48f1-103">IProviderAdmin::DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="c48f1-103">IProviderAdmin::DeleteProvider</span></span>

  
  
<span data-ttu-id="c48f1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c48f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c48f1-105">Exclui um provedor de serviços do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c48f1-105">Deletes a service provider from the message service.</span></span>
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="c48f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c48f1-106">Parameters</span></span>

 <span data-ttu-id="c48f1-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c48f1-107">_lpUID_</span></span>
  
> <span data-ttu-id="c48f1-108">[in, out] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c48f1-108">[in, out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c48f1-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c48f1-109">Return value</span></span>

<span data-ttu-id="c48f1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c48f1-110">S_OK</span></span> 
  
> <span data-ttu-id="c48f1-111">O provedor foi excluído com êxito do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c48f1-111">The provider was successfully deleted from the message service.</span></span>
    
<span data-ttu-id="c48f1-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c48f1-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c48f1-113">O **MAPIUID** apontado pelo parâmetro  _lpUID_ não foi reconhecido.</span><span class="sxs-lookup"><span data-stu-id="c48f1-113">The **MAPIUID** pointed to by the  _lpUID_ parameter was not recognized.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c48f1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c48f1-114">Remarks</span></span>

<span data-ttu-id="c48f1-115">O **método IProviderAdmin::D eleteProvider** exclui um provedor de serviços do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c48f1-115">The **IProviderAdmin::DeleteProvider** method deletes a service provider from the message service.</span></span> <span data-ttu-id="c48f1-116">**DeleteProvider** determina o provedor de serviços a ser excluído correspondendo a estrutura **MAPIUID** apontada por  _lpUID_ com o conjunto de identificadores registrados pelos provedores de serviços ativos.</span><span class="sxs-lookup"><span data-stu-id="c48f1-116">**DeleteProvider** determines the service provider to delete by matching the **MAPIUID** structure pointed to by  _lpUID_ with the set of identifiers registered by the active service providers.</span></span> 
  
<span data-ttu-id="c48f1-117">A maioria dos serviços de mensagens não permite que provedores sejam excluídos enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="c48f1-117">Most message services do not allow providers to be deleted while the profile is in use.</span></span> <span data-ttu-id="c48f1-118">Se o provedor a ser excluído estiver em uso, **DeleteProvider** marca-o para exclusão em vez de removê-lo imediatamente e retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="c48f1-118">If the provider to delete is in use, **DeleteProvider** marks it for deletion instead of removing it immediately and returns S_OK.</span></span> <span data-ttu-id="c48f1-119">Quando o provedor não está mais sendo usado, ele é excluído.</span><span class="sxs-lookup"><span data-stu-id="c48f1-119">When the provider is no longer being used, it is deleted.</span></span> 
  
 <span data-ttu-id="c48f1-120">**DeleteProvider** chama a função de ponto de entrada do serviço de mensagens antes que o provedor seja removido do serviço.</span><span class="sxs-lookup"><span data-stu-id="c48f1-120">**DeleteProvider** calls the message service's entry point function before the provider is removed from the service.</span></span> <span data-ttu-id="c48f1-121">O  _parâmetro ulContext_ é definido como MSG_SERVICE_PROVIDER_DELETE.</span><span class="sxs-lookup"><span data-stu-id="c48f1-121">The  _ulContext_ parameter is set to MSG_SERVICE_PROVIDER_DELETE.</span></span> <span data-ttu-id="c48f1-122">A função de ponto de entrada do serviço de mensagens executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c48f1-122">The message service entry point function performs the following tasks:</span></span> 
  
- <span data-ttu-id="c48f1-123">Exclui o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="c48f1-123">Deletes the service provider.</span></span>
    
- <span data-ttu-id="c48f1-124">Exclui a seção de perfil do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="c48f1-124">Deletes the service provider's profile section.</span></span>
    
<span data-ttu-id="c48f1-125">A função de ponto de entrada do serviço de mensagens não é chamada novamente depois que o provedor é excluído.</span><span class="sxs-lookup"><span data-stu-id="c48f1-125">The message service entry point function is not called again after the provider has been deleted.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c48f1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c48f1-126">See also</span></span>



[<span data-ttu-id="c48f1-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c48f1-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c48f1-128">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c48f1-128">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c48f1-129">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c48f1-129">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

