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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341605"
---
# <a name="msgserviceentry"></a><span data-ttu-id="a79b6-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="a79b6-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="a79b6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a79b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a79b6-105">Define um protótipo para uma função de ponto de entrada de serviço de mensagem para dar suporte à configuração de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a79b6-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a79b6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a79b6-106">Header file:</span></span>  <br/> |<span data-ttu-id="a79b6-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="a79b6-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a79b6-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="a79b6-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a79b6-109">Serviços de mensagens</span><span class="sxs-lookup"><span data-stu-id="a79b6-109">Message services</span></span>  <br/> |
|<span data-ttu-id="a79b6-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="a79b6-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a79b6-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a79b6-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a79b6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a79b6-112">Parameters</span></span>

 <span data-ttu-id="a79b6-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="a79b6-113">_hInstance_</span></span>
  
> <span data-ttu-id="a79b6-114">no Identificador da instância do serviço providerDLL.</span><span class="sxs-lookup"><span data-stu-id="a79b6-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="a79b6-115">Normalmente, o identificador é usado para recuperar recursos.</span><span class="sxs-lookup"><span data-stu-id="a79b6-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="a79b6-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="a79b6-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="a79b6-117">no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE.</span><span class="sxs-lookup"><span data-stu-id="a79b6-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="a79b6-118">O serviço de mensagens pode precisar usar esse método de alocação quando estiver trabalhando com determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="a79b6-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="a79b6-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="a79b6-120">no Ponteiro para uma implementação de interface [IMAPISupport: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b6-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="a79b6-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a79b6-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="a79b6-122">no Um valor específico de implementação usado para passar informações da interface do usuário para uma função ou zero.</span><span class="sxs-lookup"><span data-stu-id="a79b6-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="a79b6-123">O parâmetro _ulUIParam_ é o identificador de janela pai da caixa de diálogo de configuração e é do tipo HWND (conversão em um ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="a79b6-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="a79b6-124">Um valor igual A zero indica que não há janela pai.</span><span class="sxs-lookup"><span data-stu-id="a79b6-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="a79b6-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a79b6-125">_ulFlags_</span></span>
  
> <span data-ttu-id="a79b6-126">no Bitmask de sinalizadores que indicam opções para a função de entrada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a79b6-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="a79b6-127">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a79b6-127">The following flags can be set:</span></span>
    
<span data-ttu-id="a79b6-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a79b6-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a79b6-129">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a79b6-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a79b6-130">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a79b6-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="a79b6-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="a79b6-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="a79b6-132">A interface de usuário da configuração do serviço deve exibir a configuração atual, mas não permitir que o usuário a altere.</span><span class="sxs-lookup"><span data-stu-id="a79b6-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="a79b6-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="a79b6-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="a79b6-134">Permite que uma caixa de diálogo de configuração seja exibida se necessário.</span><span class="sxs-lookup"><span data-stu-id="a79b6-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="a79b6-135">Quando o sinalizador SERVICE_UI_ALLOWED estiver definido, a caixa de diálogo deve ser exibida somente se a matriz de valor da propriedade _lpProps_ estiver vazia ou não contiver uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="a79b6-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="a79b6-136">Se SERVICE_UI_ALLOWED não estiver definido, uma caixa de diálogo ainda poderá ser exibida se o sinalizador SERVICE_UI_ALWAYS estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a79b6-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="a79b6-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="a79b6-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="a79b6-138">Solicita que a caixa de diálogo de configuração do provedor ativo seja exibida na parte superior de outras caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a79b6-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="a79b6-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="a79b6-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="a79b6-140">Requer que o serviço de mensagens exiba uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a79b6-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="a79b6-141">Se o sinalizador SERVICE_UI_ALWAYS não estiver definido, uma caixa de diálogo de configuração ainda poderá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e as informações de configuração válidas não estiverem disponíveis na matriz de valor da propriedade _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a79b6-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="a79b6-142">O SERVICE_UI_ALLOWED ou o SERVICE_UI_ALWAYS deve ser definido para permitir que uma interface de usuário seja exibida.</span><span class="sxs-lookup"><span data-stu-id="a79b6-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="a79b6-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="a79b6-143">_ulContext_</span></span>
  
> <span data-ttu-id="a79b6-144">no A operação de configuração que o MAPI está executando no momento.</span><span class="sxs-lookup"><span data-stu-id="a79b6-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="a79b6-145">O parâmetro _ulContext_ conterá um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a79b6-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="a79b6-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="a79b6-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="a79b6-147">As alterações na configuração do serviço devem ser feitas no perfil.</span><span class="sxs-lookup"><span data-stu-id="a79b6-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="a79b6-148">Se o sinalizador SERVICE_UI_ALWAYS estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a79b6-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="a79b6-149">A caixa de diálogo também deverá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e se o parâmetro _lpProps_ estiver vazio ou não contiver dados de configuração válidos.</span><span class="sxs-lookup"><span data-stu-id="a79b6-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="a79b6-150">Se _lpProps_ contiver dados válidos, nenhuma caixa de diálogo deve ser exibida e o serviço deve usar esses dados para fazer a alteração da configuração.</span><span class="sxs-lookup"><span data-stu-id="a79b6-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="a79b6-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="a79b6-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="a79b6-152">O serviço está sendo adicionado a um perfil.</span><span class="sxs-lookup"><span data-stu-id="a79b6-152">The service is being added to a profile.</span></span> <span data-ttu-id="a79b6-153">Se o sinalizador SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a79b6-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="a79b6-154">Se nenhum sinalizador estiver definido, o serviço deve falhar.</span><span class="sxs-lookup"><span data-stu-id="a79b6-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="a79b6-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a79b6-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="a79b6-156">O serviço está sendo removido de um perfil.</span><span class="sxs-lookup"><span data-stu-id="a79b6-156">The service is being removed from a profile.</span></span> <span data-ttu-id="a79b6-157">Depois de receber esse evento, o serviço deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="a79b6-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="a79b6-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="a79b6-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="a79b6-159">O serviço foi instalado na estação de trabalho do usuário a partir de uma rede, disquete ou outra mídia externa.</span><span class="sxs-lookup"><span data-stu-id="a79b6-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="a79b6-160">Depois de receber esse evento, o serviço normalmente retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="a79b6-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="a79b6-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="a79b6-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="a79b6-162">Solicita que o serviço crie uma instância adicional de um provedor.</span><span class="sxs-lookup"><span data-stu-id="a79b6-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="a79b6-163">Se o serviço oferecer suporte a essa operação, ele deverá chamar [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a79b6-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="a79b6-164">Se o serviço não oferecer suporte a essa operação, poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a79b6-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="a79b6-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="a79b6-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="a79b6-166">Solicita que o serviço exclua uma instância de provedor.</span><span class="sxs-lookup"><span data-stu-id="a79b6-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="a79b6-167">Se o serviço oferecer suporte a essa operação, ele deverá chamar [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a79b6-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="a79b6-168">Se o serviço não oferecer suporte a essa operação, poderá retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a79b6-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="a79b6-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="a79b6-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="a79b6-170">O serviço está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="a79b6-170">The service is being removed.</span></span> <span data-ttu-id="a79b6-171">Depois de receber esse evento, o serviço pode executar qualquer tarefa de limpeza que deve ser realizada antes que o serviço seja encerrado e, em seguida, retorne com um valor de sucesso.</span><span class="sxs-lookup"><span data-stu-id="a79b6-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="a79b6-172">Se o usuário cancelar a remoção, o serviço deverá retornar MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="a79b6-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="a79b6-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="a79b6-173">_cValues_</span></span>
  
> <span data-ttu-id="a79b6-174">no Contagem de valores de propriedade na matriz apontada pelo parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a79b6-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="a79b6-175">O valor do parâmetro _cValues_ será zero se o MAPI não passar nenhum valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a79b6-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="a79b6-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="a79b6-176">_lpProps_</span></span>
  
> <span data-ttu-id="a79b6-177">no Ponteiro para uma matriz opcional de estruturas [SPropValue](spropvalue.md) indicando valores para propriedades suportadas pelo provedor que a função usará na configuração do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a79b6-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="a79b6-178">A função só usa esse parâmetro se o parâmetro _ulContext_ estiver definido como MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="a79b6-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="a79b6-179">Esse parâmetro é comumente usado para passar o caminho para um arquivo de um serviço baseado em arquivo, como um serviço de catálogo de endereços pessoal.</span><span class="sxs-lookup"><span data-stu-id="a79b6-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="a79b6-180">Se o sinalizador MSG_SERVICE_CONFIGURE não for passado no parâmetro _parâmetroulflags_ , o parâmetro _lpProps_ deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="a79b6-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="a79b6-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="a79b6-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="a79b6-182">no Ponteiro para uma interface [IProviderAdmin: IUnknown](iprovideradminiunknown.md) que a função pode usar para localizar seções de perfil de um provedor específico no serviço de mensagens atual.</span><span class="sxs-lookup"><span data-stu-id="a79b6-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="a79b6-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="a79b6-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="a79b6-184">bota Ponteiro para uma estrutura [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b6-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="a79b6-185">A estrutura é alocada com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a79b6-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="a79b6-186">Todos os membros são opcionais, embora a maioria das estruturas contenha uma cadeia de mensagem de erro válida no membro _lpszError_ .</span><span class="sxs-lookup"><span data-stu-id="a79b6-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="a79b6-187">Se os membros _lpszComponent_ ou _lpszError_ da estrutura estiverem presentes, sua memória deverá ser liberada por uma única chamada para [MAPIFreeBuffer](mapifreebuffer.md) na estrutura base.</span><span class="sxs-lookup"><span data-stu-id="a79b6-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a79b6-188">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a79b6-188">Return value</span></span>

<span data-ttu-id="a79b6-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="a79b6-189">S_OK</span></span> 
  
> <span data-ttu-id="a79b6-190">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="a79b6-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a79b6-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="a79b6-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="a79b6-192">O provedor de serviços não foi configurado.</span><span class="sxs-lookup"><span data-stu-id="a79b6-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="a79b6-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a79b6-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a79b6-194">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a79b6-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="a79b6-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a79b6-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a79b6-196">O provedor não oferece suporte a alterações em seus objetos ou não dá suporte à notificação de alterações.</span><span class="sxs-lookup"><span data-stu-id="a79b6-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="a79b6-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a79b6-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a79b6-198">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="a79b6-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a79b6-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="a79b6-199">Remarks</span></span>

<span data-ttu-id="a79b6-200">Uma função definida usando o protótipo de função **MSGSERVICEENTRY** permite que os serviços de mensagens se configurem ou realizem outras ações específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="a79b6-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="a79b6-201">A função fornece principalmente uma caixa de diálogo na qual o usuário pode alterar as configurações específicas do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a79b6-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="a79b6-202">Também pode oferecer suporte à configuração programática usando a matriz de valor de propriedade passada no parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a79b6-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="a79b6-203">A configuração programática é opcional, a menos que o serviço dê suporte ao assistente de perfil, para o qual é necessário.</span><span class="sxs-lookup"><span data-stu-id="a79b6-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="a79b6-204">MAPI chama esse ponto de entrada do aplicativo do painel de controle ou em resposta a um aplicativo cliente chamando [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a79b6-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="a79b6-205">O MAPI não coloca nenhuma restrição no nome da função que um serviço de mensagem usa para o protótipo **MSGSERVICEENTRY** , mas prefere o nome de **entrada**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="a79b6-206">Não há nenhuma restrição no ordinal para a função e uma única DLL de provedor pode conter mais de uma função.</span><span class="sxs-lookup"><span data-stu-id="a79b6-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="a79b6-207">No enTanto, apenas uma das funções pode ser nomeada como de **entrada**.</span><span class="sxs-lookup"><span data-stu-id="a79b6-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="a79b6-208">Um serviço de mensagens pode usar a função [BuildDisplayTable](builddisplaytable.md) e o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para simplificar a implementação da caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="a79b6-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="a79b6-209">É possível que um usuário cancele uma operação MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="a79b6-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="a79b6-210">Nesse caso, a função de serviço de **entrada** deve verificar com o usuário se o serviço não deve ser removido e retornar MAPI_E_USER_CANCEL se o serviço permanecer instalado.</span><span class="sxs-lookup"><span data-stu-id="a79b6-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="a79b6-211">Uma função com base no protótipo **MSGSERVICEENTRY** retorna um dos valores HRESULT listados.</span><span class="sxs-lookup"><span data-stu-id="a79b6-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="a79b6-212">O MAPI encaminha esse valor ao responder à chamada de um cliente para [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a79b6-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="a79b6-213">Os serviços de mensagens que exportam uma função de entrada de serviço devem incluir as propriedades **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) e **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) na seção serviço de mensagens de MAPISVC. INF.</span><span class="sxs-lookup"><span data-stu-id="a79b6-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

