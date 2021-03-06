---
title: Exibir uma tabela de conteúdo da pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412391"
---
# <a name="displaying-a-folder-contents-table"></a>Exibir uma tabela de conteúdo da pasta

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O sumário de uma pasta contém informações resumidas sobre todas as suas mensagens. Informações de resumo sobre novas mensagens de entrada são exibidas no sumário da pasta de recebimento da classe de mensagem. Para disponibilizar essas informações aos usuários, recupere a tabela e exibe as colunas e linhas conforme apropriado.
  
**Para exibir uma tabela de conteúdo de pasta**
  
1. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md), passando o identificador de entrada da pasta que contém a tabela.
    
2. Chame o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para abrir sua tabela de conteúdo. 
    
3. Limite seu modo de exibição da tabela de conteúdo, se desejado, chamando o método [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela para especificar colunas específicas. 
    
4. Limite seu modo de exibição da tabela de conteúdo, se desejado, chamando o método [IMAPITable::Restrict](imapitable-restrict.md) da tabela para filtrar linhas específicas. Se, por exemplo, você quiser mostrar apenas mensagens com uma classe de mensagem específica que ainda precisa ser lida: 
    
    1. Crie uma restrição de propriedade em uma estrutura [SPropertyRestriction](spropertyrestriction.md) que corresponde à propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) com a classe de mensagem desejada. 
        
    2. Crie uma restrição de bitmask em uma estrutura [SBitMaskRestriction](sbitmaskrestriction.md) que usa **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como a marca de propriedade e o valor MSGFLAG_UNREAD como a máscara.
        
    3. Crie uma restrição em uma [estrutura SAndRestriction](sandrestriction.md) que une as restrições de propriedade e bitmask. 
    
5. Classificar a tabela de conteúdo, se desejado, chamando o [método IMAPITable::SortTable da](imapitable-sorttable.md) tabela. 
    
6. Chame [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela de conteúdo para processamento. 
    

