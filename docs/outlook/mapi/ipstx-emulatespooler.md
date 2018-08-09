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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a8e353bbb4f276169ae26ba9d05821158bf55f00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767686"
---
# <a name="ipstxemulatespooler"></a>IPSTX::EmulateSpooler

  
  
**Aplica-se a**: Outlook 
  
Define um repositório local para emular o Gerenciador de protocolo do Outlook para spool mensagens de saída para um servidor.
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 _fEmulate_
  
>  [in] Defina este parâmetro como True se o armazenamento local deve emular o spooler; configurá-lo como False se não. 
    
## <a name="remarks"></a>Comentários

Um repositório local chama **IPSTX::EmulateSpooler** para agir como um protocolo Gerenciador Outlook, mensagens de spooling na fila de saída para o servidor de back-end (por exemplo, servidor do MSN ou servidor AOL) para processamento. Emula um spooler durante a sincronização, o armazenamento, em seguida, chama esses dois métodos: 
  
1. **[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obter a fila de mensagens de saída no repositório. Esse método for bem-sucedido apenas se o repositório é emula o Gerenciador de protocolo do Outlook. 
    
2. **[IMsgStore::SetLockState](imsgstore-setlockstate.md)** para proteger o acesso único a uma mensagem na fila de saída antes de enviá-la para o servidor. Esse método for bem-sucedido apenas se o repositório é emula o Gerenciador de protocolo do Outlook. Após enviar a mensagem, o repositório chama esse método novamente para liberar acesso único a ele. 
    
> [!NOTE]
> Desde o Outlook 2002, o gerente de protocolo do Outlook substituído o MAPI spooler e tornou-se responsável spooling para mensagens de saída para servidores back-end. 
  
## <a name="see-also"></a>Confira também



[IPSTX::GetLastError](ipstx-getlasterror.md)
  
[IPSTX::GetSyncObject](ipstx-getsyncobject.md)

