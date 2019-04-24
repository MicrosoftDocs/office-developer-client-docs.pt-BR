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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279553"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="e16f3-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="e16f3-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="e16f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e16f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e16f3-105">Adiciona um provedor de serviços ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e16f3-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="e16f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e16f3-106">Parameters</span></span>

 <span data-ttu-id="e16f3-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="e16f3-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="e16f3-108">no Um ponteiro para o nome do provedor a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="e16f3-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="e16f3-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="e16f3-109">_cValues_</span></span>
  
> <span data-ttu-id="e16f3-110">no A contagem de valores de propriedade apontados pelo parâmetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="e16f3-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="e16f3-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="e16f3-111">_lpProps_</span></span>
  
> <span data-ttu-id="e16f3-112">no Um ponteiro para uma matriz de valor de propriedade que descreve as propriedades do provedor a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="e16f3-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="e16f3-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e16f3-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="e16f3-114">no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.</span><span class="sxs-lookup"><span data-stu-id="e16f3-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="e16f3-115">O parâmetro _ulUIParam_ é usado se o sinalizador MAPI_DIALOG estiver definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="e16f3-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e16f3-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e16f3-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e16f3-117">no Uma bitmask de sinalizadores que controlam a adição de provedor.</span><span class="sxs-lookup"><span data-stu-id="e16f3-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="e16f3-118">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e16f3-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="e16f3-119">MAPI_DIALOG: exibe uma caixa de diálogo para solicitar informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="e16f3-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="e16f3-120">MAPI_UNICODE: o nome do provedor e as propriedades de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e16f3-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="e16f3-121">Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e16f3-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="e16f3-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="e16f3-122">_lpUID_</span></span>
  
> <span data-ttu-id="e16f3-123">bota Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="e16f3-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e16f3-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e16f3-124">Return value</span></span>

<span data-ttu-id="e16f3-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="e16f3-125">S_OK</span></span> 
  
> <span data-ttu-id="e16f3-126">O provedor foi adicionado com êxito ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e16f3-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="e16f3-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e16f3-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e16f3-128">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e16f3-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e16f3-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="e16f3-129">Remarks</span></span>

<span data-ttu-id="e16f3-130">O método **IProviderAdmin:: CreateProvider** adiciona um provedor de serviços ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e16f3-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="e16f3-131">O parâmetro _lpszProvider_ deve apontar para o nome de um provedor que pertença ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e16f3-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="e16f3-132">O **CreateProvider** não verifica se o nome corresponde ao nome de um provedor no serviço; Se o nome passado não corresponder a um nome de serviço, a chamada será bem-sucedida, mas os resultados serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="e16f3-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="e16f3-133">A maioria dos serviços de mensagem não permite que os provedores sejam adicionados ou excluídos enquanto o perfil está em uso.</span><span class="sxs-lookup"><span data-stu-id="e16f3-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="e16f3-134">Depois que todas as informações disponíveis sobre o provedor de serviços forem adicionadas ao perfil do arquivo MAPISVC. inf, **CreateProvider** chamará a função de ponto de entrada do serviço de mensagens com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_ PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="e16f3-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="e16f3-135">Se MAPI_DIALOG for definido no parâmetro _parâmetroulflags_ do método **CreateProvider** , os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados para a função de ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="e16f3-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="e16f3-136">Esses parâmetros adicionais permitem que o provedor de serviços exiba sua folha de propriedades para que o usuário possa inserir definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="e16f3-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e16f3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e16f3-137">See also</span></span>

- [<span data-ttu-id="e16f3-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e16f3-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="e16f3-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="e16f3-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="e16f3-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="e16f3-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="e16f3-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e16f3-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

