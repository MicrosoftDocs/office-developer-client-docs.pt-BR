---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430676"
---
# <a name="wizardentry"></a><span data-ttu-id="25851-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="25851-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="25851-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25851-105">Define uma função de ponto de entrada do provedor de serviços que o Assistente de Perfil chama para recuperar informações suficientes para exibir as folhas de propriedades de configuração do provedor.</span><span class="sxs-lookup"><span data-stu-id="25851-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="25851-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="25851-106">Header file:</span></span>  <br/> |<span data-ttu-id="25851-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="25851-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="25851-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="25851-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="25851-109">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="25851-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="25851-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="25851-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="25851-111">Assistente de Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="25851-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="25851-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25851-112">Parameters</span></span>

 <span data-ttu-id="25851-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="25851-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="25851-114">[in] Alça de instância da DLL do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="25851-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="25851-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="25851-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="25851-116">[out] Ponteiro para uma cadeia de caracteres que contém o nome completo do recurso de caixa de diálogo que deve ser exibido pelo Assistente de Perfil durante a configuração.</span><span class="sxs-lookup"><span data-stu-id="25851-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="25851-117">O tamanho máximo da cadeia de caracteres, incluindo o terminador NULL, é de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="25851-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="25851-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="25851-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="25851-119">[out] Ponteiro para um procedimento de caixa de diálogo padrão do Windows que será chamado pelo Assistente de Perfil para notificar o provedor de vários eventos.</span><span class="sxs-lookup"><span data-stu-id="25851-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="25851-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="25851-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="25851-121">[in] Ponteiro para uma implementação de interface de propriedade que fornece acesso às propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="25851-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="25851-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="25851-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="25851-123">[in] Ponteiro para o objeto de suporte MAPI aplicável a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="25851-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25851-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="25851-124">Return value</span></span>

<span data-ttu-id="25851-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="25851-125">S_OK</span></span> 
  
> <span data-ttu-id="25851-126">A função **WIZARDENTRY** do provedor de serviços foi chamada com êxito.</span><span class="sxs-lookup"><span data-stu-id="25851-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="25851-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="25851-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="25851-128">Um erro de origem inesperada ou desconhecida impedia a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="25851-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25851-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="25851-129">Remarks</span></span>

<span data-ttu-id="25851-130">O Assistente de Perfil chama a função baseada em **WIZARDENTRY** quando ela está pronta para exibir a interface do usuário de configuração do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="25851-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="25851-131">Quando o Assistente de Perfil terminar de configurar todos os provedores, ele grava as propriedades de configuração no perfil chamando [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="25851-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="25851-132">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="25851-132">Notes to implementers</span></span>

<span data-ttu-id="25851-133">O nome da função **com base EM WIZARDENTRY** deve ser colocado na WIZARD_ENTRY_NAME entrada MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="25851-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="25851-134">O nome do recurso é o do recurso de caixa de diálogo que será renderizado no painel do Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="25851-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="25851-135">O recurso que é passado para trás precisa conter todas as páginas em um único recurso de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="25851-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="25851-136">Quando o Assistente de Perfil recebe esse recurso, ele ignora o estilo da caixa de diálogo, mas não os estilos de controle, e cria todos os controles como filhos da página do Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="25851-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="25851-137">Todos os controles são inicialmente ocultos.</span><span class="sxs-lookup"><span data-stu-id="25851-137">All controls are initially hidden.</span></span> <span data-ttu-id="25851-138">Os provedores devem garantir que as coordenadas para seus controles sejam baseadas em zero ou zero e que não excedam uma largura máxima de 200 unidades de diálogo e uma altura máxima de 150 unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="25851-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="25851-139">Os identificadores de controle abaixo de 400 são reservados para o Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="25851-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="25851-140">O Assistente de Perfil exibe o título do provedor em negrito acima da interface do usuário do provedor.</span><span class="sxs-lookup"><span data-stu-id="25851-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="25851-141">O ponteiro da interface de propriedade fornecido no  _parâmetro lpMAPIProp_ deve ser mantido pelo provedor para referência futura.</span><span class="sxs-lookup"><span data-stu-id="25851-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="25851-142">O Assistente de Perfil lida apenas com o conjunto mais básico de propriedades, e o provedor pode usar a implementação da interface de propriedade para incluir propriedades adicionais.</span><span class="sxs-lookup"><span data-stu-id="25851-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="25851-143">Durante a configuração, os provedores devem adicionar suas propriedades de configuração ao objeto que está implementando a interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="25851-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="25851-144">Depois que todos os provedores foram configurados, o Assistente de Perfil adiciona essas propriedades ao perfil.</span><span class="sxs-lookup"><span data-stu-id="25851-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="25851-145">Para obter mais informações sobre como usar essa função, consulte Suporte à configuração [do serviço de mensagens.](supporting-message-service-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="25851-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

