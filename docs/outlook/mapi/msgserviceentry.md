---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427875"
---
# <a name="msgserviceentry"></a><span data-ttu-id="c3c7e-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c3c7e-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="c3c7e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3c7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3c7e-105">Define um protótipo para uma função de ponto de entrada do serviço de mensagens para dar suporte à configuração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3c7e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c3c7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3c7e-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="c3c7e-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="c3c7e-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="c3c7e-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="c3c7e-109">Serviços de mensagens</span><span class="sxs-lookup"><span data-stu-id="c3c7e-109">Message services</span></span>  <br/> |
|<span data-ttu-id="c3c7e-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="c3c7e-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="c3c7e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="c3c7e-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="c3c7e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3c7e-112">Parameters</span></span>

 <span data-ttu-id="c3c7e-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-113">_hInstance_</span></span>
  
> <span data-ttu-id="c3c7e-114">[in] Alça da instância do provedor de serviçosDLL.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="c3c7e-115">O alça é normalmente usado para recuperar recursos.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="c3c7e-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="c3c7e-117">[in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.**</span><span class="sxs-lookup"><span data-stu-id="c3c7e-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="c3c7e-118">O serviço de mensagens pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="c3c7e-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="c3c7e-120">[in] Ponteiro para uma [implementação de interface IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="c3c7e-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="c3c7e-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="c3c7e-122">[in] Um valor específico de implementação usado para passar informações da interface do usuário para uma função ou zero.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="c3c7e-123">O  _parâmetro ulUIParam_ é o identificador da janela pai da caixa de diálogo de configuração e é do tipo HWND (cast to a ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="c3c7e-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="c3c7e-124">Um valor zero indica que não há janela pai.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="c3c7e-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-125">_ulFlags_</span></span>
  
> <span data-ttu-id="c3c7e-126">[in] Bitmask de sinalizadores indicando opções para a função de entrada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="c3c7e-127">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c3c7e-127">The following flags can be set:</span></span>
    
<span data-ttu-id="c3c7e-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c3c7e-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c3c7e-129">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c3c7e-130">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="c3c7e-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="c3c7e-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="c3c7e-132">A interface do usuário de configuração do serviço deve exibir a configuração atual, mas não permitir que o usuário a altere.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="c3c7e-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="c3c7e-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="c3c7e-134">Permite que uma caixa de diálogo de configuração seja exibida, se necessário.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="c3c7e-135">Quando o SERVICE_UI_ALLOWED de texto estiver definido, a caixa de diálogo deverá ser exibida somente se a matriz de valores da propriedade  _lpProps_ estiver vazia ou não tiver uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="c3c7e-136">Se SERVICE_UI_ALLOWED não estiver definido, uma caixa de diálogo ainda poderá ser exibida se o sinalizador SERVICE_UI_ALWAYS estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="c3c7e-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="c3c7e-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="c3c7e-138">Solicita que a caixa de diálogo de configuração do provedor ativo seja exibida sobre outras caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="c3c7e-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="c3c7e-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="c3c7e-140">Requer que o serviço de mensagens exibir uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="c3c7e-141">Se o sinalizador SERVICE_UI_ALWAYS não estiver definido, uma caixa de diálogo de configuração ainda poderá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e as informações de configuração válidas não estarão disponíveis na matriz de valores da propriedade _lpProps._</span><span class="sxs-lookup"><span data-stu-id="c3c7e-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="c3c7e-142">As SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS devem ser definidas para permitir que uma interface do usuário seja exibida.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="c3c7e-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-143">_ulContext_</span></span>
  
> <span data-ttu-id="c3c7e-144">[in] A operação de configuração que o MAPI está executando no momento.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="c3c7e-145">O  _parâmetro ulContext_ conterá um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c3c7e-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="c3c7e-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="c3c7e-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="c3c7e-147">As alterações na configuração do serviço devem ser feitas no perfil.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="c3c7e-148">Se o SERVICE_UI_ALWAYS sinalizador estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="c3c7e-149">A caixa de diálogo também deverá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e o parâmetro  _lpProps_ estiver vazio ou não tiver dados de configuração válidos.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="c3c7e-150">Se  _lpProps_ contiver dados válidos, nenhuma caixa de diálogo deverá ser exibida e o serviço deverá usar esses dados para fazer a alteração na configuração.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="c3c7e-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="c3c7e-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="c3c7e-152">O serviço está sendo adicionado a um perfil.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-152">The service is being added to a profile.</span></span> <span data-ttu-id="c3c7e-153">Se o sinalizador SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="c3c7e-154">Se nenhum sinalizador estiver definido, o serviço deve falhar.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="c3c7e-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="c3c7e-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="c3c7e-156">O serviço está sendo removido de um perfil.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-156">The service is being removed from a profile.</span></span> <span data-ttu-id="c3c7e-157">Depois de receber esse evento, o serviço deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="c3c7e-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="c3c7e-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="c3c7e-159">O serviço foi instalado na estação de trabalho do usuário a partir de uma rede, disquete ou outra mídia externa.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="c3c7e-160">Depois de receber esse evento, o serviço geralmente retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="c3c7e-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="c3c7e-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="c3c7e-162">Solicita que o serviço crie uma instância adicional de um provedor.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="c3c7e-163">Se o serviço suportar essa operação, ele deverá chamar [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="c3c7e-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="c3c7e-164">Se o serviço não suportar essa operação, ele poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="c3c7e-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="c3c7e-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="c3c7e-166">Solicita que o serviço exclua uma instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="c3c7e-167">Se o serviço suportar essa operação, ele deverá chamar [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="c3c7e-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="c3c7e-168">Se o serviço não suportar essa operação, ele poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="c3c7e-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="c3c7e-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="c3c7e-170">O serviço está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-170">The service is being removed.</span></span> <span data-ttu-id="c3c7e-171">Depois de receber esse evento, o serviço pode executar qualquer tarefa de limpeza que deve ser feita antes do serviço terminar e, em seguida, retornar com um valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="c3c7e-172">Se o usuário cancelar a remoção, o serviço deverá retornar MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="c3c7e-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-173">_cValues_</span></span>
  
> <span data-ttu-id="c3c7e-174">[in] Contagem de valores de propriedade na matriz apontada pelo _parâmetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="c3c7e-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="c3c7e-175">O valor do parâmetro  _cValues_ será zero se MAPI não estiver passando valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="c3c7e-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-176">_lpProps_</span></span>
  
> <span data-ttu-id="c3c7e-177">[in] Ponteiro para uma matriz opcional de [estruturas SPropValue](spropvalue.md) indicando valores para propriedades com suporte do provedor que a função usará na configuração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="c3c7e-178">A função só usará esse parâmetro se o  _parâmetro ulContext_ estiver definido como MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="c3c7e-179">Esse parâmetro é normalmente usado para passar o caminho para um arquivo para um serviço baseado em arquivo, como um serviço de agenda pessoal.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="c3c7e-180">Se o MSG_SERVICE_CONFIGURE sinalizador não for passado no  _parâmetro ulFlags,_ o parâmetro  _lpProps_ deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="c3c7e-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="c3c7e-182">[in] Ponteiro para uma interface [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que a função pode usar para localizar seções de perfil para um provedor específico no serviço de mensagens atual.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="c3c7e-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="c3c7e-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="c3c7e-184">[out] Ponteiro para uma [estrutura MAPIERROR.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="c3c7e-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="c3c7e-185">A estrutura é alocada com a [função MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c3c7e-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="c3c7e-186">Todos os membros são opcionais, embora a maioria das estruturas contenha uma cadeia de caracteres de mensagem de erro válida _no membro lpszError._</span><span class="sxs-lookup"><span data-stu-id="c3c7e-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="c3c7e-187">Se os membros  _lpszComponent_ ou  _lpszError_ da estrutura estão presentes, sua memória eventualmente deve ser liberada por uma única chamada para [MAPIFreeBuffer](mapifreebuffer.md) na estrutura base.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c3c7e-188">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c3c7e-188">Return value</span></span>

<span data-ttu-id="c3c7e-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3c7e-189">S_OK</span></span> 
  
> <span data-ttu-id="c3c7e-190">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c3c7e-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="c3c7e-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="c3c7e-192">O provedor de serviços não foi configurado.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="c3c7e-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c3c7e-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c3c7e-194">O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="c3c7e-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c3c7e-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c3c7e-196">O provedor não suporta alterações em seus objetos ou não suporta a notificação de alterações.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="c3c7e-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c3c7e-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c3c7e-198">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação só dá suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3c7e-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3c7e-199">Remarks</span></span>

<span data-ttu-id="c3c7e-200">Uma função definida usando o protótipo **de função MSGSERVICEENTRY** permite que os serviços de mensagens se configurem ou executem outras ações específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="c3c7e-201">A função fornece principalmente uma caixa de diálogo na qual o usuário pode alterar configurações específicas para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="c3c7e-202">Ele também pode dar suporte à configuração programática usando a matriz de valores de propriedade passada no _parâmetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="c3c7e-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="c3c7e-203">A configuração programática é opcional, a menos que o serviço suporte o Assistente de Perfil, para o qual ele é necessário.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="c3c7e-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="c3c7e-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="c3c7e-205">MAPI não coloca restrições no nome da função que um serviço de mensagem usa para o protótipo **MSGSERVICEENTRY,** mas prefere o nome **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="c3c7e-206">Não há restrições no ordinal para a função, e um único provedor DLL pode conter mais de uma função.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="c3c7e-207">No entanto, apenas uma das funções pode ser chamada **de ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="c3c7e-208">Um serviço de mensagens pode usar a [função BuildDisplayTable](builddisplaytable.md) e o [método IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar a implementação da caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="c3c7e-209">É possível que um usuário cancele uma operação MSG_SERVICE_UNINSTALL usuário.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="c3c7e-210">Nesse caso, a **função ServiceEntry** deve verificar com o usuário para verificar se o serviço não deve ser removido e retornar MAPI_E_USER_CANCEL se o serviço permanece instalado.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="c3c7e-211">Uma função baseada no protótipo **MSGSERVICEENTRY** retorna um dos valores HRESULT listados.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="c3c7e-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="c3c7e-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="c3c7e-213">Os serviços de mensagem que exportam uma função de entrada de serviço devem incluir as propriedades **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) e **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) na seção de serviço de mensagens de MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

