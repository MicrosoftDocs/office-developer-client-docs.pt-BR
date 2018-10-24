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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385624"
---
# <a name="mapi-profile-overview"></a>Visão geral do perfil MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um perfil é uma coleção de informações sobre os serviços de mensagens e provedores de serviços que um usuário de um aplicativo cliente quer esteja disponível durante uma determinada sessão MAPI. Cada usuário tenha pelo menos um perfil; muitos usuários manter vários. Por exemplo, um usuário pode ter um perfil para trabalhar com um serviço de repositório de mensagens baseado em servidor e outro perfil para trabalhar com um serviço de repositório de mensagem no computador local. Um usuário talvez queira acessar um conjunto de sistemas de mensagens usando os serviços de transporte adequado para a parte do dia e outro conjunto para o restante do dia. Perfis fornecem uma maneira flexível para selecionar combinações de serviços do sistema de mensagens. 
  
Perfis podem ter até 64 caracteres alfanuméricos os nomes de comprimento. Os nomes podem incluir espaços incorporados, o sublinhado e ênfase caracteres e não podem conter espaços à esquerda ou à direita. 
  
Perfis são organizados hierarquicamente e divididos em seções, com uma seção para cada serviço de mensagem e uma seção para cada provedor de serviços em um serviço. As seções relacionadas são vinculadas, tornando mais fácil navegar as informações. Cada seção contém uma série de entradas MAPI ou um aplicativo cliente usa para configuração.
  
As entradas incluídas em um perfil variam de serviço de mensagem para o serviço de mensagem. Algumas das entradas comuns incluem o seguinte:
  
- O nome de cada serviço de mensagem ou o provedor de serviços.
    
- O nome de DLLs que contêm os provedores de serviço e serviços de mensagem.
    
- O nome da função do ponto de entrada do serviço de cada mensagem.
    
- Uma lista dos provedores de serviços que constituem cada serviço de mensagem.
    
Perfis podem ser criados no momento da instalação, quando o MAPI ou um serviço de mensagem for carregado em um computador, ou a qualquer momento posterior. MAPI fornece o Assistente de perfil para administração de perfil. 
  
O Assistente de perfil é um aplicativo que cria novos perfis com uma quantidade mínima de trabalho. O assistente usa valores padrão para configurações sempre que possível, economizando esforço e tempo dos usuários. Os usuários inserem valores somente quando absolutamente necessário. Para obter mais informações, consulte o [tópico Criando um perfil usando o Assistente de perfil](creating-a-profile-by-using-the-profile-wizard.md). Você também pode usar a ferramenta de personalização do Office para criar um novo perfil. Para obter mais informações, consulte [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).
  
## <a name="see-also"></a>Confira também



[Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

