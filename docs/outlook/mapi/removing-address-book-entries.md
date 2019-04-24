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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328347"
---
# <a name="removing-address-book-entries"></a>Remover entradas do catálogo de endereços
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O método IABContainer do seu contêiner [::D eleteentries](iabcontainer-deleteentries.md) é chamado para remover um ou mais destinatários. **DeleteEntries** tem dois parâmetros: uma matriz de identificadores de entrada que representa os destinatários a serem excluídos e um valor de sinalizadores reservados. A exclusão de um destinatário afeta a tabela de conteúdo do seu contêiner; Além de excluir o destinatário, seu contêiner deve excluir a linha da tabela de conteúdo que representa o destinatário. Quando a linha foi removida da tabela, seu contêiner deve emitir uma notificação de tabela para cada cliente registrado. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Para implementar o IABContainer::D eleteEntries
  
1. Exclua cada destinatário representado pelo identificador de entrada de seu contêiner.
    
2. Se a tabela de conteúdo do seu contêiner estiver aberta:
    
   - Envie uma notificação do _fnevTableModified_ com o membro **ULTABLEEVENT** definido como TABLE_ROW_DELETED para clientes registrados para cada linha de tabela de conteúdo excluída. Se seu provedor usar o utilitário de notificação, chame [IMAPISupport:: Notify](imapisupport-notify.md) para enviar essas notificações. 
    
   - Se o provedor oferecer suporte a notificações de objeto, envie também uma notificação _fnevObjectDeleted_ . 
    

