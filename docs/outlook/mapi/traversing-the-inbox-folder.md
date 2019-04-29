---
title: Atravessando a pasta caixa de entrada
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
# <a name="traversing-the-inbox-folder"></a>Atravessando a pasta caixa de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para percorrer todas as mensagens na caixa de entrada**
  
1. Chame [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) para recuperar o identificador de entrada da caixa de entrada. 
    
2. Chame **IMAPIFolder:: OpenEntry** para abrir a caixa de entrada. 
    
3. Chame o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable da caixa de entrada para recuperar a tabela de conteúdo. 
    
4. Chame o método imApitable da tabela de conteúdo [::](imapitable-setcolumns.md) SetColumns para limitar o conjunto de colunas a **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e quaisquer outras colunas necessárias. 
    
5. Call [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar um grupo de linhas. 
    
6. Até que não haja mais nenhuma linha na tabela de conteúdo:
    
1. Chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir a mensagem representada pelo identificador de entrada de cada linha. 
    
2. Atribua o parâmetro _lppUnk_ a um ponteiro de interface **IMessage** local. 
    
3. Trabalhar com as propriedades da mensagem.
    
4. Solte o ponteiro apontado pelo parâmetro _lppUnk_ . 
    
5. Call [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar o próximo grupo de linhas. 
    
7. Libera a tabela de conteúdo.
    

