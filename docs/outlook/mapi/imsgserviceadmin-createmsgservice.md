---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434974"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="f0332-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="f0332-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="f0332-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0332-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0332-105">PreTerido: o uso de [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) é recomendado.</span><span class="sxs-lookup"><span data-stu-id="f0332-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="f0332-106">Adiciona um serviço de mensagens ao perfil atual.</span><span class="sxs-lookup"><span data-stu-id="f0332-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="f0332-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0332-107">Parameters</span></span>

 <span data-ttu-id="f0332-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="f0332-108">_lpszService_</span></span>
  
> <span data-ttu-id="f0332-109">no Um ponteiro para o nome do serviço de mensagens a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="f0332-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="f0332-110">Esse nome de serviço de mensagem deve aparecer na seção **[serviços]** do arquivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="f0332-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="f0332-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="f0332-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="f0332-112">no Um ponteiro para o nome de exibição do serviço de mensagens a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="f0332-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="f0332-113">O parâmetro _lpszDisplayName_ será ignorado se o serviço de mensagens tiver definido a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) no arquivo MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="f0332-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="f0332-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f0332-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="f0332-115">no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.</span><span class="sxs-lookup"><span data-stu-id="f0332-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="f0332-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0332-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f0332-117">no Uma bitmask de sinalizadores que controla como o serviço de mensagens é instalado.</span><span class="sxs-lookup"><span data-stu-id="f0332-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="f0332-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f0332-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f0332-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0332-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f0332-120">Os parâmetros lpszService e lpszDisplayName devem ser convertidos em LPWSTR e interpretados como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0332-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="f0332-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="f0332-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="f0332-122">Ao adicionar um novo serviço de mensagens ao perfil, o subsistema MAPI, com base em várias circunstâncias e critérios, geralmente determina que essa ação requer uma reinicialização do Outlook.</span><span class="sxs-lookup"><span data-stu-id="f0332-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="f0332-123">Se o sinalizador SERVICE_NO_RESTART_WARNING não estiver incluído e a interface do usuário for baseada nos sinalizadores SERVICE_UI_ALWAYS e SERVICE_UI_ALLOWED e pelo menos um processo estiver conectado ao perfil atual, essa função exibirá a mensagem "você deve reiniciar o Outlook para que as alterações entrem em vigor. "</span><span class="sxs-lookup"><span data-stu-id="f0332-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="f0332-124">Incluir o sinalizador SERVICE_NO_RESTART_WARNING suprime a exibição dessa mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="f0332-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="f0332-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="f0332-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="f0332-126">A interface do usuário de configuração do serviço de mensagens é permitida se necessário.</span><span class="sxs-lookup"><span data-stu-id="f0332-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="f0332-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="f0332-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="f0332-128">O serviço de mensagens exibe sua folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="f0332-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0332-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f0332-129">Return value</span></span>

<span data-ttu-id="f0332-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0332-130">S_OK</span></span> 
  
> <span data-ttu-id="f0332-131">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f0332-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f0332-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f0332-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f0332-133">O nome do serviço de mensagens não está na seção **[serviços]** de MapiSvc. inf.</span><span class="sxs-lookup"><span data-stu-id="f0332-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f0332-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0332-134">Remarks</span></span>

<span data-ttu-id="f0332-135">O método **IMsgServiceAdmin:: CreateMsgService** adiciona um serviço de mensagens ao perfil atual.</span><span class="sxs-lookup"><span data-stu-id="f0332-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="f0332-136">**CreateMsgService** chama a função de ponto de entrada do serviço de mensagens para executar qualquer tarefa de configuração específica do serviço.</span><span class="sxs-lookup"><span data-stu-id="f0332-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="f0332-137">Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ , o serviço de mensagens que estiver sendo instalado poderá exibir uma folha de propriedades para permitir que o usuário defina suas configurações.</span><span class="sxs-lookup"><span data-stu-id="f0332-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="f0332-138">O arquivo MapiSvc. inf contém a lista de provedores que compõem um serviço de mensagens e as propriedades de cada um.</span><span class="sxs-lookup"><span data-stu-id="f0332-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="f0332-139">**CreateMsgService** primeiro cria uma nova seção de perfil para o serviço de mensagens e, em seguida, copia Todas as informações desse serviço do arquivo MapiSvc. inf para o perfil, criando novas seções para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="f0332-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="f0332-140">Após todas as informações terem sido copiadas de MapiSvc. inf, a função de ponto de entrada do serviço de mensagens é chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="f0332-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="f0332-141">Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ do método **CreateMsgService** , os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados quando a função de ponto de entrada do serviço de mensagens for chamada.</span><span class="sxs-lookup"><span data-stu-id="f0332-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="f0332-142">Os provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários possam configurar o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f0332-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f0332-143">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f0332-143">Notes to callers</span></span>

 <span data-ttu-id="f0332-144">**CreateMsgService** não retorna a estrutura [MAPIUID](mapiuid.md) para o serviço de mensagem que foi adicionado ao perfil.</span><span class="sxs-lookup"><span data-stu-id="f0332-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="f0332-145">Para recuperar o **MAPIUID** do serviço de mensagens criadas, use o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="f0332-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="f0332-146">Chame o método [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obter a tabela de administração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f0332-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="f0332-147">Localize a linha que representa o serviço de mensagem, colocando uma restrição na tabela que corresponde à propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) com o nome do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f0332-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="f0332-148">Recupere a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço.</span><span class="sxs-lookup"><span data-stu-id="f0332-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="f0332-149">Passe o valor da propriedade **PR_SERVICE_UID** no parâmetro _lpUid_ para o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço.</span><span class="sxs-lookup"><span data-stu-id="f0332-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="f0332-150">A implementação do Microsoft Outlook 2010 do subsistema MAPI não oferece suporte ao MAPI_UNICODE e falhará se for usado.</span><span class="sxs-lookup"><span data-stu-id="f0332-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f0332-151">O _parâmetroulflags_ SERVICE_NO_RESTART_WARNING pode não estar definido no arquivo de cabeçalho baixável que você tem atualmente, e, nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="f0332-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f0332-152">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f0332-152">MFCMAPI reference</span></span>

<span data-ttu-id="f0332-153">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0332-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f0332-154">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f0332-154">**File**</span></span>|<span data-ttu-id="f0332-155">**Função**</span><span class="sxs-lookup"><span data-stu-id="f0332-155">**Function**</span></span>|<span data-ttu-id="f0332-156">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f0332-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0332-157">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f0332-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f0332-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="f0332-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="f0332-159">MFCMAPI usa o método **IMsgServiceAdmin:: CreateMsgService** para adicionar um serviço a um perfil.</span><span class="sxs-lookup"><span data-stu-id="f0332-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0332-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0332-160">See also</span></span>



[<span data-ttu-id="f0332-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0332-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="f0332-162">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f0332-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

