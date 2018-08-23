---
title: Sobre as notificações de tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d6fd49e1a004202e0de02e262f6977ca8a07019d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571938"
---
# <a name="about-table-notifications"></a>Sobre as notificações de tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes frequentemente dependem de notificações de tabela para saber das alterações aos objetos em vez de registro para receber notificações diretamente a partir de objetos. Alterações comuns que fazer com que as notificações sejam enviadas incluem a adição, exclusão ou modificação de uma linha e quaisquer erros críticos. Quando chegam de notificações, os clientes podem determinar se fazer outra chamada recarregar a tabela. 
  
Como as notificações de tabela são assíncronas, existem alguns problemas que podem tornar o tratamento de notificações menores direta:
  
- Os dados passados na estrutura de [TABLE_NOTIFICATION](table_notification.md) podem não representar o estado de mais recente da tabela. Por exemplo, um cliente pode fazer uma alteração em uma mensagem e decida excluí-lo. O provedor de armazenamento de mensagem Implementando a tabela de conteúdo que incluem a mensagem envia notificações de duas: um evento TABLE_ROW_MODIFIED seguido de um evento TABLE_ROW_DELETED. Dependendo de como o provedor de armazenamento de mensagem tempo notificações, o cliente pode receber a notificação de TABLE_ROW_MODIFIED após a exclusão da linha. 
    
- O conjunto incluída com uma notificação de colunas podem ser diferente do conjunto atual de coluna da tabela. MAPI exige que o conjunto de coluna de notificação corresponder ao conjunto de coluna que estava em vigor no momento em que a notificação foi gerada. Porque é possível para um cliente chamar [IMAPITable::SetColumns](imapitable-setcolumns.md) para alterar a coluna definida a qualquer momento — incluindo após uma notificação — os conjuntos de duas colunas não podem ser sincronizados. 
    
- Notificações da tabela serão enviadas somente para as linhas que fazem parte do modo de exibição. Ou seja, se uma linha é excluída da exibição devido a uma restrição ou a tabela estiver recolhida, nenhuma notificação será enviada se essa linha for alterado. Além disso, nenhuma notificação é enviadas para informar um cliente sobre uma alteração no estado de categoria.
    
Clientes devem estar cientes de que nem todas as tabelas suportam a notificação TABLE_SORT_DONE e devem estar preparadas para lidar com essa condição por:
  
1. Forçando a classificação estão sincronizados.
    
2. Recarregar as linhas da tabela quando [IMAPITable:: SortTable](imapitable-sorttable.md) retorna. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

