---
title: Visão geral do serviço de mensagem MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 56f124d7d42ac41e8b5cdb7cf61c9867bbf69837
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587527"
---
# <a name="mapi-message-service-overview"></a>Visão geral do serviço de mensagem MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um serviço de mensagem define um grupo de provedores de serviço relacionado, normalmente os provedores de serviços que funcionam com o mesmo sistema de mensagens. Enquanto os provedores de serviços de executam o trabalho de comunicação entre sistemas de mensagens e o subsistema MAPI, serviços de mensagem realizar o trabalho de interface entre o usuário e os provedores de serviços que funcionam com um sistema de mensagens comuns.  
  
Serviços de mensagens existem para facilitar a instalação e configuração dos provedores de serviços para os usuários. Usuários nunca diretamente instalar ou configurar um provedor de serviços; o serviço de mensagem completamente trata a instalação e configuração de cada um dos provedores de serviços que pertencem ao serviço. Devido a esse recurso, os usuários não precisará estar familiarizado com os requisitos de configuração de provedor de serviço específico. 
  
A figura a seguir mostra a relação entre dois serviços de mensagem e de um aplicativo cliente baseado em mensagens.
  
**Message service installation and configuration**
  
![Configuração e instalação do serviço de mensagem] (media/amapi_44.gif "Configuração e instalação do serviço de mensagem")
  
O usuário chama o código de instalação de cada serviço de mensagem para adicionar o serviço e seus provedores de serviço a um perfil. Em um dos serviços de mensagem mostrados na figura, há três provedores de serviços; o outro serviço de mensagem, há dois provedores de serviço. Em algum momento posterior após a instalação for concluída, geralmente no momento do logon, os provedores de serviços em cada serviço de mensagem são configurados. O código de configuração de cada serviço de mensagem lida com a configuração dos provedores no serviço.
  
Quando um serviço de mensagem é instalado, o seu programa de instalação copia os arquivos necessários da origem de instalação no disco local do usuário e atualiza um arquivo de configuração, Mapisvc. O arquivo Mapisvc contém definições de configuração para todos os serviços de mensagens e provedores de serviços que podem ser instalados no computador. Ele é organizado nas seções hierárquicas, com links entre cada seção em cada nível. Seção de nível superior contém informações relevantes para o subsistema MAPI, como uma lista de todos os serviços de mensagens disponível e para a instalação da Ajuda online. O próximo nível tem seções para cada serviço de mensagem, com informações como o nome do arquivo DLL do serviço de mensagem e o nome da sua função de ponto de entrada de configuração. O terceiro nível tem seções com dados de configuração para cada provedor de serviço no serviço de mensagem. 
  
Para lidar com a configuração, um serviço de mensagem implementa uma função de ponto de entrada que seja compatível com um protótipo definido por MAPI e uma caixa de diálogo tabulada conhecido como uma folha de propriedades. MAPI chama a função do ponto de entrada para solicitações de cliente de serviço relacionados ao gerenciamento de perfil e o gerenciamento dos provedores de serviço no serviço de mensagem. Folhas de propriedade são usadas para exibir e alterar propriedades de configuração de provedor de serviço e de serviço de mensagem. 
  
## <a name="see-also"></a>Confira também

- [Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

