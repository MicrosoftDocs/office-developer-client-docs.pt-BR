---
title: Preparando-se para o lançamento de um provedor OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7d28349-3121-49ae-ad28-043789e2d205
description: Esta seção sugere os testes, que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 5caf4144a8daed31d30c9ecbcf9cf21c2300ed8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770830"
---
# <a name="getting-ready-to-release-an-osc-provider"></a>Preparando-se para o lançamento de um provedor OSC

Esta seção sugere os testes, que você pode fazer antes de liberar seu provedor do Outlook Social Connector (OSC). Você pode iniciar consultando os tópicos desta seção e realizar alguns desses testes durante seu desenvolvimento e as fases de teste, mas você deve concluir estes testes quando que você solta. 

Esses testes verificam a funcionalidade básica da sua implementação das interfaces do provedor do OSC com relação aos recursos que você especificar para o provedor do OSC. Além disso, mesmo que o OSC é um recurso compartilhado por vários aplicativos de cliente do Office, esses testes usam o Outlook como o cliente para testar a funcionalidade fundamental. Você deve determinar se outros testes são necessários para recursos específicos para o seu provedor.
  
## <a name="in-this-section"></a>Nesta seção

- [Implantação de teste](testing-deployment.md): descreve os cenários, você deve ser testado em torno de instalação e desinstalação de um provedor OSC.
    
- [Recursos de teste, a autenticação e a configuração](testing-capabilities-authentication-and-configuration.md): descreve os testes para obtenção de recursos e cenários em torno Configurando uma conta e autenticação de um usuário para uma rede social.
    
- [Stop-seguir pessoas e testando seguir](testing-following-and-stop-following-persons.md): descreve os cenários para testar a capacidade do provedor OSC para adicionar uma pessoa como um amigo, ou para remover um amigo da rede social. 
    
- [Testando amigos](testing-friends.md): descreve os testes e cenários para verificar que o provedor do OSC apropriadamente retorna dados de amigos e não-amigos, onde aplicável, dependendo do modo de sincronização que o provedor oferece suporte.
    
- [Atividades de teste](testing-activities.md): descreve os testes e cenários para verificar que o provedor do OSC apropriadamente retorna atividades de amigos e não-amigos, onde aplicável, dependendo do modo de sincronização que o provedor oferece suporte.
    
## <a name="reference"></a>Referência

- [Referência do provedor do Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Se��es relacionadas

- [Modelos de amostra do OSC](osc-sample-templates.md)
  
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)
  
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)
  
- [Depurando um provedor](debugging-a-provider.md)
  
- [Implantando um provedor](deploying-a-provider.md)
  

