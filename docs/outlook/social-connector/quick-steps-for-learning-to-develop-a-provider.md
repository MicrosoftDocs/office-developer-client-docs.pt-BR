---
title: Etapas rápidas para aprender a desenvolver um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13c0ae8c-d268-4bf0-942d-2a6160142f5e
description: Este tópico sugere algumas etapas para aprender a desenvolver um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 581997ab257d59062761d97bfef49a88b90bb1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329215"
---
# <a name="quick-steps-for-learning-to-develop-a-provider"></a>Etapas rápidas para aprender a desenvolver um provedor

Para desenvolver um provedor do OSC, é necessário concluir as seguintes etapas gerais:
  
- Implemente as quatro interfaces obrigatórias: [ISocialProvider](isocialprovideriunknown.md), [ISocialSession](isocialsessioniunknown.md), [métodoisocialprofile](isocialprofileisocialperson.md)e [ISocialPerson](isocialpersoniunknown.md). Dependendo do suporte de sua rede social para armazenar em cache credenciais de logon, seguindo uma pessoa na rede social ou sincronizando amigos e suas atividades dinamicamente, talvez você queira implementar a interface [ISocialSession2](isocialsession2iunknown.md) . 
    
- Em paralelo com a implementação de interfaces, teste e depure o provedor do OSC. 

- Implantar o provedor OSC.  

- Teste final antes do lançamento.
    
## <a name="step-a-implementing-interfaces"></a>Etapa A: implementar interfaces

Um provedor OSC implementa interfaces para que o OSC possa usar essas interfaces para obter as informações necessárias sobre ou da rede social, através do provedor OSC. Essas informações incluem o seguinte:
  
- Como apresentar a caixa de diálogo de logon da conta a um usuário.    
- Se o provedor oferece suporte para mostrar amigos ou atividades, conforme exibido na rede social.    
- Como exibir amigos e atividades no cartão de visita ou no painel de pessoas do Outlook.     
- Quando atualizar as informações de amigos ou atividades no cartão de visita ou no painel de pessoas.
    
Normalmente, as informações são passadas do provedor para o OSC, na forma de cadeias de caracteres XML como parâmetros de saída dos métodos de interface. O provedor OSC e o do OSC estão em conformidade com o esquema XML do provedor OSC. Portanto, ao longo da implementação das interfaces, você precisa de uma boa compreensão de como o esquema XML permite que você especifique as informações listadas acima. 

Os recursos a seguir explicam como especificar XML para recursos de provedor, amigos e atividades:
  
- [Sequências de chamada típicas do OSC](osc-typical-calling-sequences.md)    
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)    
- [Exemplo do XML de recursos](capabilities-xml-example.md)   
- [XML para recursos](xml-for-capabilities.md)    
- [Exemplo de XML de amigos](friends-xml-example.md)    
- [XML para amigos](xml-for-friends.md)   
- [Exemplo de XML de feed de atividades](activity-feed-xml-example.md)   
- [XML para atividades](xml-for-activities.md)
    
Antes de começar a implementação, consulte também os tópicos a seguir para poupar tempo mais tarde no processo de depuração:
  
- [Requisitos técnicos](technical-requirements.md)    
- [Práticas recomendadas para o desenvolvimento de um provedor](best-practices-for-developing-a-provider.md)    
- [Modelos de exemplo do OSC](osc-sample-templates.md)
    
## <a name="step-b-debugging"></a>Etapa B: depuração

O tópico [Debugging a Provider](debugging-a-provider.md) sugere procedimentos de depuração que você pode usar ao desenvolver um provedor do OSC. 
  
Durante o desenvolvimento, você também pode se referir a [preparar para liberar um provedor do OSC](getting-ready-to-release-an-osc-provider.md) para obter uma compreensão melhor do comportamento esperado em determinados cenários (por exemplo, autenticação básica e baseada em formulários). 
  
## <a name="step-c-deploying"></a>Etapa C: implantação

Consulte os tópicos a seguir para saber mais sobre os requisitos de implantação:
  
- [Implantar um provedor](deploying-a-provider.md)    
- [Registrar um provedor](registering-a-provider.md)   
- [Lista de verificação da instalação](installation-checklist.md)
    
## <a name="step-d-final-testing-before-release"></a>Etapa D: teste final antes do lançamento

Dependendo da sua rede social e do provedor OSC, há normalmente testes específicos do provedor que você deve executar antes de liberar seu provedor. Para obter uma lista de testes sugeridos, consulte [preparando-se para liberar um provedor do OSC](getting-ready-to-release-an-osc-provider.md).
  
## <a name="see-also"></a>Confira também

- [Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

