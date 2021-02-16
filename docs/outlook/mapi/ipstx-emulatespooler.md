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
# <a name="ipstxemulatespooler"></a><span data-ttu-id="fb266-103">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="fb266-103">IPSTX::EmulateSpooler</span></span>

  
  
<span data-ttu-id="fb266-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb266-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb266-105">Define um armazenamento local para emular o Gerenciador de Protocolos do Outlook para fazer o spool de mensagens de saída para um servidor.</span><span class="sxs-lookup"><span data-stu-id="fb266-105">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>
  
```cpp
HRESULT EmulateSpooler( 
    BOOL fEmulate 
);
```

 <span data-ttu-id="fb266-106">_fEmulate_</span><span class="sxs-lookup"><span data-stu-id="fb266-106">_fEmulate_</span></span>
  
>  <span data-ttu-id="fb266-107">[in] Definir esse parâmetro como True se o armazenamento local deve emular o spooler; se não for definido como False.</span><span class="sxs-lookup"><span data-stu-id="fb266-107">[in] Set this parameter to True if the local store should emulate the spooler; set it to False if not.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fb266-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb266-108">Remarks</span></span>

<span data-ttu-id="fb266-109">Um armazenamento local chama **IPSTX::EmulateSpooler** para atuar como um Gerenciador de Protocolos do Outlook, spooling de mensagens na fila de saída para o servidor back-end (por exemplo, servidor MSN ou servidor AOL) para processamento.</span><span class="sxs-lookup"><span data-stu-id="fb266-109">A local store calls **IPSTX::EmulateSpooler** to act as an Outlook Protocol Manager, spooling messages in the outgoing queue to the back-end server (for example, MSN server or AOL server) for processing.</span></span> <span data-ttu-id="fb266-110">Emulando um spooler durante a sincronização, o armazenamento chama esses dois métodos:</span><span class="sxs-lookup"><span data-stu-id="fb266-110">Emulating a spooler during synchronization, the store then calls these two methods:</span></span> 
  
1. <span data-ttu-id="fb266-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** para obter a fila de saída de mensagens no repositório.</span><span class="sxs-lookup"><span data-stu-id="fb266-111">**[IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)** to get the outgoing queue of messages in the store.</span></span> <span data-ttu-id="fb266-112">Esse método só será bem-sucedido se o armazenamento estiver emulando o Outlook Protocol Manager.</span><span class="sxs-lookup"><span data-stu-id="fb266-112">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> 
    
2. <span data-ttu-id="fb266-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** para proteger o único acesso a uma mensagem na fila de saída antes de enviá-la para o servidor.</span><span class="sxs-lookup"><span data-stu-id="fb266-113">**[IMsgStore::SetLockState](imsgstore-setlockstate.md)** to secure sole access to a message in the outgoing queue just before sending it to the server.</span></span> <span data-ttu-id="fb266-114">Esse método só será bem-sucedido se o armazenamento estiver emulando o Gerenciador de Protocolo do Outlook.</span><span class="sxs-lookup"><span data-stu-id="fb266-114">This method succeeds only if the store is emulating the Outlook Protocol Manager.</span></span> <span data-ttu-id="fb266-115">Depois de enviar a mensagem, o armazenamento chama esse método novamente para liberar o único acesso a ela.</span><span class="sxs-lookup"><span data-stu-id="fb266-115">After sending the message, the store calls this method again to release sole access to it.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="fb266-116">Desde o Outlook 2002, o Gerenciador de Protocolos do Outlook substituiu o spooler MAPI e se tornou responsável pelo spooling de mensagens de saída para servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="fb266-116">Since Outlook 2002, the Outlook Protocol Manager replaced the MAPI spooler and became responsible for spooling outgoing messages to back-end servers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb266-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb266-117">See also</span></span>



[<span data-ttu-id="fb266-118">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fb266-118">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)
  
[<span data-ttu-id="fb266-119">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="fb266-119">IPSTX::GetSyncObject</span></span>](ipstx-getsyncobject.md)

