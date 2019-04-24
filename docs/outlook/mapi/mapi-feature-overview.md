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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357712"
---
# <a name="mapi-feature-overview"></a>Visão geral do recurso MAPI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI tem vários recursos-chave que permitem que ele forneça uma maneira consistente de os desenvolvedores trabalharem com e usem sistemas de mensagens diferentes de modo perfeito. Esses recursos incluem uma interface de programação abrangente e aberta e suporte para padrões do setor. 
  
Como o MAPI é uma interface de programação aberta, ele fornece serviços de forma genérica, permitindo que os usuários adicionem qualquer personalização necessária agora e no futuro. A interface de programação MAPI cumpre os requisitos de aplicativos cliente com diversas necessidades de mensagens, como um aplicativo de processamento de texto que requer apenas a capacidade de enviar documentos ou um aplicativo de grupo de trabalho que exija a capacidade de compartilhar e armazenar diferentes tipos de dados. Na verdade, qualquer aplicativo que precise ser o Exchange ou armazenar informações em um formato específico pode se beneficiar da interface de programação MAPI. Qualquer provedor de serviços pode usar a interface para expor os recursos exclusivos de seu sistema de mensagens, selecionando os recursos que oferecem mais benefícios aos usuários de aplicativos.
  
O MAPI fornece separação entre a interface de programação usada pelos aplicativos cliente de mensagens de front-end e a interface de programação usada pelos provedores de serviços de back-end. A separação entre a interface de cliente e o provedor de serviços permite que um único aplicativo use vários sistemas de mensagens e vários aplicativos para usar um único provedor de serviços. Cada componente funciona com uma interface de usuário do Microsoft Windows comum. Esse é um grande benefício para os usuários. Os usuários podem selecionar entre vários sistemas, dependendo de suas necessidades a qualquer momento e podem trabalhar de forma consistente com cada sistema selecionado, fornecendo, assim, uma independência real dos sistemas de mensagens específicos. 
  
Por exemplo, um único aplicativo cliente de mensagens pode receber mensagens de um fax, caixa postal e um RSS feed. As mensagens de todos esses sistemas podem ser colocadas em um único local ou em uma caixa de entrada universal, na chegada. Ter um único aplicativo para lidar com todos esses sistemas reduz o custo de desenvolvimento, treinamento do usuário e administração do sistema. 
  
A separação da interface do cliente da interface do provedor remove quaisquer dependências de programação colocadas no aplicativo pelo sistema de mensagens e vice-versa. Os desenvolvedores de aplicativos cliente e provedores de serviços escrevem o código em um conjunto padrão de recursos MAPI, em vez de um conjunto variado de recursos específicos do aplicativo ou de sistema de mensagens. Os desenvolvedores se concentram apenas em seu componente, seja um cliente ou provedor de serviços, e o MAPI cuida do resto, reduzindo o tempo de desenvolvimento e os custos.
  
A interface de programação MAPI fornece um conjunto abrangente de recursos. O MAPI é destinado ao novo mercado poderoso de aplicativos de grupo de trabalho — aplicativos que se comunicam com sistemas de mensagens diferentes como fax, DEC All-in-1, correio de voz e serviços de comunicação pública, como os serviços do AT&T EasyLink, CompuServe e MCI Mala. A interface MAPI permite que os provedores de serviço sejam disponibilizados para todos esses sistemas. 
  
Os objetos compatíveis com MAPI são semelhantes nos objetos COM (Component Object Model). Os objetos COM implementam um conjunto de métodos que pertencem a uma ou mais interfaces ou coleções de funções relacionadas que definem como os objetos se comportam e operam em COM. Os usuários acessam objetos COM apenas por meio de ponteiros para essas interfaces.
  
O MAPI fornece suporte entre plataformas por meio de padrões da indústria como SMTP e X. 400. Você pode executar aplicativos MAPI no Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 e Windows XP. 
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

