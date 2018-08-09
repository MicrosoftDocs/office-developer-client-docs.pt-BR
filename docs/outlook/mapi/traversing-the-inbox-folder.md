---
title: Desviar a pasta da caixa de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 87fcde5a28a30f08bc2fd5f28fb692a4b4251fbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770631"
---
# <a name="traversing-the-inbox-folder"></a>Desviar a pasta da caixa de entrada

  
  
**Aplica-se a**: Outlook 
  
 **Para percorrer todas as mensagens na caixa de entrada**
  
1. Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da caixa de entrada. 
    
2. Chame **IMAPIFolder::OpenEntry** para abrir a caixa de entrada. 
    
3. Chame o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da caixa de entrada para recuperar a tabela de conteúdo. 
    
4. Chame o conteúdo método de [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela para limitar a coluna definida como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e quaisquer outras colunas que você precisar. 
    
5. Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar um grupo de linhas. 
    
6. Até que não existem mais quaisquer linhas na tabela de conteúdo:
    
1. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a mensagem representada pelo identificador de entrada de cada linha. 
    
2. Atribua o parâmetro _lppUnk_ para um ponteiro de interface **IMessage** local. 
    
3. Trabalhar com as propriedades da mensagem.
    
4. Libere o ponteiro apontado pelo parâmetro _lppUnk_ . 
    
5. Chame [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar o próximo grupo de linhas. 
    
7. Libere a tabela de conteúdo.
    

