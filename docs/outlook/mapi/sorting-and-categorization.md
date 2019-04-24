---
title: Classificação e categorização
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Última modificação: 08 de novembro de 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344503"
---
# <a name="sorting-and-categorization"></a>Classificação e categorização

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A classificação de uma tabela coloca linhas em uma ordem que faz sentido para o seu visualizador. Por exemplo, um visualizador pode preferir ver a tabela de conteúdo de uma pasta classificada por assunto da mensagem para que todos os threads de uma conversa estejam juntos enquanto outro visualizador possa querer as mensagens classificadas pelo nome do remetente. Uma tabela instanciada recentemente não é necessariamente classificada em uma ordem específica. 
  
Há dois tipos de classificação:
  
- Classificação padrão
    
- Classificação categorizada 
    
Com a classificação padrão, todas as linhas são exibidas em uma lista simples usando uma ou mais colunas como uma chave de classificação. Com a classificação categorizada, as linhas são exibidas hierarquicamente com uma ou mais colunas como a chave de classificação. Em cada categoria, há uma linha de título especial que contém as seguintes colunas.
  
- A coluna ou colunas que compõem a chave de classificação
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
O recuo sob a linha de título são todas as linhas da tabela que contêm colunas com valores que correspondem à chave de classificação. Essas linhas são chamadas de linhas de folha. As linhas de folha contêm todas as colunas no conjunto de colunas menos as colunas da chave de classificação. 
  
As tabelas de conteúdo das pastas com frequência oferecem suporte à classificação categorizada além da classificação padrão. As tabelas de conteúdo dos contêineres do catálogo de endereços normalmente oferecem suporte somente à classificação padrão. 
  
Uma categoria pode ter dois Estados: recolhidas e expandidas. Quando uma categoria está no estado recolhida, somente a linha de título é retornada de [IMAPITable:: QueryRows](imapitable-queryrows.md). Quando uma categoria está no estado expandido, todas as linhas relacionadas à categoria são retornadas. Isso inclui a linha de título e as linhas de folha. 
  
Cada categoria em um modo de exibição de tabela pode ser expandida ou recolhida de forma independente. Ou seja, nem todas as categorias devem estar no mesmo estado ao mesmo tempo; algumas categorias podem ser recolhidas enquanto outras são expandidas. 
  
O usuário de uma tabela categorizada decide como ela é exibida. Uma opção comum é usar um controle fornecido no Windows SDK chamado de controle TreeView. Os controles TreeView são caixas de listagem que dão suporte a informações em uma estrutura do tipo árvore. As linhas de título para categorias no estado expandido são marcadas com um sinal de menos enquanto as linhas de título para categorias no estado recolhido são marcadas com um sinal de adição. As categorias expandidas são exibidas com as linhas de folha recuadas sob as linhas de título. 
  
Para recolher e expandir uma categoria, um aplicativo cliente ou provedor de serviços usa os seguintes métodos imApitable [: IUnknown](imapitableiunknown.md) : 
  
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
    
- [Classificar tabelas após a definição de colunas e restrições](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

