---
title: Relacionar o OSC ao Outlook e a redes sociais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) pode exibir nas atividades de cartão de visita do Office e o painel de pessoas do Outlook, status ou atualizações de fotos para uma colega de trabalho, amigo ou qualquer pessoa que você está associado.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770954"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="95272-103">Relacionar o OSC ao Outlook e a redes sociais</span><span class="sxs-lookup"><span data-stu-id="95272-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="95272-104">Outlook Social Connector (OSC) pode exibir nas atividades de cartão de visita do Office e o painel de pessoas do Outlook, status ou atualizações de fotos para uma colega de trabalho, amigo ou qualquer pessoa que você está associado.</span><span class="sxs-lookup"><span data-stu-id="95272-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="95272-105">Por padrão, o OSC exibe os emails do Outlook, anexos, e solicitações de reunião recebidas de uma pessoa selecionada.</span><span class="sxs-lookup"><span data-stu-id="95272-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="95272-106">Se a pessoa selecionada e o usuário do Office colaboram em um site do SharePoint, o OSC também exibe atualizações do documento e outras atividades de site do site do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="95272-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="95272-107">Dependendo os contextos de que o usuário do Office está interessado em associação, o usuário do Office pode instalar provedores de OSC para aplicativos de linha de negócios, sites corporativos internos ou uma variedade de sites de rede profissional e social, como o LinkedIn, Facebook e Windows Live.</span><span class="sxs-lookup"><span data-stu-id="95272-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="95272-108">Para suportar o compartilhamento da funcionalidade entre aplicativos cliente do Office, o mecanismo de núcleo OSC é implementado como parte de um componente compartilhado do Office e o painel de pessoas é implementado como um suplemento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="95272-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="95272-109">Para usar o OSC, um usuário do Office deve instalou o Outlook no computador cliente e configurado o Outlook com um perfil, para que o OSC pode armazenar em cache os contatos em uma pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="95272-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="95272-110">Um provedor OSC é um modelo COM (Component Object) DLL que permite que o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social.</span><span class="sxs-lookup"><span data-stu-id="95272-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="95272-111">Um provedor OSC DLL deve ser instalado localmente em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="95272-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="95272-112">Provedor OSC da rede social conecta o OSC, que faz parte do Outlook, com a rede social na Internet.</span><span class="sxs-lookup"><span data-stu-id="95272-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="95272-113">Um provedor OSC deve implementar um conjunto de interfaces, definido como parte de extensibilidade do provedor do OSC, para se comunicar com o OSC.</span><span class="sxs-lookup"><span data-stu-id="95272-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="95272-114">Estensibilidade do provedor do OSC está disponível como uma plataforma aberta.</span><span class="sxs-lookup"><span data-stu-id="95272-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="95272-115">A arquitetura do provedor do OSC permite que vários provedores trabalhar com o mecanismo de núcleo do OSC e agregam informações sociais como amigos e atividades.</span><span class="sxs-lookup"><span data-stu-id="95272-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="95272-116">A Figura 1 ilustra a arquitetura de provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="95272-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="95272-117">**Figura 1. Arquitetura do provedor do Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="95272-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Social networks, OSC providers, OSC, and Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="95272-119">Terminologia</span><span class="sxs-lookup"><span data-stu-id="95272-119">Terminology</span></span>

<span data-ttu-id="95272-120">Nesta Outlook Social Connector Provider referência do, uma rede social é usada para referir-se aos seguintes tipos de sites:</span><span class="sxs-lookup"><span data-stu-id="95272-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="95272-121">Sites de colaboração como o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="95272-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="95272-122">Sites de rede social, como Facebook e Windows Live.</span><span class="sxs-lookup"><span data-stu-id="95272-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="95272-123">Sites de rede profissional como LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="95272-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="95272-124">Outros aplicativos de linha de negócios ou os sites internos corporativos usados para redes.</span><span class="sxs-lookup"><span data-stu-id="95272-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="95272-125">O amigo termo é usado geralmente para incluir amigos, familiares, colegas, conexões e qualquer pessoa um usuário do Office está associado em um contexto de colaboração como o SharePoint ou adicionou à conta de redes sociais do usuário.</span><span class="sxs-lookup"><span data-stu-id="95272-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="95272-126">Não-amigos são pessoas referenciadas nas atualizações da atividade de amigos dos mas não amigos que foram adicionados à conta de redes sociais do usuário do Office.</span><span class="sxs-lookup"><span data-stu-id="95272-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="95272-127">Os contatos são pessoas em uma pasta de contato do Outlook.</span><span class="sxs-lookup"><span data-stu-id="95272-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95272-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="95272-128">See also</span></span>

- [<span data-ttu-id="95272-129">Introdução ao desenvolvimento de um Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="95272-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

