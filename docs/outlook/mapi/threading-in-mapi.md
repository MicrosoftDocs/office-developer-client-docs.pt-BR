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
ms.openlocfilehash: d9ee45ea7a3592a2b0fc0675bbdb6e640f9bd046
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580387"
---
# <a name="threading-in-mapi"></a>Threading no MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um segmento é a entidade básica ao qual um sistema operacional aloca tempo da CPU. Um segmento tem seu próprio registradores, pilha, prioridade e armazenamento, mas compartilha um recursos de processo e espaço de endereço como tokens de acesso. Threads também compartilham memória, com um thread lendo o que outro thread tenha escrito.
  
Os clientes MAPI usam os seguintes modelos de threads genéricos.
  
|**Modelo de Threading**|**Descrição**|
|:-----|:-----|
|Modelo de threading único  <br/> |Todos os objetos são usados em um único segmento.  <br/> |
|Modelo de threading apartment  <br/> |Um objeto pode ser usado somente no segmento que criou a ele.  <br/> |
|Modelo de threading livre ou thread de terceiros  <br/> |Um objeto pode ser usado em qualquer segmento.  <br/> |
   
O MAPI usa o modelo de threading livre, com suporte para os objetos de thread-safe que podem ser usados em qualquer segmento a qualquer momento. OLE usa o modelo apartment threading. O modelo de threading apartment oferece suporte a objetos que devem ser transferidos explicitamente quando um thread diferente daquela que criou o objeto precisa usar esse objeto.
  
O mecanismo utilizado pelo OLE para transferir os objetos de um thread para outro é conhecido como marshaling. Empacotamento envolve a um objeto stub e um objeto de proxy. Esses objetos especiais pacote os parâmetros da interface do objeto para ser empacotado, transferir esses parâmetros para o outro segmento e descompactá-los na chegada. Os conflitos entre os dois modelos multithreaded surgem quando um objeto MAPI livre-threading é enviado para outro processo usando OLE "leve" chamada de procedimento remoto ou LRPC. LRPC altera semântica do objeto de segmentação livre para apartment threading por interposing interfaces stub e proxy com apartment threading comportamento entre o objeto e seu chamador. Divulgação das situações a MAPI que levam a esse conflito pode ajudar os clientes e provedores de serviços de impedir que os problemas ocorram.
  
Um objeto MAPI pode ser acessado:
  
- Por meio de chamadas diretas para seus métodos usando uma interface ponteiro retornado por um provedor de serviços ou MAPI vinculada ao processo do cliente, como o objeto de sessão retornado do [MAPILogonEx](mapilogonex.md).
    
- Por meio de chamadas indiretas para seus métodos usar um ponteiro de interface retornado por qualquer provedor de serviço, como o objeto folder copiados da pasta de outra no [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- Por meio de uma função de retorno de chamada, como o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) passada para um provedor de serviços ou MAPI em uma chamada **Advise** ou os métodos que podem mostrar o progresso em uma operação demorada. 
    

