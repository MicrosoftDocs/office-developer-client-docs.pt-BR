---
title: Exibindo uma tabela de conteúdo de pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766436"
---
# <a name="displaying-a-folder-contents-table"></a>Exibindo uma tabela de conteúdo de pasta

**Aplica-se a**: Outlook 
  
A tabela de conteúdo de uma pasta contém informações de resumo sobre todas as suas mensagens. Informações de resumo sobre novas mensagens de entrada é exibida na tabela de conteúdo da pasta de recebimento para a classe da mensagem. Para disponibilizar essas informações para usuários, recuperar a tabela e exibir as colunas e linhas conforme apropriado.
  
**Para exibir uma tabela de conteúdo de pasta**
  
1. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md), passando o identificador de entrada da pasta que contém a tabela.
    
2. Chame o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para abrir a tabela de seu conteúdo. 
    
3. Limite de sua exibição da tabela conteúdo se desejado, chamando o método da tabela [IMAPITable::SetColumns](imapitable-setcolumns.md) para especificar colunas específicas. 
    
4. Limite sua exibição da tabela de conteúdo, se desejado, chamando o método da tabela [IMAPITable:: Restrict](imapitable-restrict.md) para filtrar linhas específicas. Se, por exemplo, você deseja mostrar somente as mensagens com uma classe de mensagem específica que ainda precisam ser lido: 
    
    1. Crie uma restrição de propriedade em uma estrutura de [SPropertyRestriction](spropertyrestriction.md) que corresponda a propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) com a classe de mensagem desejado. 
        
    2. Crie uma restrição de bitmask em uma estrutura de [SBitMaskRestriction](sbitmaskrestriction.md) que usa **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como a marca de propriedade e o valor MSGFLAG_UNREAD como a máscara.
        
    3. Crie uma restrição em uma estrutura de [SAndRestriction](sandrestriction.md) que une as restrições de propriedade e bitmask. 
    
5. Classificar a tabela de conteúdo, se desejado, chamando o método da tabela [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
6. Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela de conteúdo para processamento. 
    

