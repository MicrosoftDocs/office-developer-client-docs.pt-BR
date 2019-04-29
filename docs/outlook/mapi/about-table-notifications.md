---
title: Sobre as notificações de tabela
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
# <a name="about-table-notifications"></a>Sobre as notificações de tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes freqüentemente dependem de notificações de tabela para aprender as alterações nos objetos em vez de se registrarem para receber notificações diretamente dos objetos. As alterações típicas que fazem com que as notificações sejam enviadas incluem adição, exclusão ou modificação de uma linha e qualquer erro crítico. Quando as notificações chegam, os clientes podem determinar se deseja fazer outra chamada para recarregar a tabela. 
  
Como as notificações de tabela são assíncronas, há alguns problemas que podem tornar as notificações de tratamento menores do que o simples:
  
- Os dados passados na estrutura [TABLE_NOTIFICATION](table_notification.md) podem não representar o estado mais atual da tabela. Por exemplo, um cliente pode fazer uma alteração em uma mensagem e, em seguida, decidir excluí-la. O provedor de repositório de mensagens que está implementando a tabela de conteúdo que incluía a mensagem envia duas notificações: um evento TABLE_ROW_MODIFIED seguido por um evento TABLE_ROW_DELETED. Dependendo de como o provedor do repositório de mensagens expira as notificações, o cliente pode receber a notificação TABLE_ROW_MODIFIED após a exclusão da linha. 
    
- O conjunto de colunas incluído com uma notificação pode ser diferente do conjunto de colunas atual da tabela. MAPI exige que o conjunto de colunas de notificação coincida com o conjunto de colunas que estava em vigor no momento em que a notificação foi gerada. Como é possível para um cliente chamar imApitable [::](imapitable-setcolumns.md) SetColumns para alterar o conjunto de colunas a qualquer momento, incluindo após uma notificação, os dois conjuntos de colunas podem não ser sincronizados. 
    
- As notificações de tabela são enviadas somente para as linhas que fazem parte do modo de exibição. Ou seja, se uma linha for excluída do modo de exibição devido a uma restrição ou porque a tabela está em um estado recolhido, nenhuma notificação será enviada se essa linha for alterada. Além disso, nenhuma notificação é enviada para informar um cliente sobre uma alteração no estado de categoria.
    
Os clientes devem estar cientes de que nem todas as tabelas oferecem suporte à notificação TABLE_SORT_DONE e devem estar preparados para lidar com essa condição:
  
1. Forçar a classificação a ser síncrona.
    
2. Recarregar as linhas da tabela quando imApitable [:: SortTable](imapitable-sorttable.md) retorna. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

