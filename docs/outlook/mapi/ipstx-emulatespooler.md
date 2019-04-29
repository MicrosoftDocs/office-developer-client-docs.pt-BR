---
title: IPSTXEmulateSpooler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.EmulateSpooler
api_type:
- COM
ms.assetid: aec72e51-1f75-b2c5-76ca-626cd21fbc7d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 024583926b5d0be638b33b1b60c5d4c5dc74d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438950"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define um repositório local para emular o Gerenciador de protocolos do Outlook para o spool de mensagens de saída para um servidor.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  no Defina esse parâmetro como true se o repositório local deve emular o spooler; Defina como false se não. 
    
## <a name="remarks"></a>Comentários

Um repositório local chama **IPSTX:: EmulateSpooler** para atuar como um Gerenciador de protocolo do Outlook, fazendo o spool de mensagens na fila de saída para o servidor back-end (por exemplo, servidor do MSN ou AOL) para processamento. Emular um spooler durante a sincronização, o repositório chama esses dois métodos: 
  
1. **[IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obter a fila de saída de mensagens no repositório. Este método será bem-sucedido somente se o repositório estiver emulando o Gerenciador de protocolos do Outlook. 
    
2. **[IMsgStore::](imsgstore-setlockstate.md)** setlockstate para proteger o acesso exclusivo a uma mensagem na fila de saída antes de enviá-la ao servidor. Este método será bem-sucedido somente se o repositório estiver emulando o Gerenciador de protocolos do Outlook. Após enviar a mensagem, o armazenamento chama esse método novamente para liberar acesso exclusivo a ele. 
    
> [!NOTE]
> Desde o Outlook 2002, o Gerenciador de protocolo do Outlook substituiu o spooler MAPI e se tornou responsável por fazer o spool de mensagens de saída para servidores de back-end. 
  
## <a name="see-also"></a>Confira também



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

