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
ms.openlocfilehash: 791dfe094aa0ff1aab656b56fbdf7d59e880b92e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593729"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="81fdc-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="81fdc-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="81fdc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81fdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81fdc-105">Copia um serviço de mensagem para um perfil.</span><span class="sxs-lookup"><span data-stu-id="81fdc-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="81fdc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81fdc-106">Parameters</span></span>

 <span data-ttu-id="81fdc-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="81fdc-107">_lpUID_</span></span>
  
> <span data-ttu-id="81fdc-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo do serviço de mensagem para copiar.</span><span class="sxs-lookup"><span data-stu-id="81fdc-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="81fdc-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="81fdc-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="81fdc-110">[in] Esse parâmetro foi reduzido.</span><span class="sxs-lookup"><span data-stu-id="81fdc-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="81fdc-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="81fdc-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="81fdc-112">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil do serviço de mensagem para copiar.</span><span class="sxs-lookup"><span data-stu-id="81fdc-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="81fdc-113">Passagem nula resulta no perfil padrão seção interface [IProfSect](iprofsectimapiprop.md), que está sendo utilizada.</span><span class="sxs-lookup"><span data-stu-id="81fdc-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="81fdc-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="81fdc-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="81fdc-115">[in] Um ponteiro para a IID que representa a interface que será usada para acessar o objeto apontado pelo parâmetro _lpObjectDst_ .</span><span class="sxs-lookup"><span data-stu-id="81fdc-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="81fdc-116">Passagem nula resulta na interface de sessão, [IMAPISession](imapisessioniunknown.md), sendo usada.</span><span class="sxs-lookup"><span data-stu-id="81fdc-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="81fdc-117">O parâmetro _lpInterfaceDst_ também pode ser definido como IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="81fdc-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="81fdc-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="81fdc-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="81fdc-119">[in] Um ponteiro para um ponteiro para um objeto de administração de serviço de sessão ou mensagem.</span><span class="sxs-lookup"><span data-stu-id="81fdc-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="81fdc-120">O tipo de objeto deve corresponder ao identificador de interface passado em _lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="81fdc-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="81fdc-121">Ponteiros de objeto válido são LPMAPISESSION e LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="81fdc-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="81fdc-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="81fdc-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="81fdc-123">[in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="81fdc-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="81fdc-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81fdc-124">_ulFlags_</span></span>
  
> <span data-ttu-id="81fdc-125">[in] Uma bitmask dos sinalizadores que controla como o serviço de mensagem é copiado.</span><span class="sxs-lookup"><span data-stu-id="81fdc-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="81fdc-126">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="81fdc-126">The following flags can be set:</span></span>
    
<span data-ttu-id="81fdc-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="81fdc-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="81fdc-128">Solicita que o serviço de mensagem sempre exibe uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="81fdc-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81fdc-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81fdc-129">Return value</span></span>

<span data-ttu-id="81fdc-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="81fdc-130">S_OK</span></span> 
  
> <span data-ttu-id="81fdc-131">O serviço de mensagem foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="81fdc-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="81fdc-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="81fdc-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="81fdc-133">O serviço de mensagem já está no perfil e não permitir que várias instâncias de si mesmo.</span><span class="sxs-lookup"><span data-stu-id="81fdc-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="81fdc-134">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="81fdc-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="81fdc-135">**MAPIUID** apontado pela _lpUID_ não faz referência a um serviço de mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="81fdc-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="81fdc-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="81fdc-136">Remarks</span></span>

<span data-ttu-id="81fdc-137">O método **IMsgServiceAdmin::CopyMsgService** copia um serviço de mensagem para um perfil, o perfil ativo ou outro perfil.</span><span class="sxs-lookup"><span data-stu-id="81fdc-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="81fdc-138">O perfil que contém o serviço de mensagem a ser copiado e o destino não precisam ser o mesmo perfil, mas eles podem ser.</span><span class="sxs-lookup"><span data-stu-id="81fdc-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="81fdc-139">Função do ponto de entrada do serviço de mensagem não é chamada para uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="81fdc-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="81fdc-140">O serviço de mensagem copiada tem as mesmas definições de configuração do seu original.</span><span class="sxs-lookup"><span data-stu-id="81fdc-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="81fdc-141">Para alterar essas configurações, um cliente deve chamar o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="81fdc-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81fdc-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="81fdc-142">See also</span></span>



[<span data-ttu-id="81fdc-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="81fdc-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="81fdc-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="81fdc-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="81fdc-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81fdc-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

