---
title: Visão geral de formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432517"
---
# <a name="mapi-forms-overview"></a>Visão geral de formulários MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um formulário MAPI é um visualizador de uma mensagem. Cada mensagem tem uma classe de mensagem que dita o formulário específico que é usado como seu visualizador. MAPI define várias classes de mensagem e implementou os formulários para exibir mensagens dessas classes. Os desenvolvedores de software cliente podem criar novas classes de mensagens e formulários personalizados para exibir mensagens criadas usando as novas classes.
  
Cada formulário personalizado implementa um conjunto de comandos de menu padrão, como **Abrir,** **Criar,** Excluir e **Responder,** e um conjunto de comandos específicos para o formulário específico. Alguns dos comandos de formulário são integrados à interface do usuário do aplicativo cliente quando o formulário está ativo; outros comandos de formulário substituem completamente os comandos do cliente. 
  
A ilustração a seguir mostra a relação entre os componentes MAPI envolvidos no uso de formulários. 
  
**MAPI form architecture**
  
![MapI form architecture](media/forms01.gif "MAPI form architecture")
  
No diagrama, observe que o gerenciador de formulário desempenha uma função semelhante a outros provedores de serviços MAPI, embora não seja um provedor de serviços em si. O gerenciador de formulário é uma DLL substituível que implementa algumas das interfaces MAPI. Embora os desenvolvedores possam implementar seu próprio gerenciador de formulário, a maioria dos ambientes usará o gerenciador de formulário fornecido pela Microsoft devido à complexidade do gerenciador de formulário.
  
A lista a seguir descreve os componentes no diagrama e sua relação com outros componentes:
  
- Cliente de mensagens: um aplicativo que pode usar objetos de formulário. O cliente de mensagens usa as interfaces de formulário MAPI para se comunicar com o gerenciador de formulário para carregar mensagens em objetos de formulário.
    
- Interfaces de formulário MAPI: um padrão definido para comunicação entre componentes MAPI relacionados a formulários.
    
- Gerenciador de formulários: a DLL que os clientes de mensagens usam para manipular a instalação de formulários em bibliotecas de formulários, o carregamento de servidores de formulários e a comunicação inicial entre clientes de mensagens e servidores de formulários.
    
- Bibliotecas de formulário: Armazenamento permanente para os arquivos executáveis associados a servidores de formulário.
    
- Servidores de formulário: arquivos executáveis que implementam um formulário. Os servidores de formulário criam objetos de formulário e interfaces de usuário para lidar com mensagens específicas. Esse executável também é um servidor OLE e segue as convenções OLE usuais.
    
- Objetos de formulário: objetos de tempo de executar criados por servidores de formulário que correspondem a mensagens específicas. Os objetos de formulário são executados no mesmo contexto de processo que seu servidor de formulário.
    
Para obter mais informações sobre componentes de formulário MAPI, consulte [MAPI Forms](mapi-forms.md).
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

