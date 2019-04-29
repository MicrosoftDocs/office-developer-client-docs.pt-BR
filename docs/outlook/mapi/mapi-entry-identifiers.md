---
title: Identificadores de entrada MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 84c37696-da7a-42e0-b8c0-29658a6c9a48
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4c414b9f8a1d70fd5eea94da326674a749ccefe2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414960"
---
# <a name="mapi-entry-identifiers"></a>Identificadores de entrada MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os identificadores de entrada são partes de dados binários [](entryid.md) armazenados em uma estrutura ENTRYID usada para identificar exclusivamente e abrir um objeto MAPI. A maioria dos objetos MAPI têm identificadores de entrada. Os identificadores de entrada para objetos são análogos aos nomes de arquivo dos arquivos. No enTanto, eles não são transmitidos e não podem ser usados em sistemas diferentes do sistema em que foram originados. 
  
## <a name="entry-identifiers"></a>Identificadores de entrada

Os provedores de repositórios de mensagens atribuem identificadores de entrada a repositórios de mensagens, pastas e mensagens; os provedores de catálogo de endereços os atribuem aos contêineres do catálogo de endereços, listas de distribuição e usuários de mensagens. Os identificadores de entrada também são usados para abrir um objeto representado por uma linha em uma tabela, como um objeto de status na tabela de status. Os objetos armazenam seus identificadores de entrada na propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Enquanto os provedores de serviços criam, atribuem e examinam identificadores de entrada, os aplicativos clientes os usam somente como ferramentas para abrir objetos. Para clientes, os identificadores de entrada são pedaços opacos de dados binários e não têm nada a ver com o sistema de mensagens subjacente. 
  
Os clientes chamam o método [IMAPIProp::](imapiprop-getprops.md) GetProps de um objeto para recuperar sua propriedade **PR_ENTRYID** ou o método IMAPITable [:: QueryColumns](imapitable-querycolumns.md) da tabela para recuperar a coluna que contém a propriedade **PR_ENTRYID** . 
  
Os identificadores de entrada são passados como parâmetros para os métodos **OpenEntry** e **CompareEntryIDs** . Vários objetos MAPI implementam os métodos **OpenEntry** e **CompareEntryIDs** . Com o **OpenEntry**, os clientes podem abrir um objeto. Com o **CompareEntryIDs**, os clientes podem comparar dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. Como os identificadores de entrada não são necessariamente equivalentes a binários, os clientes devem compará-los pelo método **CompareEntryIDs** . 
  
Os clientes devem sempre passar identificadores de entrada alinhados naturalmente em suas chamadas para os provedores de serviço, porque embora os provedores de serviços devam manipular identificadores de entrada que estão alinhados arbitrariamente, isso nem sempre é o caso. Um endereço de memória alinhado naturalmente permite que o computador acesse qualquer tipo de dados que oferece suporte a esse endereço sem gerar uma falha de alinhamento. O fator de alinhamento natural geralmente é o mesmo fator de alinhamento usado pelo alocador de memória do sistema e geralmente é de 8 bytes.
  
Os identificadores de entrada têm dois tipos: curto e de longo prazo. Identificadores de entrada de curto prazo são mais rápidos de construir, mas sua exclusividade é segura apenas na vida da sessão atual na estação de trabalho atual. Os identificadores de entrada de longo prazo têm um tempo de vida mais prolongado. Identificadores de entrada de curto prazo são usados principalmente para linhas em tabelas e entradas em caixas de diálogo, enquanto identificadores de entrada de longo prazo são usados para muitos objetos, como mensagens, pastas e listas de distribuição.
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

