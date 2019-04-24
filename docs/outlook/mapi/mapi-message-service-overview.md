---
title: Visão geral do serviço de mensagens MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8973cdcee2b10346d0ba07033357b50f7e9a6a27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345974"
---
# <a name="mapi-message-service-overview"></a>Visão geral do serviço de mensagens MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um serviço de mensagens define um grupo de provedores de serviços relacionados, geralmente provedores de serviços que funcionam com o mesmo sistema de mensagens. Enquanto os provedores de serviços realizam o trabalho de comunicação entre sistemas de mensagens e o subsistema MAPI, os serviços de mensagens executam o trabalho de interface entre o usuário e os provedores de serviço que funcionam com um sistema de mensagens comum.  
  
Os serviços de mensagens existem para facilitar a instalação e a configuração de provedores de serviços para os usuários. Os usuários nunca instalam ou configuram diretamente um provedor de serviços; o serviço de mensagens lida totalmente com a instalação e a configuração de cada um dos provedores de serviços que pertencem ao serviço. Devido a esse recurso, os usuários não precisam estar familiarizados com os requisitos de configuração específicos do provedor de serviços. 
  
A figura a seguir mostra a relação entre um aplicativo cliente baseado em mensagens e dois serviços de mensagens.
  
**Message service installation and configuration**
  
![Instalação e configuração do serviço de mensagens] (media/amapi_44.gif "Instalação e configuração do serviço de mensagens")
  
O usuário invoca o código de instalação de cada serviço de mensagens para adicionar o serviço e seus provedores de serviço a um perfil. Em um dos serviços de mensagens mostrados na figura, há três provedores de serviços; no outro serviço de mensagens, há dois provedores de serviços. Em algum momento posterior, após a conclusão da instalação, geralmente no momento do logon, os provedores de serviço em cada serviço de mensagens são configurados. O código de configuração em cada serviço de mensagens trata da configuração dos provedores no serviço.
  
Quando um serviço de mensagens é instalado, seu programa de instalação copia os arquivos necessários da origem de instalação para o disco local do usuário e atualiza um arquivo de configuração, MAPISVC. inf. O arquivo MAPISVC. inf contém definições de configuração para todos os serviços de mensagens e provedores de serviços que podem ser instalados no computador. Ele é organizado em seções hierárquicas, com links entre cada seção em cada nível. A seção no nível superior contém informações relevantes para o subsistema MAPI, como uma lista de todos os serviços de mensagens disponíveis e para a instalação da ajuda online. O próximo nível tem seções para cada serviço de mensagens, com informações como o nome de arquivo DLL do serviço de mensagens e o nome de sua função de ponto de entrada de configuração. O terceiro nível tem seções com dados de configuração para cada provedor de serviços no serviço de mensagens. 
  
Para lidar com a configuração, um serviço de mensagens implementa uma função de ponto de entrada que é compatível com um protótipo definido por MAPI, e uma caixa de diálogo com guias conhecida como folha de propriedades. MAPI chama a função de ponto de entrada para atender às solicitações de cliente relacionadas ao gerenciamento de perfil e ao gerenciamento de provedores de serviços no serviço de mensagens. As folhas de propriedades são usadas para exibir e alterar as propriedades de configuração do provedor de serviço e serviço de mensagens. 
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

