---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422079"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="94d30-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="94d30-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="94d30-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94d30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94d30-105">Fornece acesso a um objeto de administração de serviço de mensagens para fazer alterações nos serviços de mensagens em um perfil.</span><span class="sxs-lookup"><span data-stu-id="94d30-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="94d30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94d30-106">Parameters</span></span>

 <span data-ttu-id="94d30-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="94d30-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="94d30-108">no Um ponteiro para o nome do perfil a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="94d30-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="94d30-109">O parâmetro _lpszProfileName_ não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="94d30-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="94d30-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="94d30-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="94d30-111">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="94d30-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="94d30-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="94d30-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="94d30-113">no Um identificador da janela pai para quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="94d30-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="94d30-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94d30-114">_ulFlags_</span></span>
  
> <span data-ttu-id="94d30-115">no Uma bitmask de sinalizadores que controla a recuperação do objeto de administração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="94d30-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="94d30-116">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="94d30-116">The following flags can be set:</span></span>
    
<span data-ttu-id="94d30-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="94d30-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="94d30-118">Permite a exibição de uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="94d30-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="94d30-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="94d30-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="94d30-120">O nome do perfil está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="94d30-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="94d30-121">Se o sinalizador MAPI_UNICODE não estiver definido, o nome estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="94d30-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="94d30-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="94d30-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="94d30-123">bota Um ponteiro para um ponteiro para um objeto de administração de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="94d30-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="94d30-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="94d30-124">Return value</span></span>

<span data-ttu-id="94d30-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="94d30-125">S_OK</span></span> 
  
> <span data-ttu-id="94d30-126">O objeto de administração do serviço de mensagens foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="94d30-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="94d30-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="94d30-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="94d30-128">O perfil especificado não existe ou a senha estava errada e uma caixa de diálogo não pôde ser exibida para o usuário solicitar a senha correta porque o MAPI_DIALOG não foi definido no _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="94d30-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="94d30-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="94d30-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="94d30-130">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="94d30-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="94d30-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="94d30-131">Remarks</span></span>

<span data-ttu-id="94d30-132">O método **IProfAdmin:: adminservices** fornece acesso a um objeto de administração do serviço de mensagens para fazer alterações de configuração nos serviços de mensagens em um perfil.</span><span class="sxs-lookup"><span data-stu-id="94d30-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="94d30-133">O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma sequência de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="94d30-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="94d30-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="94d30-134">Notes to callers</span></span>

<span data-ttu-id="94d30-135">Embora você possa recuperar um ponteiro do [IMsgServiceAdmin](imsgserviceadminiunknown.md) chamando esse método ou [IMAPISession:: adminservices](imapisession-adminservices.md), Call **IProfAdmin:: adminservices** se você tiver estritamente um cliente de configuração e não oferecer recursos de mensagens.</span><span class="sxs-lookup"><span data-stu-id="94d30-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="94d30-136">**IProfAdmin:: adminservices** não cria um objeto Session e não carrega nenhum provedor de serviços, o que melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="94d30-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="94d30-137">Você não pode usar **IProfAdmin:: admins** para criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="94d30-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="94d30-138">Portanto, você deve especificar um perfil válido existente no _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="94d30-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="94d30-139">Se o perfil especificado não existir, **IProfAdmin:: adminservices** retornará MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="94d30-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="94d30-140">O nome do perfil pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="94d30-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="94d30-141">Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="94d30-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="94d30-142">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="94d30-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="94d30-143">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="94d30-143">MFCMAPI reference</span></span>

<span data-ttu-id="94d30-144">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="94d30-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="94d30-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="94d30-145">**File**</span></span>|<span data-ttu-id="94d30-146">**Função**</span><span class="sxs-lookup"><span data-stu-id="94d30-146">**Function**</span></span>|<span data-ttu-id="94d30-147">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="94d30-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="94d30-148">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="94d30-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="94d30-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="94d30-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="94d30-150">MFCMAPI usa o método **IProfAdmin:: adminservices** para abrir um objeto de administração de serviço de mensagens para o perfil selecionado para adicionar serviços.</span><span class="sxs-lookup"><span data-stu-id="94d30-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94d30-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="94d30-151">See also</span></span>



[<span data-ttu-id="94d30-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="94d30-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="94d30-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94d30-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="94d30-154">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="94d30-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

