---
title: Etapas rápidas para aprender a desenvolver um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Este tópico sugere algumas etapas para aprender sobre como desenvolver um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424214"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Etapas rápidas para aprender a desenvolver um provedor

Para desenvolver um provedor OSC, você precisa concluir as seguintes etapas gerais:
  
- Implemente as quatro interfaces obrigatórias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [ISocialProfile](isocialprofileisocialperson.md)e [ISocialPerson](isocialpersoniunknown.md). Dependendo do suporte da rede social para armazenar credenciais de logon em cache, acompanhar uma pessoa na rede social ou sincronizar dinamicamente amigos e suas atividades, talvez você queira implementar a interface [ISocialSession2.](isocialsession2iunknown.md) 
    
- Em paralelo com a implementação de interfaces, teste e depure o provedor OSC. 

- Implante o provedor OSC.  

- Faça testes finais antes do lançamento.
    
## <a name="step-a-implementing-interfaces"></a>Etapa A: Implementando interfaces

Um provedor OSC implementa interfaces para que o OSC possa usar essas interfaces para obter informações necessárias sobre ou da rede social, por meio do provedor OSC. Essas informações incluem o seguinte:
  
- Como apresentar a caixa de diálogo de logon da conta para um usuário.    
- Se o provedor oferece suporte à exibição de amigos ou atividades conforme exibido na rede social.    
- Como exibir amigos e atividades no Cartão de Visita ou no Painel de Pessoas do Outlook.     
- Quando atualizar as informações de amigos ou atividades no Cartão de Visita ou no Painel de Pessoas.
    
As informações são normalmente passadas do provedor para o OSC, na forma de cadeias de caracteres XML como parâmetros de saída dos métodos de interface. O OSC e um provedor OSC estão em conformidade com o esquema XML do provedor OSC. Portanto, no decorrer da implementação das interfaces, você precisa ter um bom entendimento de como o esquema XML permite especificar informações conforme listado acima. 

Os recursos a seguir explicam como especificar XML para recursos do provedor, amigos e atividades:
  
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)    
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)    
- [Exemplo do XML de recursos](capabilities-xml-example.md)   
- [XML para recursos](xml-for-capabilities.md)    
- [Exemplo de XML de amigos](friends-xml-example.md)    
- [XML para amigos](xml-for-friends.md)   
- [Exemplo de XML de feed de atividades](activity-feed-xml-example.md)   
- [XML para atividades](xml-for-activities.md)
    
Antes de iniciar a implementação, consulte também os tópicos a seguir para economizar tempo posteriormente no processo de depuração:
  
- [Requisitos técnicos](technical-requirements.md)    
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)    
- [Modelos de exemplo do OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Etapa B: depuração

O tópico [Depurando um Provedor sugere](debugging-a-provider.md) procedimentos de depuração que você pode usar durante o desenvolvimento de um provedor osC. 
  
Enquanto estiver desenvolvendo, você também pode consultar Preparando-se para Lançar um Provedor [OSC](getting-ready-to-release-an-osc-provider.md) para entender melhor o comportamento esperado em determinados cenários (por exemplo, autenticação básica e baseada em formulários). 
  
## <a name="step-c-deploying"></a>Etapa C: Implantação

Consulte os tópicos a seguir para saber mais sobre os requisitos de implantação:
  
- [Implantar um provedor](deploying-a-provider.md)    
- [Registrar um provedor](registering-a-provider.md)   
- [Lista de verificação da instalação](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Etapa D: Teste final antes do lançamento

Dependendo da sua rede social e do provedor OSC, geralmente há testes específicos do provedor que você deve realizar antes de liberar seu provedor. Para obter uma lista sugerida de testes, consulte [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Confira também

- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

