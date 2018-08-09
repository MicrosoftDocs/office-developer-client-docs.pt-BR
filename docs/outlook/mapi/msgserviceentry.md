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
ms.openlocfilehash: 9af170f3445757eb96b9fe78c7cbea2c29ef4612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768165"
---
# <a name="msgserviceentry"></a><span data-ttu-id="f54c7-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="f54c7-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="f54c7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f54c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f54c7-105">Define um protótipo para uma função de ponto de entrada de serviço mensagens oferecer suporte a configuração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f54c7-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f54c7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f54c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="f54c7-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="f54c7-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="f54c7-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="f54c7-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="f54c7-109">Serviços de mensagens</span><span class="sxs-lookup"><span data-stu-id="f54c7-109">Message services</span></span>  <br/> |
|<span data-ttu-id="f54c7-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="f54c7-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="f54c7-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="f54c7-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f54c7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f54c7-112">Parameters</span></span>

 <span data-ttu-id="f54c7-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="f54c7-113">_hInstance_</span></span>
  
> <span data-ttu-id="f54c7-114">[in] Identificador da instância do providerDLL serviço.</span><span class="sxs-lookup"><span data-stu-id="f54c7-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="f54c7-115">A alça geralmente é usada para recuperar recursos.</span><span class="sxs-lookup"><span data-stu-id="f54c7-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="f54c7-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="f54c7-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="f54c7-117">[in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="f54c7-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="f54c7-118">O serviço de mensagem, talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="f54c7-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="f54c7-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="f54c7-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="f54c7-120">[in] Ponteiro para uma [IMAPISupport: IUnknown](imapisupportiunknown.md) implementação de interface.</span><span class="sxs-lookup"><span data-stu-id="f54c7-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="f54c7-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f54c7-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="f54c7-122">[in] Um valor específico de implementação usado para passar as informações de interface de usuário para uma função ou zero.</span><span class="sxs-lookup"><span data-stu-id="f54c7-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="f54c7-123">O parâmetro _ulUIParam_ é o identificador da janela pai para a caixa de diálogo de configuração e do tipo HWND (cast para um ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="f54c7-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="f54c7-124">Um valor de zero indica que não há nenhuma janela pai.</span><span class="sxs-lookup"><span data-stu-id="f54c7-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="f54c7-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f54c7-125">_ulFlags_</span></span>
  
> <span data-ttu-id="f54c7-126">[in] Bitmask dos sinalizadores indicando opções para a função de entrada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f54c7-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="f54c7-127">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f54c7-127">The following flags can be set:</span></span>
    
<span data-ttu-id="f54c7-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f54c7-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f54c7-129">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f54c7-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f54c7-130">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f54c7-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="f54c7-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="f54c7-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="f54c7-132">Interface do usuário de configuração do serviço deve exibir a configuração atual, mas não permitir que o usuário alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="f54c7-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="f54c7-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="f54c7-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="f54c7-134">Permite que uma caixa de diálogo de configuração a ser exibido, se necessário.</span><span class="sxs-lookup"><span data-stu-id="f54c7-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="f54c7-135">Quando o sinalizador SERVICE_UI_ALLOWED é definido, a caixa de diálogo deve ser exibida apenas se a matriz de valores de propriedade _lpProps_ está vazia ou não contiver uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="f54c7-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="f54c7-136">Se SERVICE_UI_ALLOWED não estiver definida, uma caixa de diálogo ainda pode exibida se o sinalizador SERVICE_UI_ALWAYS está definido.</span><span class="sxs-lookup"><span data-stu-id="f54c7-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="f54c7-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="f54c7-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="f54c7-138">Solicita que a caixa de diálogo de configuração para o provedor ativa ser exibida na parte superior de outras caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f54c7-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="f54c7-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="f54c7-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="f54c7-140">Requer o serviço de mensagem para exibir uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="f54c7-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="f54c7-141">Se o sinalizador SERVICE_UI_ALWAYS não estiver definido, uma caixa de diálogo Configuração ainda pode exibida se o sinalizador SERVICE_UI_ALLOWED está definido e as informações de configuração válida não estão disponíveis da matriz de valores de propriedade _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="f54c7-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="f54c7-142">SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS deve ser definida para permitir que uma interface de usuário a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="f54c7-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="f54c7-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="f54c7-143">_ulContext_</span></span>
  
> <span data-ttu-id="f54c7-144">[in] A operação de configuração que MAPI está atualmente executando.</span><span class="sxs-lookup"><span data-stu-id="f54c7-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="f54c7-145">O parâmetro _ulContext_ conterá um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f54c7-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="f54c7-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="f54c7-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="f54c7-147">Alterações na configuração do serviço devem ser feitas no perfil.</span><span class="sxs-lookup"><span data-stu-id="f54c7-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="f54c7-148">Se o sinalizador SERVICE_UI_ALWAYS estiver definido, o serviço deve exibir sua caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="f54c7-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="f54c7-149">A caixa de diálogo também deve ser exibida se o sinalizador SERVICE_UI_ALLOWED está definido e o parâmetro _lpProps_ está vazio ou não contém dados de configuração válida.</span><span class="sxs-lookup"><span data-stu-id="f54c7-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="f54c7-150">Se _lpProps_ contém dados válidos, nenhuma caixa de diálogo deve ser exibida e o serviço deve usar esses dados para tornar a alteração de configuração.</span><span class="sxs-lookup"><span data-stu-id="f54c7-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="f54c7-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="f54c7-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="f54c7-152">O serviço está sendo adicionado a um perfil.</span><span class="sxs-lookup"><span data-stu-id="f54c7-152">The service is being added to a profile.</span></span> <span data-ttu-id="f54c7-153">Se o SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED sinalizador estiver definido, o serviço deve exibir sua caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="f54c7-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="f54c7-154">Se nenhum dos sinalizadores estiver definida, o serviço deve falhar.</span><span class="sxs-lookup"><span data-stu-id="f54c7-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="f54c7-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="f54c7-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="f54c7-156">O serviço está sendo removido de um perfil.</span><span class="sxs-lookup"><span data-stu-id="f54c7-156">The service is being removed from a profile.</span></span> <span data-ttu-id="f54c7-157">Após receber esse evento, o serviço deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="f54c7-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="f54c7-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="f54c7-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="f54c7-159">O serviço foi instalado a estação de trabalho do usuário de uma rede, disquete ou outra mídia externa.</span><span class="sxs-lookup"><span data-stu-id="f54c7-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="f54c7-160">Após receber esse evento, o serviço geralmente Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="f54c7-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="f54c7-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="f54c7-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="f54c7-162">Solicita que o serviço de cria uma instância adicional de um provedor.</span><span class="sxs-lookup"><span data-stu-id="f54c7-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="f54c7-163">Se o serviço oferece suporte a essa operação, ele deve chamar [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="f54c7-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="f54c7-164">Se o serviço não oferece suporte a essa operação, ele poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f54c7-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="f54c7-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="f54c7-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="f54c7-166">Solicita que o serviço excluir uma instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="f54c7-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="f54c7-167">Se o serviço oferece suporte a essa operação, ele deve chamar [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="f54c7-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="f54c7-168">Se o serviço não oferece suporte a essa operação, ele poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f54c7-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="f54c7-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="f54c7-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="f54c7-170">O serviço está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="f54c7-170">The service is being removed.</span></span> <span data-ttu-id="f54c7-171">Após receber esse evento, o serviço pode executar qualquer tarefa de limpeza que deve ser feita antes que o serviço termina e depois retornamos com um valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="f54c7-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="f54c7-172">Se o usuário cancelar a remoção, o serviço deve retornar MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="f54c7-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="f54c7-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="f54c7-173">_cValues_</span></span>
  
> <span data-ttu-id="f54c7-174">[in] Contagem de valores de propriedade na matriz apontado pelo parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="f54c7-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="f54c7-175">O valor do parâmetro _cValues_ é zero se MAPI está passando sem valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f54c7-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="f54c7-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="f54c7-176">_lpProps_</span></span>
  
> <span data-ttu-id="f54c7-177">[in] Ponteiro para uma matriz opcional de [SPropValue](spropvalue.md) estruturas indicando valores para propriedades de suporte para o provedor que a função usará na configuração do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f54c7-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="f54c7-178">A função apenas usa esse parâmetro se o parâmetro _ulContext_ for definido como MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="f54c7-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="f54c7-179">Esse parâmetro normalmente é usado para passar o caminho para um arquivo para um serviço baseado em arquivo, como um serviço de catálogo de endereços pessoal.</span><span class="sxs-lookup"><span data-stu-id="f54c7-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="f54c7-180">Se o sinalizador MSG_SERVICE_CONFIGURE não será passado no parâmetro _ulFlags_ , o parâmetro _lpProps_ deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f54c7-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="f54c7-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="f54c7-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="f54c7-182">[in] Ponteiro para uma interface de [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que a função pode usar para localizar as seções de perfil para um provedor específico no serviço de mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="f54c7-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="f54c7-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="f54c7-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="f54c7-184">[out] Ponteiro para uma estrutura [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="f54c7-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="f54c7-185">A estrutura é alocada com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f54c7-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="f54c7-186">Todos os membros são opcionais, embora a maioria das estruturas conterá uma cadeia de caracteres de mensagem de erro válido no membro _lpszError_ .</span><span class="sxs-lookup"><span data-stu-id="f54c7-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="f54c7-187">Se os membros _lpszComponent_ ou _lpszError_ da estrutura estiverem presentes, sua memória deve ser eventualmente liberada por uma única chamada de [MAPIFreeBuffer](mapifreebuffer.md) na estrutura de base.</span><span class="sxs-lookup"><span data-stu-id="f54c7-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f54c7-188">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f54c7-188">Return value</span></span>

<span data-ttu-id="f54c7-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="f54c7-189">S_OK</span></span> 
  
> <span data-ttu-id="f54c7-190">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="f54c7-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f54c7-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="f54c7-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="f54c7-192">O provedor de serviço não foi configurado.</span><span class="sxs-lookup"><span data-stu-id="f54c7-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="f54c7-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f54c7-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f54c7-194">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f54c7-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="f54c7-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f54c7-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f54c7-196">O provedor não oferece suporte a alterações em seus objetos ou não oferece suporte a notificação de alterações.</span><span class="sxs-lookup"><span data-stu-id="f54c7-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="f54c7-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f54c7-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f54c7-198">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="f54c7-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f54c7-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="f54c7-199">Remarks</span></span>

<span data-ttu-id="f54c7-200">Uma função definida usando o protótipo de função **MSGSERVICEENTRY** permite que os serviços de mensagens para configurar sozinhos ou para executar outras ações específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="f54c7-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="f54c7-201">A função principalmente fornece uma caixa de diálogo na qual o usuário pode alterar configurações específicas para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f54c7-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="f54c7-202">Ele também pode oferecer suporte configuração programática usando a matriz de valor de propriedade passada no parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="f54c7-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="f54c7-203">Configuração programática é opcional, a menos que o serviço suporta o Assistente de perfil, para os quais é necessário.</span><span class="sxs-lookup"><span data-stu-id="f54c7-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="f54c7-204">MAPI chama esse ponto de entrada do aplicativo de painel de controle ou em resposta a um aplicativo cliente chamar [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="f54c7-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="f54c7-205">MAPI coloca o nome da função que um serviço de mensagem usa para o protótipo **MSGSERVICEENTRY** mas prefira o nome **ServiceEntry**sem restrição.</span><span class="sxs-lookup"><span data-stu-id="f54c7-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="f54c7-206">Não há nenhuma restrição quanto o ordinal da função e um único provedor DLL pode conter mais de uma função.</span><span class="sxs-lookup"><span data-stu-id="f54c7-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="f54c7-207">No entanto, apenas um das funções pode ser nomeado **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="f54c7-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="f54c7-208">Um serviço de mensagem pode usar a função [BuildDisplayTable](builddisplaytable.md) e o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar a implementação de caixa de diálogo configuração.</span><span class="sxs-lookup"><span data-stu-id="f54c7-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="f54c7-209">É possível que um usuário cancelar uma operação de MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="f54c7-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="f54c7-210">Nesse caso, a função **ServiceEntry** deve verificar com o usuário para verificar se o serviço não deve ser removido e retornar MAPI_E_USER_CANCEL se o serviço permanecerá instalado.</span><span class="sxs-lookup"><span data-stu-id="f54c7-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="f54c7-211">Uma função com base em protótipo **MSGSERVICEENTRY** retorna um dos valores HRESULT listados.</span><span class="sxs-lookup"><span data-stu-id="f54c7-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="f54c7-212">MAPI encaminha esse valor ao responder a chamada de um cliente para [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="f54c7-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="f54c7-213">Serviços de mensagem que exportar uma função de entrada de serviço devem incluir as propriedades de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) e o **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) na seção serviço de mensagem do MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="f54c7-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

