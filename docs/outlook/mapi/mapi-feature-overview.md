---
title: Visão geral do recurso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1ff3677a2bbc8ca54e5bc96ae1e873e3efd3c6bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767848"
---
# <a name="mapi-feature-overview"></a>Visão geral do recurso MAPI
 
**Aplica-se a**: Outlook 
  
MAPI tem vários recursos principais que habilitá-lo oferecer uma maneira consistente para desenvolvedores trabalhar com e usar diferentes sistemas de mensagens de forma direta. Esses recursos incluem uma abrangente e abrir a interface de programação e suportam para os padrões do setor. 
  
Como MAPI é uma interface de programação aberta, ele fornece serviços de uma maneira genérica, permitindo que os usuários adicionem qualquer personalização necessária agora e no futuro. A interface de programação de MAPI atenda aos requisitos dos aplicativos de cliente com várias necessidades de mensagens, como um aplicativo de processamento de palavras que requer apenas a capacidade de enviar documentos ou um aplicativo de grupo de trabalho que requer a capacidade de compartilhar e Armazene os diferentes tipos de dados. Na verdade, qualquer aplicativo que precisa para trocar ou armazenar informações em um determinado formato pode aproveitar a interface de programação de MAPI. Qualquer provedor de serviços pode usar a interface para expor recursos exclusivos de seu sistema de mensagens, selecionando os recursos que fornecem o máximo benefício aos usuários de aplicativo.
  
MAPI fornece a separação entre a interface de programação usada pelos aplicativos cliente mensagens front-end e a interface de programação usado pelos provedores de serviço back-end. Separando a interface do cliente do provedor do serviço permite que um único aplicativo usar vários sistemas de mensagens e vários aplicativos para usar um provedor de serviço único. Cada componente funciona com uma interface de usuário baseada em Windows Microsoft comum. Isso é uma grande vantagem aos usuários. Os usuários podem selecionar uma variedade de sistemas, dependendo das suas necessidades por vez e podem trabalhar consistentemente com cada sistema selecionado, proporcionando true independência de sistemas de mensagens específicas. 
  
Por exemplo, um único aplicativo cliente de mensagens poderá receber mensagens de um fax, caixa postal e um RSS feed. Mensagens de todos esses sistemas podem ser colocadas em um único local ou universal caixa de entrada, na chegada. Ter um único aplicativo lidar com todos esses sistemas reduz o custo de desenvolvimento, treinamento do usuário e administração do sistema. 
  
Separando a interface de cliente da interface do provedor remove quaisquer dependências de programação colocadas no aplicativo pelo sistema de mensagens e vice-versa. Desenvolvedores de aplicativos cliente e provedores de serviços de escrevem código para um conjunto padrão de recursos do MAPI, em vez de uma gama de recursos específicos do sistema de mensagens ou de aplicativo específico. Os desenvolvedores focalizar seus componentes, apenas se ele é um provedor de cliente ou serviço e MAPI manipula o restante, reduzindo custos e o tempo de desenvolvimento.
  
A interface de programação de MAPI fornece um conjunto abrangente de recursos. MAPI é destinado ao mercado novo poderoso de aplicativos do grupo de trabalho — aplicativos que se comunicam com tais diferentes sistemas de mensagens como fax, All-In de dez-1, caixa postal e serviços de comunicação pública, como AT & T Easylink serviços, CompuServe e MCI EMAIL. A interface MAPI permite que os provedores de serviço fique disponível para todos esses sistemas. 
  
Objetos compatível com MAPI são semelhantes no formulário aos objetos de modelo COM (Component Object). Objetos COM implementam um conjunto de métodos que pertencem a uma ou mais interfaces ou conjuntos de funções relacionadas que definem como os objetos se comportam e operam em COM. Os usuários acessar objetos COM apenas por meio de ponteiros para essas interfaces.
  
MAPI oferece suporte a plataforma cruzada por meio de tais padrões do setor como SMTP e x. 400. Você pode executar aplicativos MAPI no Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 e Windows XP. 
  
## <a name="see-also"></a>Confira também

- [Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

