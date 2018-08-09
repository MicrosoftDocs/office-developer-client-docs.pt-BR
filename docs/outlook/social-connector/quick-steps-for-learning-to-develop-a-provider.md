---
title: Etapas rápidas para aprender a desenvolver um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Este tópico sugere algumas etapas para saber mais sobre como desenvolver um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 345e8600c704504be091ee23c66b7f85575cde90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770950"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Etapas rápidas para aprender a desenvolver um provedor

Para desenvolver um provedor OSC, você precisará concluir as seguintes etapas gerais:
  
- Implemente as quatro interfaces obrigatórias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)e [ISocialPerson](isocialpersoniunknown.md). Dependendo do suporte da sua rede social para armazenar em cache a seguir uma pessoa na rede social, ou dinamicamente sincronização amigos e suas atividades, credenciais de logon, talvez você queira implementar a interface [ISocialSession2](isocialsession2iunknown.md) . 
    
- Em paralelo com implementando interfaces, testar e depurar o provedor do OSC. 

- Implante o provedor do OSC.  

- Faça testes finais antes do lançamento.
    
## <a name="step-a-implementing-interfaces"></a>R: de etapa implementando interfaces

Um provedor OSC implementa interfaces para que o OSC possa usar essas interfaces para obter as informações necessárias sobre ou da rede social, por meio do provedor do OSC. Essas informações incluem o seguinte:
  
- Como apresentar a caixa de diálogo de logon de conta para um usuário.    
- Se o provedor oferece suporte à mostrando amigos ou atividades como exibido na rede social.    
- Como exibir amigos e atividades no cartão de visita ou no painel de pessoas do Outlook.     
- Quando atualizar informações de amigos ou atividades no cartão de visita ou no painel pessoas.
    
Normalmente, as informações são passadas do provedor para OSC, no formato de cadeias de caracteres XML como parâmetros de saída dos métodos de interface. O OSC e um provedor OSC estão em conformidade com o esquema XML de provedor do OSC. Portanto, durante a implementar as interfaces, você precisa de uma boa compreensão de como o esquema XML permite especificar informações conforme listadas acima. 

Os recursos a seguir explicam como especificar XML para recursos do provedor, amigos e atividades:
  
- [Sequências de chamadas comuns do OSC](osc-typical-calling-sequences.md)    
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md)    
- [Exemplo de XML de recursos](capabilities-xml-example.md)   
- [XML para recursos](xml-for-capabilities.md)    
- [Exemplo de XML de amigos](friends-xml-example.md)    
- [XML para amigos](xml-for-friends.md)   
- [Exemplo de XML de Feed de atividade](activity-feed-xml-example.md)   
- [XML para atividades](xml-for-activities.md)
    
Antes de começar a implementação, consulte também os tópicos a seguir para economizar tempo posteriormente no processo de depuração:
  
- [Requisitos técnicos](technical-requirements.md)    
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)    
- [Modelos de amostra do OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Etapa de depuração de b:

O tópico [depurando um provedor](debugging-a-provider.md) sugere a depuração de procedimentos que você pode usar enquanto desenvolve um provedor OSC. 
  
Enquanto desenvolve, você também pode consultar a [Obtenção pronto para lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md) para compreender melhor o comportamento esperado em determinados cenários (por exemplo, autenticação básica e baseada em formulários). 
  
## <a name="step-c-deploying"></a>Implantando o etapa c:

Consulte os tópicos a seguir para saber mais sobre os requisitos de implantação:
  
- [Implantando um provedor](deploying-a-provider.md)    
- [Registrando um provedor](registering-a-provider.md)   
- [Lista de verificação de instalação](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Etapa d: teste antes da liberação de Final

Dependendo da sua rede social e o provedor do OSC, há testes de geralmente específico do provedor, que você deve realizar antes de liberar seu provedor. Para uma lista de sugestões de testes, consulte [Getting Ready ao lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Confira também

- [Introdução ao desenvolvimento de um Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)

