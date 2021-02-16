---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404397"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="c8b13-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="c8b13-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="c8b13-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8b13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8b13-105">Cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="c8b13-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c8b13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8b13-106">Parameters</span></span>

 <span data-ttu-id="c8b13-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="c8b13-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="c8b13-108">[in] Um ponteiro para o nome do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="c8b13-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="c8b13-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="c8b13-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="c8b13-110">[in] Um ponteiro para a senha do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="c8b13-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="c8b13-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c8b13-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="c8b13-112">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="c8b13-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="c8b13-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8b13-113">_ulFlags_</span></span>
  
> <span data-ttu-id="c8b13-114">[in] Uma máscara de bits de sinalizadores que controla como o perfil é criado.</span><span class="sxs-lookup"><span data-stu-id="c8b13-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="c8b13-115">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c8b13-115">The following flags can be set:</span></span>
    
<span data-ttu-id="c8b13-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="c8b13-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="c8b13-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span><span class="sxs-lookup"><span data-stu-id="c8b13-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="c8b13-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c8b13-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="c8b13-119">As folhas de propriedades de configuração de cada um dos provedores nos serviços de mensagem a serem adicionados podem ser exibidas.</span><span class="sxs-lookup"><span data-stu-id="c8b13-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8b13-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c8b13-120">Return value</span></span>

<span data-ttu-id="c8b13-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8b13-121">S_OK</span></span> 
  
> <span data-ttu-id="c8b13-122">O novo perfil foi criado.</span><span class="sxs-lookup"><span data-stu-id="c8b13-122">The new profile was created.</span></span>
    
<span data-ttu-id="c8b13-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c8b13-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c8b13-124">O novo perfil especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="c8b13-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8b13-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8b13-125">Remarks</span></span>

<span data-ttu-id="c8b13-126">O **método IProfAdmin::CreateProfile** cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="c8b13-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8b13-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="c8b13-127">Notes to callers</span></span>

<span data-ttu-id="c8b13-128">Você pode chamar **CreateProfile no** momento da instalação do aplicativo ou a qualquer momento durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="c8b13-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="c8b13-129">Quando esse método é chamado no momento da instalação, muitas das definições de configuração vêm do arquivo de configuração Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="c8b13-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="c8b13-130">Quando esse método é chamado durante uma sessão ativa, as configurações vêm do usuário que é solicitado por meio de uma série de folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c8b13-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="c8b13-131">Se o sinalizador MAPI_DEFAULT_SERVICES for definido no parâmetro  _ulFlags,_ **CreateProfile** chamará a função de ponto de entrada do serviço de mensagens para cada serviço de mensagem na seção [Serviços Padrão] no arquivo Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="c8b13-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="c8b13-132">Cada função de ponto de entrada do serviço de mensagens é chamada com o  _parâmetro ulContext_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="c8b13-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="c8b13-133">Se os sinalizadores MAPI_DIALOG e MAPI_DEFAULT_SERVICES da mensagem estão definidos, os valores nos parâmetros  _ulUIParam_ e  _ulFlags_ também são passados para a função de ponto de entrada do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c8b13-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="c8b13-134">As funções de ponto de entrada do serviço de mensagens são chamadas somente depois que todas as informações disponíveis do arquivo Mapisvc.inf foram adicionadas ao perfil.</span><span class="sxs-lookup"><span data-stu-id="c8b13-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="c8b13-135">O nome do novo perfil e sua senha podem ter até 64 caracteres e podem incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="c8b13-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="c8b13-136">Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="c8b13-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="c8b13-137">Espaços incorporados, mas não espaços à frente ou à frente.</span><span class="sxs-lookup"><span data-stu-id="c8b13-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="c8b13-138">O  _parâmetro lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="c8b13-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8b13-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8b13-139">See also</span></span>



[<span data-ttu-id="c8b13-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="c8b13-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="c8b13-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="c8b13-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="c8b13-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c8b13-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c8b13-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8b13-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

