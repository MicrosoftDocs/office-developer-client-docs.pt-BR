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
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Relacionar o OSC ao Outlook e a redes sociais

Outlook Social Connector (OSC) pode exibir nas atividades de cartão de visita do Office e o painel de pessoas do Outlook, status ou atualizações de fotos para uma colega de trabalho, amigo ou qualquer pessoa que você está associado. Por padrão, o OSC exibe os emails do Outlook, anexos, e solicitações de reunião recebidas de uma pessoa selecionada. Se a pessoa selecionada e o usuário do Office colaboram em um site do SharePoint, o OSC também exibe atualizações do documento e outras atividades de site do site do SharePoint. Dependendo os contextos de que o usuário do Office está interessado em associação, o usuário do Office pode instalar provedores de OSC para aplicativos de linha de negócios, sites corporativos internos ou uma variedade de sites de rede profissional e social, como o LinkedIn, Facebook e Windows Live.
  
Para suportar o compartilhamento da funcionalidade entre aplicativos cliente do Office, o mecanismo de núcleo OSC é implementado como parte de um componente compartilhado do Office e o painel de pessoas é implementado como um suplemento do Outlook. Para usar o OSC, um usuário do Office deve instalou o Outlook no computador cliente e configurado o Outlook com um perfil, para que o OSC pode armazenar em cache os contatos em uma pasta Contatos. 
  
Um provedor OSC é um modelo COM (Component Object) DLL que permite que o OSC acessar dados de redes sociais de forma independente das APIs de cada rede social. Um provedor OSC DLL deve ser instalado localmente em um computador cliente. Provedor OSC da rede social conecta o OSC, que faz parte do Outlook, com a rede social na Internet.
  
Um provedor OSC deve implementar um conjunto de interfaces, definido como parte de extensibilidade do provedor do OSC, para se comunicar com o OSC. Estensibilidade do provedor do OSC está disponível como uma plataforma aberta.
  
A arquitetura do provedor do OSC permite que vários provedores trabalhar com o mecanismo de núcleo do OSC e agregam informações sociais como amigos e atividades. A Figura 1 ilustra a arquitetura de provedor do OSC.
  
**Figura 1. Arquitetura do provedor do Outlook Social Connector**

![Social networks, OSC providers, OSC, and Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologia

Nesta Outlook Social Connector Provider referência do, uma rede social é usada para referir-se aos seguintes tipos de sites: 
  
- Sites de colaboração como o SharePoint.
    
- Sites de rede social, como Facebook e Windows Live.
    
- Sites de rede profissional como LinkedIn.
    
- Outros aplicativos de linha de negócios ou os sites internos corporativos usados para redes.
    
O amigo termo é usado geralmente para incluir amigos, familiares, colegas, conexões e qualquer pessoa um usuário do Office está associado em um contexto de colaboração como o SharePoint ou adicionou à conta de redes sociais do usuário. Não-amigos são pessoas referenciadas nas atualizações da atividade de amigos dos mas não amigos que foram adicionados à conta de redes sociais do usuário do Office. Os contatos são pessoas em uma pasta de contato do Outlook. 
  
## <a name="see-also"></a>Confira também

- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)

