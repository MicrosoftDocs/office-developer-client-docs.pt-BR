---
title: Percorrendo a pasta Caixa de Entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406553"
---
# <a name="traversing-the-inbox-folder"></a>Percorrendo a pasta Caixa de Entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para passar por todas as mensagens na Caixa de Entrada**
  
1. Chame [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da Caixa de Entrada. 
    
2. Chame **IMAPIFolder::OpenEntry** para abrir a Caixa de Entrada. 
    
3. Chame o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da Caixa de Entrada para recuperar a tabela de conteúdo. 
    
4. Chame o método [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela de conteúdo para limitar o conjunto de colunas **a PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e quaisquer outras colunas necessárias. 
    
5. Chame [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar um grupo de linhas. 
    
6. Até que não haja mais linhas na tabela de conteúdo:
    
1. Chame [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir a mensagem representada pelo identificador de entrada de cada linha. 
    
2. Atribua  _o parâmetro lppUnk_ a um ponteiro da interface **IMessage** local. 
    
3. Trabalhe com as propriedades da mensagem.
    
4. Libere o ponteiro apontado pelo parâmetro _lppUnk._ 
    
5. Chame [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar o próximo grupo de linhas. 
    
7. Liberar o índice de conteúdo.
    

