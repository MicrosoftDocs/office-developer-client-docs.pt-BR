---
title: Desenvolver um provedor do repositório de mensagens MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 83692674-0b5a-468d-9cd7-a2ac3d140bda
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 76332b57b2957b5682efb415121ea6db42409c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412608"
---
# <a name="developing-a-mapi-message-store-provider"></a>Desenvolver um provedor do repositório de mensagens MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como outros provedores de serviços MAPI, os armazenamentos de mensagens são bibliotecas de vínculo dinâmico (DLLs) que apresentam os serviços de um mecanismo de armazenamento subjacente para aplicativos cliente MAPI e o spooler MAPI. O provedor de armazenamento de mensagens apresenta o mecanismo de armazenamento subjacente como um conjunto hierárquico de pastas e mensagens que os clientes MAPI e o spooler MAPI podem usar.
  
A ilustração a seguir mostra a arquitetura básica do armazenamento de mensagens MAPI.
  
**Message store architecture**
  
![Arquitetura do armazenamento de mensagens Arquitetura]do armazenamento de(media/storearc.gif "mensagens")
  
Você pode implementar um provedor de armazenamento de mensagens usando qualquer tipo de mecanismo de armazenamento subjacente que quiser. No entanto, você precisa estar ciente das preocupações de desempenho. Além disso, o mecanismo de armazenamento subjacente deve ser apresentado como uma coleção hierárquica de objetos MAPI. Esses requisitos significam que os armazenamentos de mensagens geralmente são implementados usando um produto de banco de dados existente que oferece suporte ao armazenamento hierárquico de objetos no banco de dados e que tem uma interface de programação ou estrutura de arquivos bem definida. Por exemplo, os bancos de dados do Microsoft Office Access, SQL e Oracle podem ser usados como o mecanismo de armazenamento subjacente. Alguns produtos de banco de dados têm conjuntos de recursos que facilitam a implementação de recursos MAPI, portanto, sua escolha do produto de banco de dados pode ser afetada pelos recursos que seu provedor de armazenamento de mensagens precisa suportar.
  
O uso de um banco de dados existente como mecanismo de armazenamento subjacente salva seu trabalho porque é geralmente mais fácil apresentar objetos de banco de dados para clientes MAPI como objetos MAPI do que implementar seu próprio mecanismo de armazenamento hierárquico. Isso permite tratar as operações MAPI em um nível mais alto do que se você implementar seu próprio mecanismo de armazenamento hierárquico. Por exemplo, procurar uma mensagem com uma linha de assunto específica se torna uma questão bastante simples de construir e enviar uma consulta de banco de dados apropriada, em vez de implementar rotinas complexas para pesquisar seu mecanismo de armazenamento hierárquico.
  
Os provedores de armazenamento de mensagens se comunicam com clientes MAPI e o spooler MAPI para executar operações em pastas e objetos. O provedor de armazenamento de mensagens converte essas operações em operações de nível inferior no mecanismo de armazenamento subjacente. O spooler MAPI normalmente se comunica com o provedor de armazenamento de mensagens ao enviar e receber mensagens. Os clientes MAPI normalmente se comunicam com provedores de armazenamento de mensagens para manipular a hierarquia de pastas e ler, editar, excluir e enviar mensagens.
  
Tanto o spooler MAPI quanto os clientes MAPI se comunicam com o provedor de armazenamento de mensagens para criar novas mensagens. Os aplicativos cliente fazem isso quando os usuários compõem uma mensagem. O spooler MAPI faz isso quando recebe uma mensagem de entrada. Em ambos os casos, a nova mensagem geralmente é criada na pasta Caixa de Entrada do armazenamento de mensagens, se houver uma.
  
Os provedores de armazenamento de mensagens fazem uso intenso de tabelas, pastas, mensagens e propriedades MAPI. Os detalhes de implementação para esses objetos estão documentados em tabelas [MAPI,](mapi-tables.md)pastas [MAPI,](mapi-folders.md)mensagens [MAPI](mapi-messages.md)e visão [geral da propriedade MAPI](mapi-property-overview.md). Você deve se familiarizar com esse material antes de tentar implementar um provedor de armazenamento de mensagens.
  
Há dois tipos importantes de provedores de armazenamento de mensagens: aqueles que podem atuar como o armazenamento de mensagens padrão de um usuário e aqueles que não podem. Um armazenamento de mensagens padrão é aquele em que os aplicativos cliente e o spooler MAPI podem executar qualquer tarefa de mensagens, como receber mensagens ou criar pastas. Um provedor de armazenamento de mensagens padrão deve suportar vários recursos a mais do que o número mínimo necessário para todos os provedores de armazenamento de mensagens.
  
## <a name="see-also"></a>Confira também

- [Conceitos de MAPI](mapi-concepts.md)

