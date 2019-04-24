---
title: Visão geral do provedor de repositório de mensagens MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eae44469-b217-4d05-b47f-5a0b1fab7056
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5d4ef074523cd654c3db2d686494d9a4f864e7cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345869"
---
# <a name="mapi-message-store-provider-overview"></a>Visão geral do provedor de repositório de mensagens MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositórios de mensagens lidam com o armazenamento e a recuperação de mensagens e outras informações para os usuários de aplicativos cliente. As informações da mensagem são organizadas usando um sistema hierárquico conhecido como repositório de mensagens. O repositório de mensagens é implementado em vários níveis, com contêineres chamados pastas que contêm mensagens de tipos diferentes. Não há limite para o número de níveis em um repositório de mensagens; as pastas podem conter muitas subpastas. 
  
A ilustração a seguir mostra a arquitetura de repositório de mensagens hierárquica.
  
**Message store architecture**
  
![Arquitetura do repositório de mensagens] (media/amapi_03.gif "Arquitetura do repositório de mensagens")
  
A figura mostra duas pastas, uma com uma subpasta. Os usuários do aplicativo cliente podem acessar um modo de exibição de resumo das mensagens contidas em cada pasta ou exibi-las individualmente com um formulário. Se o cliente exibe um formulário padrão que o MAPI fornece ou um formulário personalizado que um desenvolvedor de formulário fornece depende do tipo, ou classe, da mensagem. A primeira pasta contém mensagens de observação e usa o formato de nota padrão MAPI. A segunda pasta contém mensagens de solicitação de inventário e usa um formulário de inventário personalizado. As informações nos dois formulários representam as propriedades da mensagem.
  
Você pode usar os dados do repositório de mensagens de várias maneiras. Além de usar dados para correio eletrônico tradicional, você pode usar pastas como um fórum para discussão pública, como um repositório para documentos de referência ou como um contêiner para caixa postal, calendário, contatos ou tarefas, por exemplo. Um único repositório de mensagens pode conter vários tipos de informações. Vários clientes podem instalar o mesmo repositório de mensagens. Isso torna o compartilhamento de dados fácil e rápido. 
  
As pastas do repositório de mensagens permitem que você classifique e Filtre mensagens e personalize a exibição da mensagem em uma interface do usuário. Links para mensagens filtradas são mantidos em pastas especiais chamadas de resultados de pesquisa. O usuário de um aplicativo cliente insere critérios de filtragem, aos quais o MAPI se refere como uma restrição, e os critérios são aplicados às mensagens armazenadas em uma ou mais pastas. Por exemplo, um usuário pode querer exibir apenas as mensagens que lidam com um assunto específico e ter datas de chegada mais recentes do que a semana passada. As referências às mensagens que correspondem aos critérios são listadas na pasta de pesquisa e as mensagens reais permanecem em suas pastas regulares.
  
As mensagens são as unidades de dados que são transferidas de um usuário ou aplicativo para outro usuário ou aplicativo. Cada mensagem contém algum texto de mensagem, com formatação simples ou complexa, e informações de envelope de mensagens usadas para transmissão. Algumas mensagens incluem um ou mais anexos ou dados adicionais relacionados a e transportados com uma mensagem no formato de um arquivo, outra mensagem ou um objeto OLE. 
  
Dependendo do provedor de repositório de mensagens, um usuário pode salvar uma nova mensagem que está sendo gravada, além de mensagens que foram enviadas ou recebidas. As mensagens podem ser copiadas ou movidas de uma pasta para outra com cada cópia se tornando uma mensagem separada que pode ser copiada, excluída ou modificada individualmente. Outro recurso que alguns provedores de repositórios de mensagens habilitam é a capacidade de alterar uma mensagem após ela ter sido recebida e armazená-la novamente em sua pasta. Um usuário pode aproveitar esse recurso para girar uma mensagem de fax que chegou de cabeça para baixo. O usuário pode armazenar o modo de exibição correto na pasta para exibição posterior. 
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

