---
title: Classificação e categorização
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 5e63d276d25a26f937e9b4f44575fea1030f52d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770455"
---
# <a name="sorting-and-categorization"></a>Classificação e categorização

 
  
**Aplica-se a**: Outlook 
  
Classificar uma tabela coloca as linhas em uma ordem que faz sentido para seu visualizador. Por exemplo, um visualizador pode preferir ver o índice de conteúdo de uma pasta classificada por assunto da mensagem, para que todos os threads de uma conversa sejam juntos enquanto outro visualizador pode querer as mensagens classificadas pelo nome do remetente. Uma tabela instâncias recém-criadas não é necessariamente classificada em alguma ordem específica. 
  
Existem dois tipos de classificação:
  
- Classificação padrão
    
- Categorizados classificação 
    
Com a classificação padrão, todas as linhas são exibidas em uma lista plana usando uma ou mais colunas como uma chave de classificação. Com a classificação categorizada, as linhas são exibidas hierarquicamente com uma ou mais colunas como a chave de classificação. Em cada categoria, há uma linha de título especial que contém as seguintes colunas.
  
- A coluna ou colunas que compõem a chave de classificação
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Recuados sob a linha do cabeçalho são todas as linhas da tabela que contêm colunas com valores que correspondem a chave de classificação. Essas linhas são chamadas as linhas da folha. Linhas de folha contêm todas as colunas na coluna definir menos as colunas de chave de classificação. 
  
Geralmente, os índices de conteúdo de pastas suportam a classificação categorizada além de classificar standard. Normalmente, os índices de conteúdo de contêineres do catálogo de endereços suportam a classificação apenas standard. 
  
Uma categoria pode ter dois estados: expandida e recolhida. Quando uma categoria está no estado recolhido, somente a linha do cabeçalho é retornada da [IMAPITable:: QueryRows](imapitable-queryrows.md). Quando uma categoria está no estado expandido, todas as linhas relacionadas à categoria são retornadas. Isso inclui a linha do cabeçalho e as linhas da folha. 
  
Cada categoria em um modo de exibição de tabela pode ser expandida ou recolhida de forma independente. Ou seja, não todas as categorias devem estar no mesmo estado ao mesmo tempo; Algumas categorias podem ser recolhidas, enquanto outras são expandidas. 
  
O usuário de uma tabela categorizado decidirá como ele é exibido. Uma opção comum é usar um controle fornecido no SDK do Windows chamado controle treeview. Controles TreeView são caixas de listagem informações de suporte em uma estrutura de árvore. Linhas de título para categorias no estado expandido estão marcadas com um sinal de menos enquanto linhas do título para categorias no estado recolhido são marcadas com um sinal de adição. Expandida categorias são exibidas com as linhas da folha recuadas sob as linhas de título. 
  
Para recolher e expandir uma categoria, um provedor de serviço ou um aplicativo cliente usa os seguintes [IMAPITable: IUnknown](imapitableiunknown.md) métodos: 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Para obter mais informações sobre como classificar os threads de uma conversa consulte os seguintes tópicos:
  
- [SSortOrder](ssortorder.md)
    
- [Propriedade canônica PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Propriedade canônica PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Propriedade canônica PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Propriedade canônica PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Propriedade canônica PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Classificar tabelas depois de configurar colunas e restrições](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

