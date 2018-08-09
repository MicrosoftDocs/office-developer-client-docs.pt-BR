---
title: Removendo entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770225"
---
# <a name="removing-address-book-entries"></a>Removendo entradas do catálogo de endereços
  
**Aplica-se a**: Outlook 
  
Método de [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) do seu contêiner é chamado para remover um ou mais destinatários. **DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representa os destinatários a ser excluído e um valor de flags reservado. Excluir um destinatário afeta o índice de conteúdo de seu contêiner; Além de excluir o destinatário, seu contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário. Quando a linha foi removida da tabela, seu contêiner deve emitir uma notificação de tabela para cada cliente registrado. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Para implementar IABContainer::DeleteEntries
  
1. Exclua cada destinatário representado pelo identificador de entrada do seu contêiner.
    
2. Se a tabela de conteúdo do seu contêiner estiver aberta:
    
   - Envie uma notificação de _fnevTableModified_ com o membro **ulTableEvent** definido como TABLE_ROW_DELETED aos clientes registrados para cada linha da tabela de conteúdo excluído. Se seu provedor de usar o utilitário de notificação, chame [IMAPISupport::Notify](imapisupport-notify.md) para enviar essas notificações. 
    
   - Se o provedor oferece suporte a notificações de objeto, também envie uma notificação _fnevObjectDeleted_ . 
    

