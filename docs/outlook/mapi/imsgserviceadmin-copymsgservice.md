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
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="31760-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="31760-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="31760-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31760-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31760-105">Copia um serviço de mensagens para um perfil.</span><span class="sxs-lookup"><span data-stu-id="31760-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="31760-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31760-106">Parameters</span></span>

 <span data-ttu-id="31760-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="31760-107">_lpUID_</span></span>
  
> <span data-ttu-id="31760-108">[in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagens a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="31760-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="31760-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="31760-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="31760-110">[in] Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="31760-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="31760-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="31760-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="31760-112">[in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a seção de perfil do serviço de mensagens a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="31760-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="31760-113">Passar resultados NULL na interface da seção de perfil padrão, [IProfSect](iprofsectimapiprop.md), sendo usado.</span><span class="sxs-lookup"><span data-stu-id="31760-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="31760-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="31760-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="31760-115">[in] Um ponteiro para a IID que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpObjectDst._</span><span class="sxs-lookup"><span data-stu-id="31760-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="31760-116">Passar resultados NULL na interface de sessão, [IMAPISession](imapisessioniunknown.md), sendo usado.</span><span class="sxs-lookup"><span data-stu-id="31760-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="31760-117">O  _parâmetro lpInterfaceDst_ também pode ser definido como IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="31760-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="31760-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="31760-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="31760-119">[in] Um ponteiro para um ponteiro para um objeto de administração de serviço de mensagens ou sessão.</span><span class="sxs-lookup"><span data-stu-id="31760-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="31760-120">O tipo de objeto deve corresponder ao identificador de interface passado  _em lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="31760-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="31760-121">Ponteiros de objeto válidos são LPMAPISESSION e LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="31760-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="31760-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="31760-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="31760-123">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="31760-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="31760-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31760-124">_ulFlags_</span></span>
  
> <span data-ttu-id="31760-125">[in] Uma máscara de bits de sinalizadores que controla como o serviço de mensagens é copiado.</span><span class="sxs-lookup"><span data-stu-id="31760-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="31760-126">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="31760-126">The following flags can be set:</span></span>
    
<span data-ttu-id="31760-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="31760-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="31760-128">Solicita que o serviço de mensagens sempre exibe uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="31760-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31760-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="31760-129">Return value</span></span>

<span data-ttu-id="31760-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="31760-130">S_OK</span></span> 
  
> <span data-ttu-id="31760-131">O serviço de mensagens foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="31760-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="31760-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="31760-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="31760-133">O serviço de mensagens já está no perfil e não permite várias instâncias de si mesmo.</span><span class="sxs-lookup"><span data-stu-id="31760-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="31760-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="31760-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="31760-135">O **MAPIUID** apontado por  _lpUID_ não se refere a um serviço de mensagens existente.</span><span class="sxs-lookup"><span data-stu-id="31760-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31760-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="31760-136">Remarks</span></span>

<span data-ttu-id="31760-137">O **método IMsgServiceAdmin::CopyMsgService** copia um serviço de mensagens para um perfil, seja o perfil ativo ou outro perfil.</span><span class="sxs-lookup"><span data-stu-id="31760-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="31760-138">O perfil que contém o serviço de mensagens a ser copiado e o destino não precisa ser o mesmo perfil, mas pode ser.</span><span class="sxs-lookup"><span data-stu-id="31760-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="31760-139">A função de ponto de entrada do serviço de mensagens não é chamada para uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="31760-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="31760-140">O serviço de mensagens copiado tem as mesmas definições de configuração que o original.</span><span class="sxs-lookup"><span data-stu-id="31760-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="31760-141">Para alterar essas configurações, um cliente deve chamar o [método IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="31760-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31760-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="31760-142">See also</span></span>



[<span data-ttu-id="31760-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="31760-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="31760-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="31760-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="31760-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31760-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

