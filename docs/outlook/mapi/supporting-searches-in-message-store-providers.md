---
title: Suporte a pesquisas em provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0cd8bbe14e6af020ec5c93cd46a24853d1c8401c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770548"
---
# <a name="supporting-searches-in-message-store-providers"></a>Suporte a pesquisas em provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 
  
Aplicativos clientes frequentemente têm alguns componentes de interface do usuário devotados a pesquisar mensagens em um repositório de mensagem. Critérios de pesquisa são especificados no [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) interface por meio dos métodos [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) e [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Clientes usam a mensagem repositório de propriedade do objeto **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) para identificar a pasta raiz no repositório de mensagem que contém pastas para os resultados da pesquisa. A pasta de resultados de pesquisa geralmente é uma pasta de nível superior do repositório de mensagem que não faz parte da árvore da pasta IPM e é, portanto, oculto.
  
Se o seu provedor de armazenamento de mensagem usa uma pasta de resultados de pesquisa permanente ou cria um quando um cliente abre o identificador de entrada armazenado na propriedade **PR_FINDER_ENTRYID** é um detalhe da implementação. É relativamente mais fácil para seu provedor de armazenamento de mensagem usar uma pasta permanente que é criada quando o armazenamento de mensagens é criado, porque fazer isso evita a complexidade das verificando o identificador de entrada sempre que qualquer pasta é aberta para ver se é necessário criar um pasta de resultados de pesquisa. No entanto, nem todos os provedores de armazenamento de mensagens podem fazer isso; em especial, repositórios de mensagem de somente leitura ou repositórios que fornecem uma interface MAPI para um banco de dados herdado geralmente não são permitidos ou não conseguem criar uma pasta de resultados de pesquisa permanente no mecanismo de armazenamento subjacente. 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

