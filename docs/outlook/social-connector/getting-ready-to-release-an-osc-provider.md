---
title: Preparando-se para liberar um provedor do OSC
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
# <a name="getting-ready-to-release-an-osc-provider"></a>Preparando-se para liberar um provedor do OSC

Esta seção sugere testes que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC). Você pode começar a fazer referência aos tópicos desta seção e a executar alguns desses testes durante suas fases de desenvolvimento e teste, mas você deve ter concluído esses testes no momento da liberação. 

Esses testes verificam a funcionalidade básica da sua implementação das interfaces do provedor OSC com relação aos recursos que você especificar para o provedor do OSC. Além disso, mesmo que o OSC seja um recurso compartilhado por vários aplicativos cliente do Office, esses testes usam o Outlook como cliente para testar a funcionalidade fundamental. Você deve determinar se outros testes são necessários para os recursos específicos do provedor.
  
## <a name="in-this-section"></a>Nesta seção

- [Testing Deployment](testing-deployment.md): descreve os cenários em que você deve testar a instalação e desinstalação de um provedor do OSC.
    
- [Recursos de teste, autenticação e configuração](testing-capabilities-authentication-and-configuration.md): descreve os testes para obter recursos e cenários sobre como configurar uma conta e autenticar um usuário para uma rede social.
    
- [Teste a seguir e pare as pessoas a seguir](testing-following-and-stop-following-persons.md): descreve cenários para testar a capacidade do provedor do OSC de adicionar uma pessoa como amigo ou remover um amigo da rede social. 
    
- [TestAndo amigos](testing-friends.md): descreve testes e cenários para verificar se o provedor do OSC retorna adequadamente dados de amigos e não amigos, quando aplicável, dependendo do modo de sincronização que o provedor suporta.
    
- [Atividades de teste](testing-activities.md): descreve testes e cenários para verificar se o provedor do OSC retorna adequadamente as atividades de amigos e não amigos, quando aplicável, dependendo do modo de sincronização que o provedor suporta.
    
## <a name="reference"></a>Referências

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Seções relacionadas

- [Modelos de exemplo do OSC](osc-sample-templates.md)
  
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)
  
- [Desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurar um provedor](debugging-a-provider.md)
  
- [Implantar um provedor](deploying-a-provider.md)
  

