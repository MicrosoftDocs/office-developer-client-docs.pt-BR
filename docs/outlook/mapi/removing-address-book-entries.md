---
title: Remover entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425257"
---
# <a name="removing-address-book-entries"></a>Remover entradas do catálogo de endereços
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O método [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) do contêiner é chamado para remover um ou mais destinatários. **DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representam os destinatários a serem excluídos e um valor de sinalizadores reservados. A exclusão de um destinatário afeta o índice de conteúdo do contêiner; além de excluir o destinatário, o contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário. Quando a linha tiver sido removida da tabela, o contêiner deverá emitir uma notificação de tabela para cada cliente registrado. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Para implementar IABContainer::D eleteEntries
  
1. Exclua cada destinatário representado pelo identificador de entrada do contêiner.
    
2. Se a tabela de conteúdo do contêiner estiver aberta:
    
   - Envie uma  _notificação fnevTableModified_ com o membro **ulTableEvent** definido como TABLE_ROW_DELETED clientes registrados para cada linha de tabela de conteúdo excluída. Se o provedor usar o utilitário de notificação, chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar essas notificações. 
    
   - Se o provedor suportar notificações de objeto, envie também uma _notificação fnevObjectDeleted._ 
    

