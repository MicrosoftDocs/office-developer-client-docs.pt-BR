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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7566bb075c2ef9903b5a376fd90f209c8683c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767626"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="102d6-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="102d6-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="102d6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="102d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="102d6-105">Fornece acesso a um objeto de administração do serviço de mensagem para aplicar alterações para os serviços de mensagem em um perfil.</span><span class="sxs-lookup"><span data-stu-id="102d6-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="102d6-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="102d6-106">Parameters</span></span>

 <span data-ttu-id="102d6-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="102d6-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="102d6-108">[in] Um ponteiro para o nome do perfil a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="102d6-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="102d6-109">O parâmetro _lpszProfileName_ não deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="102d6-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="102d6-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="102d6-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="102d6-111">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="102d6-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="102d6-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="102d6-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="102d6-113">[in] Uma alça da janela pai para todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="102d6-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="102d6-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="102d6-114">_ulFlags_</span></span>
  
> <span data-ttu-id="102d6-115">[in] Uma bitmask dos sinalizadores que controla a recuperação do objeto de administração do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="102d6-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="102d6-116">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="102d6-116">The following flags can be set:</span></span>
    
<span data-ttu-id="102d6-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="102d6-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="102d6-118">Habilita a exibição de uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="102d6-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="102d6-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="102d6-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="102d6-120">O nome do perfil está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="102d6-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="102d6-121">Se o sinalizador MAPI_UNICODE não estiver definido, o nome é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="102d6-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="102d6-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="102d6-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="102d6-123">[out] Um ponteiro para um ponteiro para um objeto de administração do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="102d6-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="102d6-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="102d6-124">Return value</span></span>

<span data-ttu-id="102d6-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="102d6-125">S_OK</span></span> 
  
> <span data-ttu-id="102d6-126">O objeto de administração do serviço de mensagem foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="102d6-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="102d6-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="102d6-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="102d6-128">O perfil especificado não existe, ou a senha estava errada e uma caixa de diálogo não pôde ser exibida ao usuário para solicitar a senha correta porque MAPI_DIALOG não foi definido em _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="102d6-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="102d6-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="102d6-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="102d6-130">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="102d6-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="102d6-131">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="102d6-131">Remarks</span></span>

<span data-ttu-id="102d6-132">O método **IProfAdmin::AdminServices** fornece acesso a um objeto de administração do serviço de mensagem para as alterações de configuração a mensagem serviços em um perfil.</span><span class="sxs-lookup"><span data-stu-id="102d6-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="102d6-133">O parâmetro _lpszPassword_ deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="102d6-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="102d6-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="102d6-134">Notes to callers</span></span>

<span data-ttu-id="102d6-135">Embora você possa recuperar um ponteiro [IMsgServiceAdmin](imsgserviceadminiunknown.md) chamando este método ou o [IMAPISession::AdminServices](imapisession-adminservices.md), chame **IProfAdmin::AdminServices** se você tiver estritamente um cliente de configuração e oferece sem recursos de mensagens.</span><span class="sxs-lookup"><span data-stu-id="102d6-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="102d6-136">**IProfAdmin::AdminServices** não cria um objeto de sessão e não carregar quaisquer provedores de serviço, que melhora o desempenho.</span><span class="sxs-lookup"><span data-stu-id="102d6-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="102d6-137">Você não pode usar **IProfAdmin::AdminServices** para criar um perfil.</span><span class="sxs-lookup"><span data-stu-id="102d6-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="102d6-138">Portanto, você deve especificar um perfil de válido existente no _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="102d6-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="102d6-139">Se o perfil especificado não existir, o **IProfAdmin::AdminServices** retornará MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="102d6-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="102d6-140">O nome do perfil pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="102d6-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="102d6-141">Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.</span><span class="sxs-lookup"><span data-stu-id="102d6-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="102d6-142">Espaços incorporados, mas não espaços à esquerda ou à direita.</span><span class="sxs-lookup"><span data-stu-id="102d6-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="102d6-143">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="102d6-143">MFCMAPI reference</span></span>

<span data-ttu-id="102d6-144">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="102d6-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="102d6-145">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="102d6-145">**File**</span></span>|<span data-ttu-id="102d6-146">**Function**</span><span class="sxs-lookup"><span data-stu-id="102d6-146">**Function**</span></span>|<span data-ttu-id="102d6-147">**Comment**</span><span class="sxs-lookup"><span data-stu-id="102d6-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="102d6-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="102d6-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="102d6-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="102d6-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="102d6-150">MFCMAPI usa o método **IProfAdmin::AdminServices** para abrir um objeto de administração do serviço de mensagem para o perfil selecionado adicionar serviços.</span><span class="sxs-lookup"><span data-stu-id="102d6-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="102d6-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="102d6-151">See also</span></span>



[<span data-ttu-id="102d6-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="102d6-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="102d6-153">IProfAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="102d6-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="102d6-154">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="102d6-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

