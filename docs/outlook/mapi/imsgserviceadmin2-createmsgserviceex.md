---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310007"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="567ad-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="567ad-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="567ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="567ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="567ad-105">Adiciona um serviço de mensagens ao perfil atual e retorna à UID do serviço recém-adicionada.</span><span class="sxs-lookup"><span data-stu-id="567ad-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="567ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="567ad-106">Parameters</span></span>

 <span data-ttu-id="567ad-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="567ad-107">_lpszService_</span></span>
  
> <span data-ttu-id="567ad-108">no Um ponteiro para o nome do serviço de mensagens a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="567ad-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="567ad-109">Esse nome de serviço de mensagem deve aparecer na seção **[serviços]** do arquivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="567ad-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="567ad-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="567ad-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="567ad-111">no Um ponteiro para o nome de exibição do serviço de mensagens a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="567ad-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="567ad-112">O parâmetro _lpszDisplayName_ será ignorado se o serviço de mensagens tiver definido a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) no arquivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="567ad-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="567ad-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="567ad-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="567ad-114">no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.</span><span class="sxs-lookup"><span data-stu-id="567ad-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="567ad-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="567ad-115">_ulFlags_</span></span>
  
> <span data-ttu-id="567ad-116">no Uma bitmask de sinalizadores que controla como o serviço de mensagens é instalado.</span><span class="sxs-lookup"><span data-stu-id="567ad-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="567ad-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="567ad-117">The following flags can be set:</span></span>
    
<span data-ttu-id="567ad-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="567ad-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="567ad-119">Os parâmetros lpszService e lpszDisplayName devem ser convertidos em LPWSTR e interpretados como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="567ad-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="567ad-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="567ad-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="567ad-121">Ao adicionar um novo serviço de mensagens ao perfil, o subsistema MAPI, com base em várias circunstâncias e critérios, geralmente determina que essa ação requer uma reinicialização do Outlook.</span><span class="sxs-lookup"><span data-stu-id="567ad-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="567ad-122">Se o sinalizador SERVICE_NO_RESTART_WARNING não estiver incluído e a interface do usuário for baseada nos sinalizadores SERVICE_UI_ALWAYS e SERVICE_UI_ALLOWED e pelo menos um processo estiver conectado ao perfil atual, essa função exibirá a mensagem "você deve reiniciar o Outlook para que as alterações entrem em vigor. "</span><span class="sxs-lookup"><span data-stu-id="567ad-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="567ad-123">Incluir o sinalizador SERVICE_NO_RESTART_WARNING suprime a exibição dessa mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="567ad-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="567ad-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="567ad-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="567ad-125">A interface do usuário de configuração do serviço de mensagens é permitida se necessário.</span><span class="sxs-lookup"><span data-stu-id="567ad-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="567ad-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="567ad-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="567ad-127">O serviço de mensagens exibe sua folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="567ad-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="567ad-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="567ad-128">_lpuidService_</span></span>
  
> <span data-ttu-id="567ad-129">bota O ponteiro para a UID do serviço de mensagens adicionado.</span><span class="sxs-lookup"><span data-stu-id="567ad-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="567ad-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="567ad-130">Return value</span></span>

<span data-ttu-id="567ad-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="567ad-131">S_OK</span></span>
  
> <span data-ttu-id="567ad-132">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="567ad-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="567ad-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="567ad-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="567ad-134">O nome do serviço de mensagens não está na seção **[serviços]** de MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="567ad-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="567ad-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="567ad-135">Remarks</span></span>

<span data-ttu-id="567ad-136">O método **IMsgServiceAdmin2:: CreateMsgServiceEx** adiciona um serviço de mensagens ao perfil atual.</span><span class="sxs-lookup"><span data-stu-id="567ad-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="567ad-137">**CreateMsgServiceEx** chama a função de ponto de entrada do serviço de mensagens para executar qualquer tarefa de configuração específica do serviço.</span><span class="sxs-lookup"><span data-stu-id="567ad-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="567ad-138">Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ , o serviço de mensagens que estiver sendo instalado poderá exibir uma folha de propriedades, permitindo que o usuário defina suas configurações.</span><span class="sxs-lookup"><span data-stu-id="567ad-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="567ad-139">O arquivo MapiSvc. inf contém a lista de provedores que compõem um serviço de mensagens e as propriedades de cada um.</span><span class="sxs-lookup"><span data-stu-id="567ad-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="567ad-140">**CreateMsgServiceEx** primeiro cria uma nova seção de perfil para o serviço de mensagens e, em seguida, copia Todas as informações desse serviço do arquivo MapiSvc. inf para o perfil, criando novas seções para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="567ad-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="567ad-141">Depois que todas as informações tiverem sido copiadas de MapiSvc. inf, a função de ponto de entrada do serviço de mensagens, **MSGSERVICEENTRY**, será chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="567ad-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="567ad-142">Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ do método **CreateMsgServiceEx** , os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados quando a função de ponto de entrada do serviço de mensagens for chamada.</span><span class="sxs-lookup"><span data-stu-id="567ad-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="567ad-143">Os provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários possam configurar o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="567ad-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="567ad-144">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="567ad-144">Notes to callers</span></span>

<span data-ttu-id="567ad-145">Se o argumento **CreateMsgServiceEx** _LPUIDSERVICE_ não for nulo, a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagem que foi adicionada ao perfil será retornada no **GUID** para o qual ele aponta.</span><span class="sxs-lookup"><span data-stu-id="567ad-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="567ad-146">Passe o valor da propriedade **PR_SERVICE_UID** no parâmetro _lpuidService_ para o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="567ad-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="567ad-147">A implementação do Microsoft Outlook 2010 do subsistema MAPI não oferece suporte ao MAPI_UNICODE e falhará se for usado.</span><span class="sxs-lookup"><span data-stu-id="567ad-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="567ad-148">A interface IMsgServiceAdmin2 é exposta pelo mesmo objeto que implementa a interface IMsgServiceAdmin e está disponível usando a implementação do subsistema MAPI do Outlook desde o Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="567ad-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="567ad-149">Sua IID é definida da seguinte maneira: `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> > o _parâmetroulflags_ SERVICE_NO_RESTART_WARNING pode não estar definido no arquivo de cabeçalho baixável que você tem atualmente e, nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="567ad-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="567ad-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="567ad-150">See also</span></span>



[<span data-ttu-id="567ad-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="567ad-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="567ad-152">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="567ad-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

