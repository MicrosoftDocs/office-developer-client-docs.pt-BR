---
title: Desenvolvendo um aplicativo de cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 42558fcc3d94b108c0dabb92d62f7c61fdf3039f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766404"
---
# <a name="developing-a-mapi-client-application"></a>Desenvolvendo um aplicativo de cliente MAPI

  
  
**Aplica-se a**: Outlook 
  
Aplicativos de cliente MAPI são gravados com a interface de cliente MAPI orientada a objeto. Clientes MAPI interagem com um ou mais sistemas de mensagens por meio do subsistema MAPI e os provedores de serviço compatível com MAPI. Essa interação pode ocorrer de várias maneiras diferentes; Não há uma enorme variedade em aplicativos cliente. A maioria dos clientes são mensagens de clientes, a integração de mensagens em seu conjunto de recursos estabelecidas ou realização de mensagens como seu recurso principal. Outros recursos que podem fornecer a clientes MAPI incluem a administração de perfil ou gerenciamento de repositório de mensagem e catálogo de endereços.
  
Todos os clientes de mensagens inicializar as bibliotecas MAPI e iniciar uma **sessão** com o subsistema de MAPI. Para obter mais informações, consulte [Acessando objetos usando a sessão](accessing-objects-by-using-the-session.md). Depois que uma sessão tiver sido estabelecida, um cliente pode:
  
- Trata as mensagens de saída, incluindo respostas, encaminhadas mensagens e retransmissões.
    
- Trata as mensagens de entrada.
    
- Lidar com o armazenamento de mensagens por abrindo pastas e mensagens, criando, modificando, copiar e envio de mensagens, conversas de acompanhamento e uma ou mais pastas de pesquisa.
    
- Manipule o catálogo de endereços, criação e modificação de destinatários, localizar entradas e atravessando a hierarquia de contêiner.
    
- Lidar com um provedor de transporte executando reconfiguração, definindo opções e transporte de ordem, e enviando mensagens sob demanda.
    
- Manipule notificações de evento.
    
- Lidar com formulários.
    
- Lidar com perfis e serviços de mensagem.
    
Use os tópicos desta seção para ajudá-lo a implementar essas tarefas básicas e os recursos específicos que tornarão seu cliente MAPI exclusivo.
  

