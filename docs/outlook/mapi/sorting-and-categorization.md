---
title: Classificação e categorização
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418481"
---
# <a name="sorting-and-categorization"></a>Classificação e categorização

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Classificar uma tabela coloca linhas em uma ordem que faz sentido para seu visualizador. Por exemplo, um visualizador pode preferir ver o índice de conteúdo de uma pasta classificar por assunto da mensagem para que todos os threads de uma conversa ficam juntos enquanto outro visualizador pode querer que as mensagens sejam ordenadas pelo nome do remetente. Uma tabela recém-criada não é necessariamente ordenada em uma ordem específica. 
  
Há dois tipos de classificação:
  
- Classificação padrão
    
- Classificação categorizada 
    
Com a classificação padrão, todas as linhas são exibidas em uma lista simples usando uma ou mais colunas como uma chave de classificação. Com a classificação categorizada, as linhas são exibidas hierarquicamente com uma ou mais colunas como a chave de classificação. Em cada categoria, há uma linha de título especial que contém as colunas a seguir.
  
- A coluna ou colunas que com a chave de classificação
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Recuados sob a linha de título são todas as linhas da tabela que contêm colunas com valores que corresponderem à chave de classificação. Essas linhas são chamadas de linhas folha. As linhas Leaf contêm todas as colunas no conjunto de colunas menos as colunas de chave de classificação. 
  
Os índices de conteúdo de pastas geralmente suportam a classificação categorizada, além da classificação padrão. Os índices de conteúdo dos contêineres do livro de endereços normalmente suportam apenas a classificação padrão. 
  
Uma categoria pode ter dois estados: recolhido e expandido. Quando uma categoria está no estado recolhido, somente a linha de título é retornada de [IMAPITable::QueryRows](imapitable-queryrows.md). Quando uma categoria está no estado expandido, todas as linhas relacionadas à categoria são retornadas. Isso inclui a linha de título e as linhas folha. 
  
Cada categoria em um exibição de tabela pode ser expandida ou recolhido independentemente. Ou seja, nem todas as categorias devem estar no mesmo estado ao mesmo tempo; algumas categorias podem ser recolhidos enquanto outras são expandidas. 
  
O usuário de uma tabela categorizada decide como ela é exibida. Uma opção comum é usar um controle fornecido no SDK do Windows chamado controle treeview. Controles treeview são caixas de listagem que suportam informações em uma estrutura em forma de árvore. As linhas de título para categorias no estado expandido são marcadas com um sinal de menos enquanto as linhas de título para categorias no estado recolhido são marcadas com um sinal de mais. As categorias expandidas são exibidas com as linhas folha recuadas sob as linhas de título. 
  
Para collapse and expand a category, a client application or service provider uses the following [IMAPITable : IUnknown](imapitableiunknown.md) methods: 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Para obter mais informações sobre como classificar os threads de uma conversa, consulte os seguintes tópicos:
  
- [SSortOrder](ssortorder.md)
    
- [Propriedade canônica PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propriedade canônica PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propriedade canônica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propriedade canônica PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propriedade canônica PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Classificar tabelas após definir colunas e restrições](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

