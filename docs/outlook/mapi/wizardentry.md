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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2c307d18c5b62e5190aa10632a47a3f16b80e81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770718"
---
# <a name="wizardentry"></a><span data-ttu-id="7dbe8-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="7dbe8-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="7dbe8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7dbe8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7dbe8-105">Define uma função de ponto de entrada de provedor de serviço que o Assistente de perfil chama para recuperar informações suficientes para exibir as folhas de propriedades de configuração do provedor.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7dbe8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7dbe8-106">Header file:</span></span>  <br/> |<span data-ttu-id="7dbe8-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="7dbe8-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="7dbe8-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="7dbe8-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="7dbe8-109">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="7dbe8-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="7dbe8-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="7dbe8-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="7dbe8-111">Assistente de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="7dbe8-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="7dbe8-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="7dbe8-112">Parameters</span></span>

 <span data-ttu-id="7dbe8-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="7dbe8-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="7dbe8-114">[in] Alça da instância da DLL do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="7dbe8-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="7dbe8-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="7dbe8-116">[out] Ponteiro para uma cadeia de caracteres que contém o nome completo do recurso diálogo que deve ser exibido pelo Assistente de perfil durante a configuração.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="7dbe8-117">O tamanho máximo da cadeia de caracteres, incluindo o terminador NULL, é 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="7dbe8-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="7dbe8-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="7dbe8-119">[out] Ponteiro para um procedimento de caixa de diálogo Windows padrão que será chamado pelo Assistente de perfil para notificar o provedor de vários eventos.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="7dbe8-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="7dbe8-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="7dbe8-121">[in] Ponteiro para uma implementação de interface de propriedade que fornece acesso às propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="7dbe8-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="7dbe8-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="7dbe8-123">[in] Ponteiro para o objeto de suporte MAPI aplicável a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7dbe8-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7dbe8-124">Return value</span></span>

<span data-ttu-id="7dbe8-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="7dbe8-125">S_OK</span></span> 
  
> <span data-ttu-id="7dbe8-126">Função **WIZARDENTRY** do provedor de serviços foi chamada com êxito.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="7dbe8-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7dbe8-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="7dbe8-128">Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7dbe8-129">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="7dbe8-129">Remarks</span></span>

<span data-ttu-id="7dbe8-130">O Assistente de perfil chama a função **WIZARDENTRY** com base em quando ele estiver pronto para exibir a interface do usuário de configuração do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="7dbe8-131">Quando o Assistente de perfil for terminar de configurar todos os provedores, ele grava as propriedades de configuração para o perfil chamando [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe8-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7dbe8-132">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="7dbe8-132">Notes to implementers</span></span>

<span data-ttu-id="7dbe8-133">Deve ser colocado o nome da função **WIZARDENTRY** com base na entrada WIZARD_ENTRY_NAME Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="7dbe8-134">O nome do recurso é que o recurso de diálogo que serão renderizados no painel do Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="7dbe8-135">O recurso que é passado regressivo deve conter todas as páginas em um recurso de diálogo único.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="7dbe8-136">Quando o Assistente de perfil recebe este recurso, ele ignora o estilo de diálogo, mas não os estilos de controle e cria todos os controles como filhos da página do Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="7dbe8-137">Todos os controles inicialmente estão ocultas.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-137">All controls are initially hidden.</span></span> <span data-ttu-id="7dbe8-138">Provedores Certifique-se de que as coordenadas para seus controles zero ou baseado em zero e que não exceder a largura máxima de 200 unidades de diálogo e uma altura de máxima de 150 unidades de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="7dbe8-139">Identificadores de controle abaixo 400 são reservados para o Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="7dbe8-140">O Assistente de perfil exibe o título do provedor com texto em negrito acima da interface de usuário do provedor.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="7dbe8-141">O ponteiro de interface da propriedade fornecido no parâmetro _lpMAPIProp_ deve ser mantido pelo provedor para referência futura.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="7dbe8-142">O Assistente de perfil lida com apenas o conjunto de forma mais básico de propriedades e o provedor pode usar a implementação de interface de propriedade para incluir propriedades adicionais.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="7dbe8-143">Durante a configuração, provedores devem adicionar suas propriedades de configuração para o objeto implementando a interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="7dbe8-144">Depois que todos os provedores que tiverem sido configurados, o Assistente de perfil adiciona essas propriedades para o perfil.</span><span class="sxs-lookup"><span data-stu-id="7dbe8-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="7dbe8-145">Para obter mais informações sobre como usar esta função, consulte [Configuração do serviço de mensagem com suporte](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="7dbe8-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

