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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578623"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="72246-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="72246-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="72246-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72246-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72246-105">Adiciona um provedor de serviço para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="72246-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="72246-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72246-106">Parameters</span></span>

 <span data-ttu-id="72246-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="72246-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="72246-108">[in] Um ponteiro para o nome do provedor para adicionar.</span><span class="sxs-lookup"><span data-stu-id="72246-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="72246-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="72246-109">_cValues_</span></span>
  
> <span data-ttu-id="72246-110">[in] A contagem dos valores de propriedade apontado pelo parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="72246-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="72246-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="72246-111">_lpProps_</span></span>
  
> <span data-ttu-id="72246-112">[in] Um ponteiro para uma matriz de valor de propriedade que descreve as propriedades do provedor para adicionar.</span><span class="sxs-lookup"><span data-stu-id="72246-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="72246-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="72246-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="72246-114">[in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="72246-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="72246-115">O parâmetro _ulUIParam_ é usado se o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="72246-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="72246-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72246-116">_ulFlags_</span></span>
  
> <span data-ttu-id="72246-117">[in] Uma bitmask dos sinalizadores que controla a adição do provedor.</span><span class="sxs-lookup"><span data-stu-id="72246-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="72246-118">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="72246-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="72246-119">MAPI_DIALOG: Exibe uma caixa de diálogo para solicitar informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="72246-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="72246-120">MAPI_UNICODE: As propriedades de nome e a cadeia de caracteres do provedor estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="72246-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="72246-121">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="72246-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="72246-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="72246-122">_lpUID_</span></span>
  
> <span data-ttu-id="72246-123">[out] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor para adicionar.</span><span class="sxs-lookup"><span data-stu-id="72246-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="72246-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="72246-124">Return value</span></span>

<span data-ttu-id="72246-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="72246-125">S_OK</span></span> 
  
> <span data-ttu-id="72246-126">O provedor foi adicionado com êxito ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="72246-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="72246-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="72246-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="72246-128">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="72246-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="72246-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="72246-129">Remarks</span></span>

<span data-ttu-id="72246-130">O método **IProviderAdmin::CreateProvider** adiciona um provedor de serviço para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="72246-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="72246-131">O parâmetro _lpszProvider_ deve apontar para o nome de um provedor que pertence ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="72246-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="72246-132">**CreateProvider** não verifica se o nome corresponde ao nome de um provedor de serviço; Se o nome passado não corresponder a um nome de serviço, a chamada é bem-sucedida, mas os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="72246-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="72246-133">A maioria dos serviços de mensagem não permita provedores a ser adicionado ou excluído enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="72246-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="72246-134">Afinal das informações disponíveis sobre o serviço provedor foi adicionada ao perfil do arquivo Mapisvc, **CreateProvider** chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_ PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="72246-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="72246-135">Se MAPI_DIALOG é definida no parâmetro de _ulFlags_ do método **CreateProvider** , os valores nos parâmetros _ulUIParam_ e _ulFlags_ também são passados para a função do ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="72246-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="72246-136">Esses parâmetros adicionais habilitar o provedor de serviços para exibir sua folha de propriedades, de modo que o usuário pode digitar as definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="72246-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72246-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="72246-137">See also</span></span>

- [<span data-ttu-id="72246-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="72246-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="72246-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="72246-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="72246-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="72246-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="72246-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72246-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

