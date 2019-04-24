---
title: Depurar um provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Há várias maneiras de depurar um provedor de serviços do Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281066"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="cd91a-103">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="cd91a-103">Debugging a provider</span></span>

<span data-ttu-id="cd91a-104">Há várias maneiras de depurar um provedor de serviços do Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="cd91a-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="cd91a-105">Usando os comandos de depuração no componente da faixa de opções da interface de usuário do Office Fluent no Outlook ou o aplicativo de suporte ao do Office você pode fazer com que o OSC execute várias ações.</span><span class="sxs-lookup"><span data-stu-id="cd91a-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="cd91a-106">Usando Fiddler para rastrear chamadas de API de e XML enviadas entre o seu provedor OSC e uma rede social</span><span class="sxs-lookup"><span data-stu-id="cd91a-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="cd91a-107">Botões de depurar</span><span class="sxs-lookup"><span data-stu-id="cd91a-107">Debug buttons</span></span>

<span data-ttu-id="cd91a-108">A extensibilidade do provedor OSC fornece a capacidade de depuração de um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="cd91a-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="cd91a-109">Para depurar um provedor, crie um chave `DebugProviders` com o valor DWORD no registro do Windows na `SocialConnector` (como mostrado na linha seguinte) e configure o `DebugProviders` valor 1.</span><span class="sxs-lookup"><span data-stu-id="cd91a-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="cd91a-110">Por padrão, o provedor de depuração de bugs está desativado.</span><span class="sxs-lookup"><span data-stu-id="cd91a-110">By default, provider debugging is off.</span></span> <span data-ttu-id="cd91a-111">Se o valor `DebugProviders` não estiver presente, ou estiver presente e definir o valor de 0, a depuração do provedor estará desativada.</span><span class="sxs-lookup"><span data-stu-id="cd91a-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="cd91a-112">Se o provedor de depuração de bugs estiver ativado, o OSC exibirá uma caixa de diálogo de alerta com informações detalhadas sobre erros, quando ocorrer um erro e validará qualquer XML de provedor OSC contra o esquema XML do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="cd91a-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="cd91a-113">Com base no namespace especificado por uma cadeia de XML, um provedor de OSC que foi desenvolvido usando o OSC 1.0 é validado contra o esquema de arquivo OSC 1.0, OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="cd91a-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="cd91a-114">Um provedor de OSC desenvolvido usando OSC 1.1 ou posterior valida o arquivo de esquema OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="cd91a-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="cd91a-115">Quando você usa o valor`DebugProviders` o alerta de depuração é exibido para todos os provedores carregados em vez de um provedor específico.</span><span class="sxs-lookup"><span data-stu-id="cd91a-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="cd91a-116">Para exibir os botões de depuração que podem te ajudar a deputar um provedor, crie um`ShowDebugButtons` com o valor DWORD no registro do Windows dentro da `SocialConnector` chave e configure o `ShowDebugButtons` valor 1.</span><span class="sxs-lookup"><span data-stu-id="cd91a-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="cd91a-117">Para ocultar os botões da barra de comando depuração, defina o `ShowDebugButtons` valor como 0.</span><span class="sxs-lookup"><span data-stu-id="cd91a-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="cd91a-118">Para aplicativos de clientes como o Office 2013 e Outlook 2010, os botões de depuração aparecem na guia \*\*suplementos da faixa explorar de opções.</span><span class="sxs-lookup"><span data-stu-id="cd91a-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="cd91a-119">Para o Outlook 2007 e o Outlook 2003, os botões de depuração aparecem na barra de comandos padrão da janela no Explorador do Outlook.</span><span class="sxs-lookup"><span data-stu-id="cd91a-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="cd91a-120">A tabela a seguir descreve os botões de depurar.</span><span class="sxs-lookup"><span data-stu-id="cd91a-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="cd91a-121">**Botões de depurar**</span><span class="sxs-lookup"><span data-stu-id="cd91a-121">**Debug button**</span></span>|<span data-ttu-id="cd91a-122">**Função**</span><span class="sxs-lookup"><span data-stu-id="cd91a-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd91a-123">Sincronizar contatos</span><span class="sxs-lookup"><span data-stu-id="cd91a-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="cd91a-124">Faz com que o OSC peça ao provedor OSC somente contatos armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="cd91a-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="cd91a-125">Sincronização do GAL</span><span class="sxs-lookup"><span data-stu-id="cd91a-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="cd91a-126">Faz com que o OSC preencha dados da lista de endereços Global do Exchange para contatos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="cd91a-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="cd91a-127">Invalidar o Cache de categoria</span><span class="sxs-lookup"><span data-stu-id="cd91a-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="cd91a-128">Faz com que o OSC recarregue a lista de categorias para cada loja quando o feed de atividades for atualizado.</span><span class="sxs-lookup"><span data-stu-id="cd91a-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="cd91a-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="cd91a-129">Fiddler</span></span>

<span data-ttu-id="cd91a-130">Fiddler é uma ferramenta de depuração acima do fio para verificar chamadas de API enviadas para o seu provedor de rede social e XML enviados pela rede social para o seu provedor.</span><span class="sxs-lookup"><span data-stu-id="cd91a-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="cd91a-131">Fiddler está disponível para download em[Fiddler Web Proxy de depuração](https://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="cd91a-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](https://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd91a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd91a-132">See also</span></span>

- [<span data-ttu-id="cd91a-133">Etapas rápidas para aprender a desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="cd91a-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="cd91a-134">Sincronizar amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="cd91a-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="cd91a-135">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="cd91a-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="cd91a-136">Sequências de chamadas típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="cd91a-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="cd91a-137">Desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="cd91a-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="cd91a-138">Preparando um provedor de OSC para lançamento</span><span class="sxs-lookup"><span data-stu-id="cd91a-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

