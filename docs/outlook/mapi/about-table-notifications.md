---
title: Sobre notificações de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417949"
---
# <a name="about-table-notifications"></a>Sobre notificações de tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes geralmente dependem de notificações de tabela para aprender sobre alterações em objetos em vez de se registrar para receber notificações diretamente dos objetos. As alterações típicas que causam o enviar notificações incluem a adição, exclusão ou modificação de uma linha e qualquer erro crítico. Quando as notificações chegam, os clientes podem determinar se devem fazer outra chamada para recarregar a tabela. 
  
Como as notificações de tabela são assíncronas, há alguns problemas que podem tornar o tratamento de notificações menos simples:
  
- Os dados passados [na TABLE_NOTIFICATION](table_notification.md) estrutura podem não representar o estado mais atual da tabela. Por exemplo, um cliente pode fazer uma alteração em uma mensagem e decidir excluí-la. O provedor de armazenamento de mensagens que implementa o índice de conteúdo que incluiu a mensagem envia duas notificações: um evento de TABLE_ROW_MODIFIED seguido por um TABLE_ROW_DELETED evento. Dependendo de como o provedor de armazenamento de mensagens tempo notificações, o cliente pode receber a notificação de TABLE_ROW_MODIFIED após a exclusão da linha. 
    
- O conjunto de colunas incluído em uma notificação pode ser diferente do conjunto de colunas atual da tabela. MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated. Como é possível que um cliente chame [IMAPITable::SetColumns](imapitable-setcolumns.md) para alterar o conjunto de colunas a qualquer momento — incluindo após uma notificação — os dois conjuntos de colunas podem não ser sincronizados. 
    
- As notificações de tabela são enviadas apenas para linhas que fazem parte do exibição. Ou seja, se uma linha for excluída da exibição devido a uma restrição ou porque a tabela está em um estado recolhido, nenhuma notificação será enviada se essa linha for mudada. Além disso, nenhuma notificação é enviada para informar um cliente sobre uma alteração no estado da categoria.
    
Os clientes devem estar cientes de que nem todas as tabelas suportam a notificação TABLE_SORT_DONE e devem estar preparados para lidar com essa condição ao:
  
1. Forçar a classificação a ser síncrona.
    
2. Recarregando as linhas da tabela quando [IMAPITable::SortTable retorna.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

