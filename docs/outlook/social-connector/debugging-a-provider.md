---
title: Depurar um provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Há várias maneiras que você pode depurar um provedor do Outlook Social Connector (OSC):'
ms.openlocfilehash: ada439ca3b038ca9a0e849b47ff6a5f54e5016f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770829"
---
# <a name="debugging-a-provider"></a><span data-ttu-id="6b5a7-103">Depurar um provedor</span><span class="sxs-lookup"><span data-stu-id="6b5a7-103">Debugging a provider</span></span>

<span data-ttu-id="6b5a7-104">Há várias maneiras que você pode depurar um provedor do Outlook Social Connector (OSC):</span><span class="sxs-lookup"><span data-stu-id="6b5a7-104">There are several ways you can debug an Outlook Social Connector (OSC) provider:</span></span> 
  
- <span data-ttu-id="6b5a7-105">Usando os comandos debug no componente da faixa de opções da interface de usuário Office Fluent no Outlook ou no aplicativo cliente do Office de suporte para fazer com que o OSC levar a várias ações.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-105">By using debug commands in the ribbon component of the Office Fluent user interface in Outlook or the supporting Office client application to cause the OSC to take various actions.</span></span>
    
- <span data-ttu-id="6b5a7-106">Usando o Fiddler para chamadas de API de rastreamento e XML enviadas entre uma rede social e seu provedor OSC</span><span class="sxs-lookup"><span data-stu-id="6b5a7-106">By using Fiddler to trace API calls and XML sent between a social network and its OSC provider</span></span>
    
## <a name="debug-buttons"></a><span data-ttu-id="6b5a7-107">Botões de depuração</span><span class="sxs-lookup"><span data-stu-id="6b5a7-107">Debug buttons</span></span>

<span data-ttu-id="6b5a7-108">A extensibilidade do provedor OSC oferece a capacidade de um provedor OSC de depuração.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-108">The OSC provider extensibility provides the capability of debugging an OSC provider.</span></span> <span data-ttu-id="6b5a7-109">Para depurar um provedor, crie um `DebugProviders` valor do tipo DWORD no registro do Windows sob o `SocialConnector` principais (conforme mostrado na seguinte linha) e defina o `DebugProviders` valor como 1.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-109">To debug a provider, create a  `DebugProviders` value of type DWORD in the Windows registry under the  `SocialConnector` key (as shown in the following line), and set the  `DebugProviders` value to 1.</span></span> 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
<span data-ttu-id="6b5a7-110">Por padrão, o provedor de depuração está desativada.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-110">By default, provider debugging is off.</span></span> <span data-ttu-id="6b5a7-111">Se o `DebugProviders` valor não estiver presente, ou ele está presente e definido com um valor 0, o provedor de depuração está desativado.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-111">If the  `DebugProviders` value is not present, or it is present and set to a value of 0, provider debugging is turned off.</span></span> 
  
<span data-ttu-id="6b5a7-112">Se o provedor de depuração está ativado, o OSC exibe uma caixa de diálogo alerta com informações de erro verbose quando ocorre um erro e valida qualquer provedor OSC XML em relação ao esquema XML de provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-112">If provider debugging is turned on, the OSC displays an alert dialog box with verbose error information when an error occurs, and validates any OSC provider XML against the OSC provider XML schema.</span></span> <span data-ttu-id="6b5a7-113">Um provedor OSC desenvolvido usando OSC 1.0 com base no namespace especificado para uma sequência de caracteres XML, é validado contra o arquivo de esquema OSC 1.0, OutlookSocialProvider.xsd.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-113">Based on the namespace specified for an XML string, an OSC provider developed by using OSC 1.0 is validated against the OSC 1.0 schema file, OutlookSocialProvider.xsd.</span></span> <span data-ttu-id="6b5a7-114">Um provedor OSC desenvolvidos usando OSC 1.1 ou posterior é validado contra o arquivo de esquema, OutlookSocialProvider_1.1.xsd.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-114">An OSC provider developed by using OSC 1.1 or later is validated against the schema file, OutlookSocialProvider_1.1.xsd.</span></span> <span data-ttu-id="6b5a7-115">Quando você usa o `DebugProviders` valor, o alerta de depuração aparece para todos carregados provedores em vez de um provedor específico.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-115">When you use the  `DebugProviders` value, the debug alert appears for all loaded providers instead of a specific provider.</span></span> 
  
<span data-ttu-id="6b5a7-116">Para exibir os botões de depuração que podem ajudá-lo um provedor de depuração, crie um `ShowDebugButtons` valor do tipo DWORD no registro do Windows sob o `SocialConnector` principais e definir o `ShowDebugButtons` valor como 1.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-116">To display debug buttons that can help you debug a provider, create a  `ShowDebugButtons` value of type DWORD in the Windows registry under the  `SocialConnector` key, and set the  `ShowDebugButtons` value to 1.</span></span> <span data-ttu-id="6b5a7-117">Para ocultar os botões de barra de comandos de depuração, defina o `ShowDebugButtons` valor como 0.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-117">To hide the debug command bar buttons, set the  `ShowDebugButtons` value to 0.</span></span> 
  
<span data-ttu-id="6b5a7-118">Para o Outlook 2010 e aplicativos de cliente desde o Office 2013, os botões de depuração aparecem na guia **suplementos** da faixa de opções do explorer.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-118">For Outlook 2010 and client applications since Office 2013, the debug buttons appear on the **Add-ins** tab of the explorer ribbon.</span></span> <span data-ttu-id="6b5a7-119">Para o Outlook 2007 e Outlook 2003, os botões de depuração aparecem na barra de comandos padrão da janela do explorer do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-119">For Outlook 2007 and Outlook 2003, the debug buttons appear on the standard command bar of the Outlook explorer window.</span></span> 
  
<span data-ttu-id="6b5a7-120">A tabela a seguir descreve os botões de depuração.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-120">The following table describes the debug buttons.</span></span>
  
|<span data-ttu-id="6b5a7-121">**Botão de depuração**</span><span class="sxs-lookup"><span data-stu-id="6b5a7-121">**Debug button**</span></span>|<span data-ttu-id="6b5a7-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="6b5a7-122">**Function**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b5a7-123">Sincronizar contatos</span><span class="sxs-lookup"><span data-stu-id="6b5a7-123">Sync Contacts</span></span>  <br/> |<span data-ttu-id="6b5a7-124">Faz com que o OSC pedir o provedor do OSC apenas os contatos em cache.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-124">Causes the OSC to ask the OSC provider for cached contacts only.</span></span>  <br/> |
|<span data-ttu-id="6b5a7-125">Sincronização da GAL</span><span class="sxs-lookup"><span data-stu-id="6b5a7-125">GAL Sync</span></span>  <br/> |<span data-ttu-id="6b5a7-126">Faz com que o OSC preencher dados da lista de endereços Global do Exchange para contatos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-126">Causes the OSC to populate data from the Exchange Global Address List to Outlook contacts.</span></span>  <br/> |
|<span data-ttu-id="6b5a7-127">Invalidar o Cache de categoria</span><span class="sxs-lookup"><span data-stu-id="6b5a7-127">Invalidate Category Cache</span></span>  <br/> |<span data-ttu-id="6b5a7-128">Faz com que o OSC recarregar a lista de categorias para cada repositório quando o feed de atividade for atualizado.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-128">Causes the OSC to reload the category list for each store when the activity feed is refreshed.</span></span>  <br/> |
   
## <a name="fiddler"></a><span data-ttu-id="6b5a7-129">Fiddler</span><span class="sxs-lookup"><span data-stu-id="6b5a7-129">Fiddler</span></span>

<span data-ttu-id="6b5a7-130">Fiddler é uma ferramenta de depuração do over-durante a transmissão para verificar a chamadas à API enviadas do seu provedor para a rede social e XML enviadas pela rede social para seu provedor.</span><span class="sxs-lookup"><span data-stu-id="6b5a7-130">Fiddler is an over-the-wire debugging tool to check the API calls sent from your provider to the social network, and XML sent by the social network to your provider.</span></span> <span data-ttu-id="6b5a7-131">Fiddler está disponível para download no [Proxy de depuração da Web Fiddler](http://www.fiddler2.com/fiddler2/version.asp).</span><span class="sxs-lookup"><span data-stu-id="6b5a7-131">Fiddler is available for download at [Fiddler Web Debugging Proxy](http://www.fiddler2.com/fiddler2/version.asp).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b5a7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b5a7-132">See also</span></span>

- [<span data-ttu-id="6b5a7-133">Etapas rápidas de aprendizado para desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="6b5a7-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)  
- [<span data-ttu-id="6b5a7-134">Sincronização de amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="6b5a7-134">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md) 
- [<span data-ttu-id="6b5a7-135">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="6b5a7-135">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
- [<span data-ttu-id="6b5a7-136">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="6b5a7-136">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="6b5a7-137">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="6b5a7-137">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="6b5a7-138">Preparando-se para o lançamento de um provedor OSC</span><span class="sxs-lookup"><span data-stu-id="6b5a7-138">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

