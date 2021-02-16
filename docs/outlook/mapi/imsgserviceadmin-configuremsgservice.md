---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422184"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="9cc9f-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="9cc9f-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="9cc9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cc9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cc9f-105">Reconfigura um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="9cc9f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cc9f-106">Parameters</span></span>

 <span data-ttu-id="9cc9f-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="9cc9f-107">_lpUID_</span></span>
  
> <span data-ttu-id="9cc9f-108">[in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagens configurar.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="9cc9f-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9cc9f-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="9cc9f-110">[in] Um alça para a janela pai da folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="9cc9f-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9cc9f-111">_ulFlags_</span></span>
  
> <span data-ttu-id="9cc9f-112">[in] Uma máscara de bits de sinalizadores que controla a exibição da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="9cc9f-113">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="9cc9f-113">The following flags can be set:</span></span>
    
<span data-ttu-id="9cc9f-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9cc9f-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9cc9f-115">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9cc9f-116">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="9cc9f-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="9cc9f-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="9cc9f-118">O serviço de mensagens deve exibir sua folha de propriedades de configuração, mas não permitir que o usuário a altere.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="9cc9f-119">A maioria dos serviços de mensagens ignora esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="9cc9f-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="9cc9f-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="9cc9f-121">O serviço de mensagens deve exibir sua folha de propriedades de configuração somente se o serviço não estiver completamente configurado.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="9cc9f-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="9cc9f-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="9cc9f-123">O serviço de mensagens deve sempre exibir sua folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="9cc9f-124">Se SERVICE_UI_ALWAYS não estiver definida, uma folha de propriedades de configuração ainda poderá ser exibida se SERVICE_UI_ALLOWED estiver definida e as informações de configuração válidas não estarão disponíveis na matriz de valores de propriedade no parâmetro _lpProps._</span><span class="sxs-lookup"><span data-stu-id="9cc9f-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="9cc9f-125">As SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS devem ser definidas para que uma folha de propriedades seja exibida.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="9cc9f-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="9cc9f-126">_cValues_</span></span>
  
> <span data-ttu-id="9cc9f-127">[in] A contagem de valores de propriedade [na estrutura SPropValue](spropvalue.md) apontado por  _lpProps_.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="9cc9f-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="9cc9f-128">_lpProps_</span></span>
  
> <span data-ttu-id="9cc9f-129">[in] Um ponteiro para uma matriz de valores de propriedade que descrevem as propriedades a exibir na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="9cc9f-130">O  _parâmetro lpProps_ não deve ser NULL se o serviço de mensagens deve ser configurado sem uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9cc9f-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9cc9f-131">Return value</span></span>

<span data-ttu-id="9cc9f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="9cc9f-132">S_OK</span></span> 
  
> <span data-ttu-id="9cc9f-133">O serviço de mensagens foi configurado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="9cc9f-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="9cc9f-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="9cc9f-135">Um erro específico de um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-135">An error specific to a message service.</span></span> <span data-ttu-id="9cc9f-136">Para obter a [estrutura MAPIERROR](mapierror.md) que descreve o erro, o aplicativo cliente deve chamar o método [IMsgServiceAdmin::GetLastError.](imsgserviceadmin-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="9cc9f-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="9cc9f-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9cc9f-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9cc9f-138">O **MAPIUID** apontado por  _lpUID_ não é igual ao de um serviço de mensagens existente.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="9cc9f-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="9cc9f-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="9cc9f-140">O serviço de mensagens não tem uma função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="9cc9f-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9cc9f-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9cc9f-142">O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9cc9f-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cc9f-143">Remarks</span></span>

<span data-ttu-id="9cc9f-144">O **método IMsgServiceAdmin::ConfigureMsgService** permite que um serviço de mensagens seja configurado, com ou sem uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="9cc9f-145">Para permitir a configuração sem uma exibição de folha de propriedades, os serviços de mensagens normalmente preparam um arquivo de header que inclui constantes para todas as propriedades necessárias e opcionais e seus valores.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9cc9f-146">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9cc9f-146">Notes to callers</span></span>

<span data-ttu-id="9cc9f-147">Para recuperar a estrutura **MAPIUID** do serviço de mensagens a ser configurada, recupere a coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagens na tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="9cc9f-148">Para obter mais informações, consulte o procedimento descrito no [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="9cc9f-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="9cc9f-149">Você pode configurar um serviço de mensagens sem exibir uma folha de propriedades para um usuário somente se tiver informações antecipadas sobre os valores de propriedade a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="9cc9f-150">Se você estiver configurando um serviço de mensagem sem exibir uma folha de propriedades, passe valores de propriedade válidos no parâmetro  _lpProps_ e não de definir os sinalizadores MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="9cc9f-151">Se você receber todas ou algumas das informações de configuração do usuário por meio de uma folha de propriedades, defina SERVICE_UI_ALLOWED em  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="9cc9f-152">Se você usar informações de propriedade existentes apenas para estabelecer configurações padrão e o usuário for capaz de alterar as configurações, defina SERVICE_UI_ALWAYS  _em ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9cc9f-153">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9cc9f-153">MFCMAPI reference</span></span>

<span data-ttu-id="9cc9f-154">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9cc9f-155">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9cc9f-155">**File**</span></span>|<span data-ttu-id="9cc9f-156">**Função**</span><span class="sxs-lookup"><span data-stu-id="9cc9f-156">**Function**</span></span>|<span data-ttu-id="9cc9f-157">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="9cc9f-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9cc9f-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="9cc9f-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9cc9f-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="9cc9f-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="9cc9f-160">MFCMAPI usa o **método IMsgServiceAdmin::ConfigureMsgService** para configurar um serviço que foi adicionado a um perfil.</span><span class="sxs-lookup"><span data-stu-id="9cc9f-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cc9f-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cc9f-161">See also</span></span>



[<span data-ttu-id="9cc9f-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9cc9f-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9cc9f-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="9cc9f-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="9cc9f-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9cc9f-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="9cc9f-165">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9cc9f-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

