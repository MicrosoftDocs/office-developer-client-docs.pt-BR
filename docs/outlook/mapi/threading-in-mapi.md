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
  
Um thread é a entidade básica para a qual um sistema operacional aloca tempo de CPU. Um thread tem seus próprios registros, pilha, prioridade e armazenamento, mas compartilha um espaço de endereço e recursos de processo, como tokens de acesso. Threads também compartilham memória, com um thread lendo o que outro thread escreveu.
  
Os clientes MAPI usam os seguintes modelos de threading genéricos.
  
|**Modelo de threading**|**Descrição**|
|:-----|:-----|
|Modelo de threading único  <br/> |Todos os objetos são usados no thread único.  <br/> |
|Modelo de threading de apartment  <br/> |Um objeto só pode ser usado no thread que o criou.  <br/> |
|Modelo de threading gratuito ou thread-party  <br/> |Um objeto pode ser usado em qualquer thread.  <br/> |
   
O MAPI usa o modelo de threading livre, dando suporte a objetos thread-safe que podem ser usados em qualquer thread a qualquer momento. OLE usa o modelo de threading de apartment. O modelo de threading de apartment dá suporte a objetos que devem ser explicitamente transferidos quando um thread diferente do que criou o objeto precisa usar esse objeto.
  
O mecanismo que o OLE usa para transferir objetos de um thread para outro é conhecido como empacotamento. A empacotamento envolve um objeto stub e um objeto proxy. Esses objetos especiais empacotam os parâmetros da interface no objeto a ser empacotado, transferem esses parâmetros para o outro thread e os descompactam na chegada. O conflito entre os dois modelos multithreaded surge quando um objeto MAPI de thread livre é enviado para outro processo usando a Chamada de Procedimento Remoto "leve" OLE ou LRPC. LRPC altera a semântica do objeto de threading livre para threading de apartment interpondo interfaces stub e proxy com comportamento de threading de apartment entre o objeto e seu chamador. O reconhecimento das situações em MAPI que levam a esse conflito pode ajudar clientes e provedores de serviços a evitar problemas.
  
Um objeto MAPI pode ser acessado:
  
- Através de chamadas diretas para seus métodos usando um ponteiro de interface retornado por um provedor de serviços ou MAPI vinculado ao processo do cliente, como o objeto de sessão retornado de [MAPILogonEx](mapilogonex.md).
    
- Através de chamadas indiretas para seus métodos usando um ponteiro de interface retornado por qualquer provedor de serviços, como o objeto de pasta copiado de outra pasta em [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- Por meio de uma função de retorno de chamada, como o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) passado para um provedor de serviços ou para MAPI em uma chamada de Advise ou os métodos que podem mostrar o progresso em uma operação demorada.  
    

