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
ms.openlocfilehash: 36233d51f47c53d6a69494c0fcd799a7c83add29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567871"
---
# <a name="developing-a-mapi-message-store-provider"></a>Desenvolver um provedor do repositório de mensagens MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como outros provedores de serviço MAPI, armazenamentos de mensagem são bibliotecas de vínculos dinâmicos (DLLs) que apresentam os serviços de um mecanismo de armazenamento subjacente para aplicativos de cliente MAPI e o spooler MAPI. O provedor de armazenamento de mensagem apresenta o mecanismo de armazenamento subjacente como um conjunto hierárquico de pastas e mensagens de clientes MAPI e o MAPI spooler podem usar.
  
A ilustração a seguir mostra a arquitetura básica de repositório de mensagem MAPI.
  
**Message store architecture**
  
![Arquitetura de armazenamento de mensagens] (media/storearc.gif "Arquitetura de armazenamento de mensagens")
  
Você pode implementar um provedor de armazenamento de mensagem usando qualquer tipo de mecanismo de armazenamento subjacente que você gosta. No entanto, você precisa estar ciente questões de desempenho. Além disso, o mecanismo de armazenamento subjacente deve ser apresentado como um conjunto hierárquico de objetos MAPI. Esses requisitos média repositórios de mensagem são geralmente implementados por meio de um produto de banco de dados existente que suporta o armazenamento hierárquico de objetos no banco de dados e que tem uma interface de programação ou a estrutura de arquivo bem definida. Por exemplo, os bancos de dados do Microsoft Office Access, SQL e Oracle podem ser usados como o mecanismo de armazenamento subjacente. Alguns produtos de banco de dados tem conjuntos de recursos que tornam mais fácil implementar os recursos MAPI, portanto sua escolha de produto do banco de dados pode ser afetada pelos recursos que seu provedor de armazenamento de mensagem precisa suportar.
  
Usando um banco de dados existente como o subjacente salva do mecanismo de armazenamento que você trabalha porque é geralmente mais fácil presente objetos de banco de dados aos clientes MAPI como objetos MAPI que ao implementar seu próprio mecanismo de armazenamento hierárquico. Isso permite tratar operações MAPI em um nível superior que se você implementar seu próprio mecanismo de armazenamento hierárquico. Por exemplo, procurando por uma mensagem com uma linha de assunto específico se torna uma questão razoavelmente simple de Construindo e enviar uma consulta de banco de dados apropriado, ao invés de implementar as rotinas complexas para pesquisar seu mecanismo de armazenamento hierárquico.
  
Provedores de armazenamento de mensagem se comunicar com clientes MAPI e o spooler MAPI para executar operações em pastas e objetos. O provedor de armazenamento de mensagem converte essas operações em operações de nível inferiores no mecanismo de armazenamento subjacente. O spooler MAPI normalmente se comunica com o provedor de armazenamento de mensagem durante o envio e recebimento de mensagens. Clientes MAPI normalmente se comuniquem com provedores de repositório de mensagem para manipular a hierarquia de pasta e para ler, editar, excluir e enviar mensagens.
  
O spooler MAPI e clientes MAPI se comunicar com o provedor de armazenamento de mensagem para criar novas mensagens. Aplicativos cliente fazem isso quando os usuários redigir uma mensagem. O MAPI spooler faz isso quando ele recebe uma mensagem de entrada. Em ambos os casos, a nova mensagem geralmente é criada na pasta caixa de entrada do armazenamento de mensagens, se houver uma.
  
Provedores de armazenamento de mensagem fazer uso intenso de tabelas, pastas, mensagens e propriedades MAPI. Os detalhes da implementação para esses objetos são documentados no [MAPI tabelas](mapi-tables.md), [Pastas MAPI](mapi-folders.md), [Mensagens MAPI](mapi-messages.md)e [Visão geral da propriedade de MAPI](mapi-property-overview.md). Você deve familiarizar com esse material antes de tentar implementar um provedor de armazenamento de mensagem.
  
Existem dois tipos importantes de provedores de armazenamento de mensagem: aqueles que podem agir como o padrão de um usuário de mensagens repositório e aqueles que não é possível. Um armazenamento de mensagens padrão é um no qual cliente aplicativos e o MAPI spooler podem executar qualquer tarefa de mensagens, como o recebimento de mensagens ou a criação de pastas. Um provedor de armazenamento de mensagem padrão deve oferecer suporte a vários recursos mais que o número mínimo necessário para todos os provedores de armazenamento de mensagem.
  
## <a name="see-also"></a>Confira também

- [Conceitos MAPI](mapi-concepts.md)

