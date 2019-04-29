---
title: Desenvolver um aplicativo cliente MAPI
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
# <a name="developing-a-mapi-client-application"></a>Desenvolver um aplicativo cliente MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos clientes MAPI são escritos com a interface de cliente MAPI orientada a objeto. Os clientes MAPI interagem com um ou mais sistemas de mensagens por meio do subsistema MAPI e provedores de serviço compatíveis com MAPI. Essa interação pode ocorrer de várias maneiras diferentes; Há uma enorme variedade de aplicativos cliente. A maioria dos clientes são clientes de mensagens, integrando o sistema de mensagens ao conjunto de recursos estabelecidos ou realizando mensagens como seu recurso principal. Outros recursos que os clientes MAPI podem fornecer incluem administração de perfil ou catálogo de endereços e gerenciamento de repositório de mensagens.
  
Todos os clientes de mensagens inicializam as bibliotecas MAPI e iniciam uma **sessão** com o subsistema MAPI. Para obter mais informações, consulte acEssando [objetos usando a sessão](accessing-objects-by-using-the-session.md). Depois que uma sessão for estabelecida, um cliente poderá:
  
- Gerenciar mensagens de saída, incluindo respostas, mensagens encaminhadas e retransmissões.
    
- Lidar com mensagens de entrada.
    
- Manipule o repositório de mensagens abrindo pastas e mensagens, criando, modificando, copiando e enviando mensagens, controlando conversas e pesquisando uma ou mais pastas.
    
- Manipule o catálogo de endereços criando e modificando destinatários, localizando entradas e atravessando a hierarquia de contêineres.
    
- Gerenciar um provedor de transporte executando reconfiguração, definindo opções e ordem de transporte e enviando mensagens sob demanda.
    
- Lidar com notificações de eventos.
    
- Manipular formulários.
    
- Gerenciar perfis e serviços de mensagens.
    
Use os tópicos desta seção para ajudá-lo a implementar essas tarefas básicas e os recursos específicos que farão com que seu cliente MAPI seja exclusivo.
  

