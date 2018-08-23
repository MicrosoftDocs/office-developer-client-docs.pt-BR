---
title: Identificadores de entrada MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d8c9fb0b24d8954fae75274bfbedca9d7c62de93
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567857"
---
# <a name="mapi-entry-identifiers"></a>Identificadores de entrada MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identificadores de entrada são partes de dados binários armazenados em uma estrutura [ENTRYID](entryid.md) que são usados para identificar exclusivamente e abrir um objeto MAPI. A maioria dos objetos MAPI têm identificadores de entrada. Identificadores de entrada para objetos são análogos aos nomes de arquivo para arquivos. No entanto, eles não são transmittable e não podem ser usados nos sistemas que não seja o sistema que eles se originou. 
  
## <a name="entry-identifiers"></a>Identificadores de entradas

Provedores de armazenamento de mensagem atribuir identificadores de entrada para repositórios de mensagem, pastas e mensagens; provedores de catálogo de endereços atribuí-las aos usuários mensagens, listas de distribuição e contêineres do catálogo de endereços. Identificadores de entrada também são usados para abrir um objeto representado por uma linha em uma tabela, como um objeto de status da tabela de status. Objetos armazenam seus identificadores de entrada em sua propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Enquanto os provedores de serviço criar, atribuir e examinar os identificadores de entrada, os aplicativos cliente usá-los somente como ferramentas para abertura de objetos. Para os clientes, os identificadores de entrada são opacos partes de dados binários em têm nada a ver com o sistema de mensagens subjacente. 
  
Clientes chamar o método de [IMAPITable::QueryColumns](imapitable-querycolumns.md) de uma tabela para recuperar a coluna que contém a propriedade **PR_ENTRYID** ou um método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar sua propriedade **PR_ENTRYID** . 
  
Identificadores de entrada são passados como parâmetros para os métodos **OpenEntry** e **CompareEntryIDs** . Vários objetos MAPI implementam os métodos **OpenEntry** e **CompareEntryIDs** . Com **OpenEntry**, clientes podem abrir um objeto. Com **CompareEntryIDs**, os clientes podem comparar dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. Como os identificadores de entrada não são necessariamente binários comparável, os clientes devem compará-los pelo método **CompareEntryIDs** . 
  
Clientes sempre devem passar identificadores de entrada naturalmente alinhadas em suas chamadas a provedores de serviços, porque embora provedores de serviços devem lidar com identificadores de entrada que são alinhados arbitrariamente, isso não é sempre o caso. Um endereço de memória naturalmente alinhado habilita o computador acessar qualquer tipo de dados suporta nesse endereço sem gerar uma falha de alinhamento. O fator de alinhamento natural é normalmente o mesmo fator de alinhamento usado pelo alocador de memória do sistema e geralmente tem 8 bytes.
  
Identificadores de entrada vêm em dois tipos: curto e longo prazo. Identificadores de entrada de curto prazo são mais rápidas construir, mas sua exclusividade é garantida somente durante a vigência da sessão atual na estação de trabalho atual. Identificadores de entrada de longo prazo tem um tempo de vida mais prolongado. Identificadores de entrada de curto prazo são usados principalmente para linhas nas tabelas e entradas nas caixas de diálogo, enquanto a longo prazo identificadores de entrada são usados para muitos objetos como mensagens, pastas e listas de distribuição.
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

