---
title: Relacionar o OSC ao Outlook e a redes sociais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: O Outlook Social Connector (OSC) pode ser exibido nas atividades, status ou atualizações do Painel de Pessoas do Office e do Painel de Pessoas do Outlook para um colega de trabalho, amigo ou qualquer pessoa com quem você está associado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428008"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="2c25a-103">Relacionar o OSC ao Outlook e a redes sociais</span><span class="sxs-lookup"><span data-stu-id="2c25a-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="2c25a-104">O Outlook Social Connector (OSC) pode ser exibido nas atividades, status ou atualizações do Painel de Pessoas do Office e do Painel de Pessoas do Outlook para um colega de trabalho, amigo ou qualquer pessoa com quem você está associado.</span><span class="sxs-lookup"><span data-stu-id="2c25a-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="2c25a-105">Por padrão, o OSC exibe os emails, anexos e solicitações de reunião do Outlook recebidos de uma pessoa selecionada.</span><span class="sxs-lookup"><span data-stu-id="2c25a-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="2c25a-106">Se a pessoa selecionada e o usuário do Office colaborarem em um site do SharePoint, o OSC também exibirá atualizações de documentos e outras atividades de site desse site do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2c25a-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="2c25a-107">Dependendo dos contextos de associação em que o usuário do Office está interessado, o usuário do Office pode instalar provedores OSC para aplicativos de linha de negócios, sites corporativos internos ou uma variedade de sites de redes sociais e profissionais, como LinkedIn, Facebook e Windows Live.</span><span class="sxs-lookup"><span data-stu-id="2c25a-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="2c25a-108">Para dar suporte ao compartilhamento de funcionalidades entre aplicativos cliente do Office, o mecanismo principal do OSC é implementado como parte de um componente compartilhado do Office e o Painel de Pessoas é implementado como um complemento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2c25a-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="2c25a-109">Para usar o OSC, um usuário do Office deve ter instalado o Outlook no computador cliente e configurado o Outlook com um perfil, para que o OSC possa armazenar em cache contatos em uma pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="2c25a-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="2c25a-110">Um provedor de OSC é um Component Object Model (COM) DLL que permite o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social.</span><span class="sxs-lookup"><span data-stu-id="2c25a-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="2c25a-111">Uma DLL do provedor OSC deve ser instalada localmente em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="2c25a-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="2c25a-112">O provedor osC de uma rede social conecta o OSC, que faz parte do Outlook, com a rede social na Internet.</span><span class="sxs-lookup"><span data-stu-id="2c25a-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="2c25a-113">Um provedor OSC deve implementar um conjunto de interfaces, definido como parte da extensibilidade do provedor OSC, para se comunicar com o OSC.</span><span class="sxs-lookup"><span data-stu-id="2c25a-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="2c25a-114">A extensibilidade do provedor OSC está disponível como uma plataforma aberta.</span><span class="sxs-lookup"><span data-stu-id="2c25a-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="2c25a-115">A arquitetura de provedor do OSC permite que vários provedores trabalhem com o mecanismo principal do OSC e agregam informações sociais, como amigos e atividades.</span><span class="sxs-lookup"><span data-stu-id="2c25a-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="2c25a-116">A Figura 1 ilustra a arquitetura do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="2c25a-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="2c25a-117">**Figura 1. Arquitetura do provedor do Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="2c25a-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Social networks, OSC providers, OSC, and Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="2c25a-119">Terminologia</span><span class="sxs-lookup"><span data-stu-id="2c25a-119">Terminology</span></span>

<span data-ttu-id="2c25a-120">Nesta Referência do Provedor do Outlook Social Connector, uma rede social é usada para se referir aos seguintes tipos de sites:</span><span class="sxs-lookup"><span data-stu-id="2c25a-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="2c25a-121">Sites colaborativos, como o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2c25a-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="2c25a-122">Sites de redes sociais, como Facebook e Windows Live.</span><span class="sxs-lookup"><span data-stu-id="2c25a-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="2c25a-123">Sites de rede profissionais, como o LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2c25a-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="2c25a-124">Outros aplicativos de linha de negócios ou sites internos corporativos usados para rede.</span><span class="sxs-lookup"><span data-stu-id="2c25a-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="2c25a-125">O termo amigo geralmente é usado para incluir amigos, familiares, colegas, conexões e qualquer outra pessoa à qual um usuário do Office está associado em um contexto colaborativo, como o SharePoint, ou adicionou à conta de rede social do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c25a-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="2c25a-126">Não amigos são pessoas referenciadas nas atualizações de atividades dos amigos, mas não são amigos que foram adicionados à conta de rede social do usuário do Office.</span><span class="sxs-lookup"><span data-stu-id="2c25a-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="2c25a-127">Contatos são pessoas em uma pasta de contatos do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2c25a-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c25a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c25a-128">See also</span></span>

- [<span data-ttu-id="2c25a-129">Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="2c25a-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

