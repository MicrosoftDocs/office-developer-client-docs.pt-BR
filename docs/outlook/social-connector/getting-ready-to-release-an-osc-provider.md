---
title: Preparando-se para lançar um provedor do OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Esta seção sugere testes que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 8a36b13f8adc42a1834481d3a5942f0350c43cc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414659"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Preparando-se para lançar um provedor do OSC

Esta seção sugere testes que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC). Você pode começar a se referir aos tópicos nesta seção e realizar alguns desses testes durante suas fases de desenvolvimento e teste, mas já deve ter concluído esses testes no momento da liberação. 

Esses testes verificam a funcionalidade básica de sua implementação das interfaces do provedor OSC em relação aos recursos especificados para o provedor osC. Além disso, embora o OSC seja um recurso compartilhado por vários aplicativos cliente do Office, esses testes usam o Outlook como o cliente para testar a funcionalidade fundamental. Você deve determinar se outros testes são necessários para recursos específicos do seu provedor.
  
## <a name="in-this-section"></a>Nesta seção

- [Teste de implantação:](testing-deployment.md)descreve cenários que você deve testar em torno da instalação e desinstalação de um provedor do OSC.
    
- [Recursos de teste, autenticação](testing-capabilities-authentication-and-configuration.md)e configuração: descreve testes para obter recursos e cenários sobre como configurar uma conta e autenticar um usuário para uma rede social.
    
- [Testing Following and Stop-Following Persons:](testing-following-and-stop-following-persons.md)Describes scenarios to test the OSC provider's ability to add a person as a friend, or to remove a friend from the social network. 
    
- [Amigos de](testing-friends.md)teste: descreve testes e cenários para verificar se o provedor OSC retorna adequadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização que o provedor oferece suporte.
    
- [Atividades de](testing-activities.md)teste: descreve testes e cenários para verificar se o provedor OSC retorna adequadamente atividades de amigos e não amigos, quando aplicável, dependendo do modo de sincronização que o provedor oferece suporte.
    
## <a name="reference"></a>Referências

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Seções relacionadas

- [Modelos de exemplo do OSC](osc-sample-templates.md)
  
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)
  
- [Desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurar um provedor](debugging-a-provider.md)
  
- [Implantar um provedor](deploying-a-provider.md)
  

