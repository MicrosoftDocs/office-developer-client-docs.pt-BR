---
title: Desviar a pasta da caixa de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594485"
---
# <a name="traversing-the-inbox-folder"></a>Desviar a pasta da caixa de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
    

