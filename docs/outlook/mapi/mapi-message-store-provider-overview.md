---
title: Visão geral do provedor de armazenamento de mensagem MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5cc8261dfee6803492ffcf62c182930e2ac6d425
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767898"
---
# <a name="mapi-message-store-provider-overview"></a>Visão geral do provedor de armazenamento de mensagem MAPI
  
**Aplica-se a**: Outlook 
  
Provedores de armazenamento de mensagem lidar com o armazenamento e a recuperação de mensagens e outras informações para os usuários de aplicativos do cliente. As informações da mensagem são organizadas por meio de um sistema hierárquico conhecido como um armazenamento de mensagens. O armazenamento de mensagens é implementado em vários níveis, com chamadas pastas que contêm mensagens de diferentes tipos de contêineres. Não há nenhum limite no número de níveis em um armazenamento de mensagem. pastas podem conter muitas subpastas. 
  
A ilustração a seguir mostra a arquitetura de armazenamento de mensagem hierárquico.
  
**Message store architecture**
  
![Arquitetura de armazenamento de mensagens] (media/amapi_03.gif "Arquitetura de armazenamento de mensagens")
  
A figura mostra duas pastas, um com uma subpasta. Os usuários do aplicativo cliente podem acessar um modo de exibição de resumo das mensagens contidos em cada pasta ou visualizá-las individualmente com um formulário. Se o cliente exibe um formulário personalizado que fornece um desenvolvedor de formulário ou um formulário padrão que fornece MAPI depende do tipo ou classe da mensagem. A primeira pasta contém mensagens de nota e usa o formulário de anotação padrão de MAPI. A segunda pasta contém mensagens de solicitação de inventário e usa um formulário personalizado do estoque. As informações em ambos os formulários representam as propriedades da mensagem.
  
Você pode usar os dados do repositório de mensagens de várias maneiras. Além de usar os dados para email tradicional, você pode usar pastas como um fórum de discussão pública, como um repositório para documentos de referência, ou como um contêiner para caixa postal, calendário, contatos ou tarefas, por exemplo. Um repositório de mensagem única pode conter vários tipos de informações. Vários clientes podem instalar o mesmo armazenamento de mensagens. Isso faz com que o compartilhamento de dados de forma fácil e rápida. 
  
Pastas do repositório de mensagens permitem que você deve classificar e filtrar mensagens e personalize a exibição de mensagem em uma interface de usuário. Links para mensagens filtradas são mantidos nas pastas especiais chamadas de pastas de resultados de pesquisa. O usuário de um aplicativo cliente insere os critérios de filtragem, que MAPI se refere a como uma restrição, e os critérios é aplicado às mensagens armazenadas em pastas de um ou mais. Por exemplo, um usuário talvez queira exibir somente as mensagens que lidam com um assunto específico e com datas de chegada que são mais recentes do que a última semana. Referências para as mensagens que correspondem aos critérios estão listadas na pasta de pesquisa e as mensagens reais permanecem em suas pastas regulares.
  
As mensagens são as unidades de dados que são transferidos de um usuário ou aplicativo para outro usuário ou aplicativo. Cada mensagem contém alguns texto da mensagem, com formatação simples ou complexa e informações de envelope de mensagem que são usadas para a transmissão. Algumas mensagens incluem um ou mais anexos ou dados adicionais relacionadas a e transportados com uma mensagem na forma de um arquivo, outra mensagem ou um objeto OLE. 
  
Dependendo da mensagem o provedor de armazenamento, um usuário pode salvar uma nova mensagem sendo gravada além às mensagens que foram enviadas ou recebidas. As mensagens podem ser copiadas ou movidas de uma pasta para outro, com cada cópia se tornando uma mensagem separada que pode ser copiada, excluída ou modificada individualmente. Outro recurso que algumas mensagem armazenar provedores enable é a capacidade de alterar uma mensagem depois que ela foi recebida e armazená-lo novamente em sua pasta. Um usuário pode tirar proveito desse recurso para girar uma mensagem de fax chegou cabeça para baixo. O usuário pode armazenar o modo de exibição correto na pasta para exibir posteriormente. 
  
## <a name="see-also"></a>Confira também

- [Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

