---
title: Visão geral do recurso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b1087f5156ad79b20eb31ef55c0388ffd82e1601
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416920"
---
# <a name="mapi-feature-overview"></a>Visão geral do recurso MAPI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI tem vários recursos importantes que permitem que ele forneça uma maneira consistente para os desenvolvedores trabalharem com e usarem diferentes sistemas de mensagens de maneira perfeita. Esses recursos incluem uma interface de programação abrangente e aberta e suporte para padrões do setor. 
  
Como o MAPI é uma interface de programação aberta, ele fornece serviços de maneira genérica, permitindo que os usuários adicionem qualquer personalização necessária agora e no futuro. A interface de programação MAPI atende aos requisitos de aplicativos cliente com diversas necessidades de mensagens, como um aplicativo de processamento de texto que requer apenas a capacidade de enviar documentos ou um aplicativo de grupo de trabalho que requer a capacidade de compartilhar e armazenar diferentes tipos de dados. Na verdade, qualquer aplicativo que precise trocar ou armazenar informações em um formato específico pode se beneficiar da interface de programação MAPI. Qualquer provedor de serviços pode usar a interface para expor os recursos exclusivos de seu sistema de mensagens, selecionando os recursos que oferecem mais benefícios aos usuários de aplicativos.
  
MAPI provides separation between the programming interface used by the front-end messaging client applications and the programming interface used by the back-end service providers. Separar a interface do cliente do provedor de serviços permite que um único aplicativo use vários sistemas de mensagens e vários aplicativos para usar um único provedor de serviços. Cada componente funciona com uma interface de usuário comum baseada no Microsoft Windows. Esse é um ótimo benefício para os usuários. Os usuários podem selecionar de uma variedade de sistemas, dependendo de suas necessidades a qualquer momento, e podem trabalhar consistentemente com cada sistema selecionado, fornecendo, assim, independência verdadeira de sistemas de mensagens específicos. 
  
Por exemplo, um único aplicativo cliente de mensagens pode receber mensagens de um fax, caixa postal e um RSS feed. As mensagens de todos esses sistemas podem ser colocadas em um único local, ou na Caixa de Entrada universal, na chegada. Ter um único aplicativo lida com todos esses sistemas diminui o custo de desenvolvimento, treinamento de usuários e administração do sistema. 
  
Separar a interface do cliente da interface do provedor remove quaisquer dependências de programação colocadas no aplicativo pelo sistema de mensagens e vice-versa. Os desenvolvedores de aplicativos cliente e provedores de serviços escrevem código em um conjunto padrão de recursos MAPI, em vez de um conjunto diversificado de recursos específicos do aplicativo ou do sistema de mensagens. Os desenvolvedores se concentram apenas no componente, seja um cliente ou provedor de serviços, e o MAPI lida com o resto, reduzindo o tempo de desenvolvimento e os custos.
  
A interface de programação MAPI fornece um conjunto abrangente de recursos. O MAPI destina-se ao poderoso novo mercado de aplicativos de grupo de trabalho — aplicativos que se comunicam com diferentes sistemas de mensagens, como fax, DEC All-In-1, caixa postal e serviços de comunicações públicas, como AT&T Easylink Services, CompuServe e MCI MAIL. A interface MAPI permite que os provedores de serviços sejam disponibilizados para todos esses sistemas. 
  
Os objetos compatíveis com MAPI são semelhantes aos objetos COM (Component Object Model). Os objetos COM implementam um conjunto de métodos que pertencem a uma ou mais interfaces ou coleções de funções relacionadas que definem como os objetos se comportam e operam no COM. Os usuários acessam objetos COM somente por meio de ponteiros para essas interfaces.
  
A MAPI oferece suporte a plataforma cruzada por meio de padrões do setor como SMTP e X.400. Você pode executar aplicativos MAPI no Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 e Windows XP. 
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

