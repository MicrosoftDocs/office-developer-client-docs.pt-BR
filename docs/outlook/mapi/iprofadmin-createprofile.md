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
ms.openlocfilehash: 92d5dcdf3e5e3fbdb7490d777a24976c9ae4af1a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582788"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="4d581-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="4d581-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="4d581-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d581-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d581-105">Cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="4d581-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4d581-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d581-106">Parameters</span></span>

 <span data-ttu-id="4d581-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="4d581-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="4d581-108">[in] Um ponteiro para o nome do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="4d581-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="4d581-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="4d581-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="4d581-110">[in] Um ponteiro para a senha do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="4d581-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="4d581-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4d581-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="4d581-112">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="4d581-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="4d581-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d581-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4d581-114">[in] Uma bitmask dos sinalizadores que controla como o perfil é criado.</span><span class="sxs-lookup"><span data-stu-id="4d581-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="4d581-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="4d581-115">The following flags can be set:</span></span>
    
<span data-ttu-id="4d581-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="4d581-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="4d581-117">MAPI deve preencher o novo perfil com os serviços de mensagem que estão incluídos na seção [padrão Services] do arquivo Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="4d581-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="4d581-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4d581-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4d581-119">Podem ser exibidas as folhas de propriedades de configuração de cada um dos provedores nos serviços de mensagem a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="4d581-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d581-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4d581-120">Return value</span></span>

<span data-ttu-id="4d581-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d581-121">S_OK</span></span> 
  
> <span data-ttu-id="4d581-122">O novo perfil foi criado.</span><span class="sxs-lookup"><span data-stu-id="4d581-122">The new profile was created.</span></span>
    
<span data-ttu-id="4d581-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4d581-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4d581-124">O novo perfil especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="4d581-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d581-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d581-125">Remarks</span></span>

<span data-ttu-id="4d581-126">O método **IProfAdmin::CreateProfile** cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="4d581-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d581-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="4d581-127">Notes to callers</span></span>

<span data-ttu-id="4d581-128">Você pode chamar **CreateProfile** no momento da instalação de aplicativos ou a qualquer momento durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="4d581-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="4d581-129">Quando esse método é chamado no momento da instalação, muitas das definições de configuração provenientes do arquivo de configuração Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="4d581-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="4d581-130">Quando esse método é chamado durante uma sessão ativa, as configurações são provenientes de usuário que será solicitado por uma série de folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4d581-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="4d581-131">Se o sinalizador MAPI_DEFAULT_SERVICES é definido no parâmetro _ulFlags_ , **CreateProfile** chama a função de ponto de entrada de serviço de mensagem para cada serviço de mensagem na seção [padrão Services] no arquivo Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="4d581-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="4d581-132">Cada função de ponto de entrada de serviço de mensagem é chamada com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="4d581-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="4d581-133">Se flags MAPI_DIALOG tanto o MAPI_DEFAULT_SERVICES estiverem definidas, os valores nos parâmetros _ulUIParam_ e _ulFlags_ também são passados para a função de ponto de entrada de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d581-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="4d581-134">As funções de ponto de entrada de serviço de mensagem são chamadas somente depois que todas as informações disponíveis do arquivo Mapisvc foi adicionadas ao perfil.</span><span class="sxs-lookup"><span data-stu-id="4d581-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="4d581-135">O nome do novo perfil e sua senha pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="4d581-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="4d581-136">Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.</span><span class="sxs-lookup"><span data-stu-id="4d581-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="4d581-137">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="4d581-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="4d581-138">O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="4d581-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d581-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d581-139">See also</span></span>



[<span data-ttu-id="4d581-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="4d581-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="4d581-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="4d581-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="4d581-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="4d581-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="4d581-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d581-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

