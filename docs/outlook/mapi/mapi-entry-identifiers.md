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
  
Identificadores de entrada são partes de dados binários armazenados em uma estrutura [ENTRYID](entryid.md) que são usadas para identificar e abrir exclusivamente um objeto MAPI. A maioria dos objetos MAPI tem identificadores de entrada. Os identificadores de entrada para objetos são análogos aos nomes de arquivo dos arquivos. No entanto, eles não são transmitiveis e não podem ser usados em sistemas diferentes do sistema em que se originaram. 
  
## <a name="entry-identifiers"></a>Identificadores de entrada

Os provedores de armazenamento de mensagens atribuem identificadores de entrada a armazenamentos de mensagens, pastas e mensagens; os provedores de listas de endereços os atribuem a contêineres de listas de endereços, listas de distribuição e usuários de mensagens. Os identificadores de entrada também são usados para abrir um objeto representado por uma linha em uma tabela, como um objeto de status na tabela de status. Os objetos armazenam seus identificadores de entrada **na PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
  
Enquanto os provedores de serviços criam, atribuem e examinam identificadores de entrada, os aplicativos cliente os usam apenas como ferramentas para abrir objetos. Para clientes, os identificadores de entrada são partes opacas de dados binários e não têm nada a ver com o sistema de mensagens subjacente. 
  
Os clientes chamam o método [IMAPIProp::GetProps](imapiprop-getprops.md) de um objeto para recuperar sua propriedade **PR_ENTRYID** ou o método [IMAPITable::QueryColumns](imapitable-querycolumns.md) de uma tabela para recuperar a coluna que contém a propriedade **PR_ENTRYID.** 
  
Os identificadores de entrada são passados como parâmetros para os **métodos OpenEntry** e **CompareEntryIDs.** Vários objetos MAPI implementam **os métodos OpenEntry** e **CompareEntryIDs.** Com **OpenEntry**, os clientes podem abrir um objeto. Com **CompareEntryIDs**, os clientes podem comparar dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. Como os identificadores de entrada não são necessariamente binários comparáveis, os clientes devem compará-los pelo **método CompareEntryIDs.** 
  
Os clientes sempre devem passar identificadores de entrada alinhados naturalmente em suas chamadas aos provedores de serviços, pois, embora os provedores de serviços deverão lidar com identificadores de entrada arbitrariamente alinhados, esse nem sempre será o caso. Um endereço de memória alinhado naturalmente permite que o computador acesse qualquer tipo de dados compatível com esse endereço sem gerar uma falha de alinhamento. O fator de alinhamento natural normalmente é o mesmo fator de alinhamento usado pelo alocador de memória do sistema e é geralmente 8 bytes.
  
Os identificadores de entrada vêm em dois tipos: curto e longo prazo. Os identificadores de entrada de curto prazo são mais rápidos de construir, mas sua exclusividade é garantida apenas durante a sessão atual na estação de trabalho atual. Identificadores de entrada a longo prazo têm um tempo de vida mais prolongado. Identificadores de entrada de curto prazo são usados principalmente para linhas em tabelas e entradas em caixas de diálogo, enquanto identificadores de entrada de longo prazo são usados para muitos objetos, como mensagens, pastas e listas de distribuição.
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

