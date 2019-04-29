---
title: Suporte a pesquisas em provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425383"
---
# <a name="supporting-searches-in-message-store-providers"></a>Suporte a pesquisas em provedores de repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente freqüentemente têm alguns componentes de interface do usuário dedicados à pesquisa de mensagens em um repositório de mensagens. Os critérios de pesquisa são especificados na interface [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) por meio dos métodos [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) e [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Os clientes usam a propriedade **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) do objeto de repositório de mensagens para identificar a pasta raiz no repositório de mensagens que contém pastas para resultados da pesquisa. Em geral, a pasta de resultados de pesquisa é uma pasta no nível superior do repositório de mensagens que não faz parte da árvore de pastas IPM e é, portanto, oculta.
  
Se seu provedor de repositório de mensagens usa uma pasta de resultados de pesquisa permanente ou cria um quando um cliente abre o identificador de entrada armazenado na propriedade **PR_FINDER_ENTRYID** é um detalhe de implementação. É um pouco mais fácil para o provedor de armazenamento de mensagens usar uma pasta permanente que é criada quando o repositório de mensagens é criado, pois isso evita a complicação de verificar o identificador de entrada sempre que qualquer pasta é aberta para ver se deve criar um pasta de resultados de pesquisa. No enTanto, nem todos os provedores de repositório de mensagens podem fazer isso; notavelmente, repositórios de mensagens somente leitura ou repositórios que fornecem uma interface MAPI para um banco de dados herdado geralmente não são permitidos ou não podem criar uma pasta de resultados de pesquisa permanente no mecanismo de armazenamento subjacente. 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

