---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430802"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="ba3cf-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="ba3cf-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="ba3cf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba3cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba3cf-105">Adiciona um provedor de serviços ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-105">Adds a service provider to the message service.</span></span> 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="ba3cf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba3cf-106">Parameters</span></span>

 <span data-ttu-id="ba3cf-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="ba3cf-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="ba3cf-108">[in] Um ponteiro para o nome do provedor a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="ba3cf-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="ba3cf-109">_cValues_</span></span>
  
> <span data-ttu-id="ba3cf-110">[in] A contagem de valores de propriedade apontados pelo _parâmetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="ba3cf-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="ba3cf-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="ba3cf-111">_lpProps_</span></span>
  
> <span data-ttu-id="ba3cf-112">[in] Um ponteiro para uma matriz de valores de propriedade que descreve as propriedades do provedor a adicionar.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="ba3cf-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ba3cf-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="ba3cf-114">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="ba3cf-115">O _parâmetro ulUIParam_ será usado se o sinalizador MAPI_DIALOG for definido no _parâmetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="ba3cf-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ba3cf-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ba3cf-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ba3cf-117">[in] Uma bitmask de sinalizadores que controla a adição do provedor.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="ba3cf-118">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ba3cf-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="ba3cf-119">MAPI_DIALOG: exibe uma caixa de diálogo para solicitar informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="ba3cf-120">MAPI_UNICODE: o nome do provedor e as propriedades de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="ba3cf-121">Se o MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ba3cf-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="ba3cf-122">_lpUID_</span></span>
  
> <span data-ttu-id="ba3cf-123">[out] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ba3cf-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ba3cf-124">Return value</span></span>

<span data-ttu-id="ba3cf-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba3cf-125">S_OK</span></span> 
  
> <span data-ttu-id="ba3cf-126">O provedor foi adicionado com êxito ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="ba3cf-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ba3cf-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ba3cf-128">O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ba3cf-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba3cf-129">Remarks</span></span>

<span data-ttu-id="ba3cf-130">O **método IProviderAdmin::CreateProvider** adiciona um provedor de serviços ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="ba3cf-131">O  _parâmetro lpszProvider_ deve apontar para o nome de um provedor que pertence ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="ba3cf-132">**CreateProvider** não verifica se o nome corresponde ao nome de um provedor no serviço; se o nome passado não corresponder ao nome de um serviço, a chamada será bem-sucedida, mas os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="ba3cf-133">A maioria dos serviços de mensagens não permite que provedores sejam adicionados ou excluídos enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="ba3cf-134">Depois que todas as informações disponíveis sobre o provedor de serviços são adicionadas ao perfil do arquivo Mapisvc.inf, **CreateProvider** chama a função de ponto de entrada do serviço de mensagens com o parâmetro  _ulContext_ definido como MSG_SERVICE_PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="ba3cf-135">Se MAPI_DIALOG for definido no parâmetro _ulFlags_ do método **CreateProvider,** os valores nos parâmetros _ulUIParam_ e _ulFlags_ também serão passados para a função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="ba3cf-136">Esses parâmetros adicionais permitem que o provedor de serviços exibir sua folha de propriedades para que o usuário possa inserir definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="ba3cf-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ba3cf-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba3cf-137">See also</span></span>

- [<span data-ttu-id="ba3cf-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ba3cf-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="ba3cf-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="ba3cf-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="ba3cf-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ba3cf-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="ba3cf-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba3cf-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

