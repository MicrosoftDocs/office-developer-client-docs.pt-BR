---
title: Threading no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405538"
---
# <a name="threading-in-mapi"></a>Threading no MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um thread é a entidade básica para a qual um sistema operacional aloca tempo de CPU. Um thread tem seus próprios registradores, Stack, Priority e Storage, mas compartilha um espaço de endereço e recursos de processo, como tokens de acesso. Threads também compartilham memória, com um thread lendo o que é gravado por outro thread.
  
Os clientes MAPI usam os seguintes modelos de segmentação genérica.
  
|**Modelo de segmentação**|**Descrição**|
|:-----|:-----|
|Modelo de segmentação única  <br/> |Todos os objetos são usados no único thread.  <br/> |
|Modelo de segmentação de apartamento  <br/> |Um objeto pode ser usado somente no thread que o criou.  <br/> |
|Segmentação livre, ou thread-festa, modelo  <br/> |Um objeto pode ser usado em qualquer thread.  <br/> |
   
O MAPI usa o modelo de segmentação livre, com suporte a objetos isentos de thread que podem ser usados em qualquer thread a qualquer momento. O OLE usa o modelo de segmentação de apartamento. O modelo de segmentação de apartamento suporta objetos que devem ser transferidos explicitamente quando um thread diferente daquele que criou o objeto precisa usar esse objeto.
  
O mecanismo que o OLE usa para transferir objetos de um thread para outro é conhecido como marshaling. O empacotamento envolve um objeto stub e um objeto proxy. Esses objetos especiais empacotam os parâmetros da interface no objeto a ser empacotado, transferir esses parâmetros para o outro thread e desempacotá-los na chegada. O conflito entre os dois modelos multissegmentados surge quando um objeto MAPI de thread livre é enviado para outro processo usando uma chamada de procedimento remoto "leve" de OLE ou LRPC. O LRPC altera a semântica do objeto de segmentação livre para a segmentação de apartamento por meio da troca de stub e interfaces de proxy com comportamento de segmentação de apartamento entre o objeto e seu chamador. A conscientização das situações em MAPI que levam a esse conflito pode ajudar os clientes e os provedores de serviços a impedir que problemas ocorram.
  
Um objeto MAPI pode ser acessado:
  
- Por meio de chamadas diretas para seus métodos usando um ponteiro de interface retornado por um provedor de serviços ou MAPI vinculado ao processo do cliente, como o objeto Session retornado por [funçãomapilogonex](mapilogonex.md).
    
- Por meio de chamadas indiretas para seus métodos usando um ponteiro de interface retornado por qualquer provedor de serviços, como o objeto Folder copiado de outra pasta em [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md).
    
- Por meio de uma função de retorno de chamada, como o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) passado para um provedor de serviços ou para MAPI em uma chamada de **aviso** ou os métodos que podem mostrar o progresso em uma operação demorada. 
    

