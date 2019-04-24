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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317112"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="a158c-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="a158c-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="a158c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a158c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a158c-105">Cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="a158c-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a158c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a158c-106">Parameters</span></span>

 <span data-ttu-id="a158c-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="a158c-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="a158c-108">no Um ponteiro para o nome do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="a158c-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="a158c-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="a158c-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="a158c-110">no Um ponteiro para a senha do novo perfil.</span><span class="sxs-lookup"><span data-stu-id="a158c-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="a158c-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a158c-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="a158c-112">no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="a158c-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a158c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a158c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="a158c-114">no Uma bitmask de sinalizadores que controla como o perfil é criado.</span><span class="sxs-lookup"><span data-stu-id="a158c-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="a158c-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a158c-115">The following flags can be set:</span></span>
    
<span data-ttu-id="a158c-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="a158c-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="a158c-117">O MAPI deve preencher o novo perfil com os serviços de mensagem incluídos na seção [serviços padrão] do arquivo MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="a158c-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="a158c-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a158c-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a158c-119">É possível exibir as folhas de propriedades de configuração de cada um dos provedores nos serviços de mensagens a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="a158c-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a158c-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a158c-120">Return value</span></span>

<span data-ttu-id="a158c-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a158c-121">S_OK</span></span> 
  
> <span data-ttu-id="a158c-122">O novo perfil foi criado.</span><span class="sxs-lookup"><span data-stu-id="a158c-122">The new profile was created.</span></span>
    
<span data-ttu-id="a158c-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a158c-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a158c-124">O novo perfil especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="a158c-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a158c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a158c-125">Remarks</span></span>

<span data-ttu-id="a158c-126">O método **IProfAdmin:: CreateProfile** cria um novo perfil.</span><span class="sxs-lookup"><span data-stu-id="a158c-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a158c-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a158c-127">Notes to callers</span></span>

<span data-ttu-id="a158c-128">Você pode chamar **CreateProfile** no momento da instalação do aplicativo ou a qualquer momento durante uma sessão.</span><span class="sxs-lookup"><span data-stu-id="a158c-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="a158c-129">Quando esse método é chamado no momento da instalação, muitas das definições de configuração são provenientes do arquivo de configuração MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="a158c-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="a158c-130">Quando esse método é chamado durante uma sessão ativa, as configurações são provenientes do usuário que é solicitado através de uma série de folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a158c-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="a158c-131">Se o sinalizador MAPI_DEFAULT_SERVICES estiver definido no parâmetro _parâmetroulflags_ , **CreateProfile** chamará a função de ponto de entrada do serviço de mensagens para cada serviço de mensagens na seção [serviços padrão] no arquivo MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="a158c-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="a158c-132">Cada função de ponto de entrada de serviço de mensagens é chamada com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="a158c-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="a158c-133">Se ambos os sinalizadores MAPI_DIALOG e MAPI_DEFAULT_SERVICES estiverem definidos, os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados para a função de ponto de entrada de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a158c-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="a158c-134">As funções do ponto de entrada do serviço de mensagens são chamadas somente depois que todas as informações disponíveis do arquivo MAPISVC. inf forem adicionadas ao perfil.</span><span class="sxs-lookup"><span data-stu-id="a158c-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="a158c-135">O nome do novo perfil e sua senha podem ter até 64 caracteres de comprimento e podem incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="a158c-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="a158c-136">Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="a158c-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="a158c-137">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="a158c-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="a158c-138">O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma sequência de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="a158c-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a158c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a158c-139">See also</span></span>



[<span data-ttu-id="a158c-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="a158c-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="a158c-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="a158c-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="a158c-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="a158c-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="a158c-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a158c-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

