---
title: Desenvolvendo um aplicativo cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410032"
---
# <a name="developing-a-mapi-client-application"></a>Desenvolvendo um aplicativo cliente MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente MAPI são escritos com a interface de cliente MAPI orientada ao objeto. Os clientes MAPI interagem com um ou mais sistemas de mensagens por meio do subsistema MAPI e provedores de serviços compatíveis com MAPI. Essa interação pode ocorrer de várias maneiras diferentes; há uma enorme variedade em aplicativos cliente. A maioria dos clientes são clientes de mensagens, integrando mensagens ao conjunto de recursos estabelecido ou executando mensagens como seu recurso principal. Outros recursos que os clientes MAPI podem fornecer incluem a administração de perfil ou o livro de endereços e o gerenciamento de armazenamento de mensagens.
  
Todos os clientes de mensagens inicializam as bibliotecas MAPI e iniciam **uma sessão com** o subsistema MAPI. Para obter mais informações, [consulte Acessando objetos usando a sessão.](accessing-objects-by-using-the-session.md) Depois que uma sessão é estabelecida, um cliente pode:
  
- Lidar com mensagens de saída, incluindo respostas, mensagens encaminhadas e retransmissões.
    
- Manipular mensagens de entrada.
    
- Manipular o armazenamento de mensagens abrindo pastas e mensagens, criando, modificando, copiando e enviando mensagens, acompanhando conversas e pesquisando uma ou mais pastas.
    
- Manipular o livro de endereços criando e modificando destinatários, localizando entradas e percorrendo a hierarquia do contêiner.
    
- Manipular um provedor de transporte executando reconfiguração, definindo opções e ordem de transporte e enviando mensagens sob demanda.
    
- Manipular notificação de evento.
    
- Manipular formulários.
    
- Manipular perfis e serviços de mensagens.
    
Use os tópicos desta seção para ajudá-lo a implementar essas tarefas básicas e os recursos específicos que tornarão seu cliente MAPI exclusivo.
  

