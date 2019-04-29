---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432118"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="d2c32-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="d2c32-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="d2c32-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2c32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2c32-105">Copia um serviço de mensagens em um perfil.</span><span class="sxs-lookup"><span data-stu-id="d2c32-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d2c32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2c32-106">Parameters</span></span>

 <span data-ttu-id="d2c32-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d2c32-107">_lpUID_</span></span>
  
> <span data-ttu-id="d2c32-108">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="d2c32-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="d2c32-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="d2c32-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="d2c32-110">no Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="d2c32-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="d2c32-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="d2c32-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="d2c32-112">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil do serviço de mensagens a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="d2c32-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="d2c32-113">Passar resultados nulos na interface de seção de perfil padrão, [IProfSect](iprofsectimapiprop.md), que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="d2c32-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="d2c32-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="d2c32-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="d2c32-115">no Um ponteiro para o IID que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpObjectDst_ .</span><span class="sxs-lookup"><span data-stu-id="d2c32-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="d2c32-116">Passar resultados nulos na interface de sessão, [IMAPISession](imapisessioniunknown.md), sendo usado.</span><span class="sxs-lookup"><span data-stu-id="d2c32-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="d2c32-117">O parâmetro _lpInterfaceDst_ também pode ser definido como IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="d2c32-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="d2c32-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="d2c32-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="d2c32-119">no Um ponteiro para um ponteiro para um objeto de administração de sessão ou serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d2c32-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="d2c32-120">O tipo de objeto deve corresponder ao identificador de interface passado no _lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="d2c32-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="d2c32-121">Os ponteiros de objeto válidos são LPMAPISESSION e LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="d2c32-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="d2c32-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d2c32-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="d2c32-123">no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.</span><span class="sxs-lookup"><span data-stu-id="d2c32-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="d2c32-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2c32-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d2c32-125">no Uma bitmask de sinalizadores que controla como o serviço de mensagens é copiado.</span><span class="sxs-lookup"><span data-stu-id="d2c32-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="d2c32-126">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="d2c32-126">The following flags can be set:</span></span>
    
<span data-ttu-id="d2c32-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="d2c32-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="d2c32-128">Solicita que o serviço de mensagens sempre exiba uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="d2c32-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2c32-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d2c32-129">Return value</span></span>

<span data-ttu-id="d2c32-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2c32-130">S_OK</span></span> 
  
> <span data-ttu-id="d2c32-131">O serviço de mensagens foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d2c32-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="d2c32-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d2c32-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d2c32-133">O serviço de mensagens já está no perfil e não permite várias instâncias de si mesmo.</span><span class="sxs-lookup"><span data-stu-id="d2c32-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="d2c32-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d2c32-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d2c32-135">O **MAPIUID** apontado por _lpUID_ não se refere a um serviço de mensagens existente.</span><span class="sxs-lookup"><span data-stu-id="d2c32-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d2c32-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2c32-136">Remarks</span></span>

<span data-ttu-id="d2c32-137">O método **IMsgServiceAdmin:: CopyMsgService** copia um serviço de mensagem em um perfil, seja o perfil ativo ou outro perfil.</span><span class="sxs-lookup"><span data-stu-id="d2c32-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="d2c32-138">O perfil que contém o serviço de mensagens a ser copiado e o destino não precisam ser o mesmo perfil, mas podem ser.</span><span class="sxs-lookup"><span data-stu-id="d2c32-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="d2c32-139">A função de ponto de entrada do serviço de mensagens não é chamada para uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="d2c32-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="d2c32-140">O serviço de mensagens copiadas tem as mesmas definições de configuração que o original.</span><span class="sxs-lookup"><span data-stu-id="d2c32-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="d2c32-141">Para alterar essas configurações, um cliente deve chamar o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d2c32-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2c32-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2c32-142">See also</span></span>



[<span data-ttu-id="d2c32-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="d2c32-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="d2c32-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d2c32-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d2c32-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2c32-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

