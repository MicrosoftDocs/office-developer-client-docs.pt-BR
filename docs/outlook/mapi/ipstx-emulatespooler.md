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
ms.openlocfilehash: 079b54757cfcd5c9b38365abc5a6d901e2b06724
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580716"
---
# <a name="ipstxemulatespooler"></a><span data-ttu-id="00f85-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="00f85-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="00f85-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00f85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00f85-105">Define um repositório local para emular o Gerenciador de protocolo do Outlook para spool mensagens de saída para um servidor.</span><span class="sxs-lookup"><span data-stu-id="00f85-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="00f85-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="00f85-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="00f85-107">[in] Defina este parâmetro como True se o armazenamento local deve emular o spooler; configurá-lo como False se não.</span><span class="sxs-lookup"><span data-stu-id="00f85-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00f85-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="00f85-108">Remarks</span></span>

<span data-ttu-id="00f85-109">Um repositório local chama **IPSTX::EmulateSpooler** para agir como um protocolo Gerenciador Outlook, mensagens de spooling na fila de saída para o servidor de back-end (por exemplo, servidor do MSN ou servidor AOL) para processamento.</span><span class="sxs-lookup"><span data-stu-id="00f85-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="00f85-110">Emula um spooler durante a sincronização, o armazenamento, em seguida, chama esses dois métodos:</span><span class="sxs-lookup"><span data-stu-id="00f85-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="00f85-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obter a fila de mensagens de saída no repositório.</span><span class="sxs-lookup"><span data-stu-id="00f85-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="00f85-112">Esse método for bem-sucedido apenas se o repositório é emula o Gerenciador de protocolo do Outlook.</span><span class="sxs-lookup"><span data-stu-id="00f85-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="00f85-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** para proteger o acesso único a uma mensagem na fila de saída antes de enviá-la para o servidor.</span><span class="sxs-lookup"><span data-stu-id="00f85-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="00f85-114">Esse método for bem-sucedido apenas se o repositório é emula o Gerenciador de protocolo do Outlook.</span><span class="sxs-lookup"><span data-stu-id="00f85-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="00f85-115">Após enviar a mensagem, o repositório chama esse método novamente para liberar acesso único a ele.</span><span class="sxs-lookup"><span data-stu-id="00f85-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="00f85-116">Desde o Outlook 2002, o gerente de protocolo do Outlook substituído o MAPI spooler e tornou-se responsável spooling para mensagens de saída para servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="00f85-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00f85-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="00f85-117">See also</span></span>



[<span data-ttu-id="00f85-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="00f85-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="00f85-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="00f85-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

