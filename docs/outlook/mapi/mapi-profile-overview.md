---
title: Visão geral do perfil MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328158"
---
# <a name="mapi-profile-overview"></a>Visão geral do perfil MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um perfil é uma coleção de informações sobre os serviços de mensagens e provedores de serviços que um usuário de um aplicativo cliente deseja que esteja disponível durante uma sessão MAPI específica. Todos os usuários têm pelo menos um perfil; muitos usuários mantêm vários. Por exemplo, um usuário pode ter um perfil para trabalhar com um serviço de armazenamento de mensagens baseado em servidor e outro perfil para trabalhar com um serviço de armazenamento de mensagens no computador local. Um usuário pode querer acessar um conjunto de sistemas de mensagens usando os serviços de transporte apropriados por parte do dia e outro conjunto para o resto do dia. Os perfis fornecem uma maneira flexível de selecionar combinações de serviços do sistema de mensagens. 
  
Os perfis podem ter nomes de até 64 caracteres alfanuméricos de comprimento. Os nomes podem incluir caracteres de destaque, sublinhado e espaços incorporados e não podem incluir espaços à esquerda ou à direita. 
  
Os perfis são organizados hierarquicamente e divididos em seções, com uma seção para cada serviço de mensagens e uma seção para cada provedor de serviços em um serviço. As seções relacionadas são vinculadas, facilitando a navegação nas informações. Cada seção contém uma série de entradas que o MAPI ou um aplicativo cliente usa para configuração.
  
As entradas incluídas em um perfil variam de serviço de mensagens para serviço de mensagens. Algumas das entradas comuns incluem o seguinte:
  
- O nome de cada serviço de mensagens ou provedor de serviços.
    
- O nome das DLLs que contêm provedores de serviço e serviços de mensagens.
    
- O nome da função de ponto de entrada de cada serviço de mensagens.
    
- Uma lista dos provedores de serviços que compõem cada serviço de mensagens.
    
Os perfis podem ser criados no momento da instalação, quando MAPI ou um serviço de mensagens é carregado em um computador ou em qualquer momento posterior. MAPI fornece o assistente de perfil para administração de perfil. 
  
O assistente de perfil é um aplicativo que cria novos perfis com uma quantidade mínima de trabalho. O assistente usa valores padrão para as configurações sempre que possível, poupando tempo e esforço dos usuários. Os usuários inserem valores somente quando é absolutamente necessário. Para obter mais informações, consulte [criando um perfil usando o assistente de perfil](creating-a-profile-by-using-the-profile-wizard.md). Você também pode usar a ferramenta de personalização do Office para criar um novo perfil. Para obter mais informações, consulte [Ferramenta de Personalização do Office](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Confira também



[Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

