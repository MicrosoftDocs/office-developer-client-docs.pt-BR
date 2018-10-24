---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fe722e8723fdc3868cbbc3188f03e13ef3f466f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575333"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="c1072-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="c1072-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="c1072-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1072-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1072-105">Fornece acesso à tabela de fila saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c1072-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="c1072-106">Este método é chamado somente pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1072-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c1072-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1072-107">Parameters</span></span>

 <span data-ttu-id="c1072-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1072-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c1072-109">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c1072-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c1072-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c1072-110">_lppTable_</span></span>
  
> <span data-ttu-id="c1072-111">[out] Um ponteiro para um ponteiro para a tabela de fila de saída.</span><span class="sxs-lookup"><span data-stu-id="c1072-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1072-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c1072-112">Return value</span></span>

<span data-ttu-id="c1072-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1072-113">S_OK</span></span> 
  
> <span data-ttu-id="c1072-114">A tabela de fila de saída foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="c1072-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1072-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1072-115">Remarks</span></span>

<span data-ttu-id="c1072-116">O método **IMsgStore::GetOutgoingQueue** fornece o MAPI spooler com acesso à tabela que mostra a fila do armazenamento de mensagens de mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="c1072-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="c1072-117">Normalmente, as mensagens são colocadas na tabela de fila de saída depois seu método [IMessage::SubmitMessage](imessage-submitmessage.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="c1072-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="c1072-118">No entanto, como a ordem de envio afeta a ordem de pré-processamento e o envio para o provedor de transporte, algumas mensagens que foram marcadas para enviar talvez não apareçam na tabela de fila de saída imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c1072-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c1072-119">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="c1072-119">Notes to implementers</span></span>

<span data-ttu-id="c1072-120">Para obter uma lista das propriedades que devem ser incluídos como colunas em sua tabela de fila de saída, consulte as [Tabelas de fila de saída](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c1072-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="c1072-121">Como o spooler MAPI foi projetado para aceitar mensagens de um armazenamento de mensagens em ordem crescente de hora de envio, permitir que o spooler MAPI classificar a tabela de fila de saída para que corresponda nesta ordem ou estabelecê-la como a ordem de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="c1072-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="c1072-122">Você deve suportar as notificações para a saída tabela de fila de mensagens, garantindo que o MAPI spooler é notificado quando o conteúdo da fila for alterado.</span><span class="sxs-lookup"><span data-stu-id="c1072-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1072-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1072-123">See also</span></span>



[<span data-ttu-id="c1072-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c1072-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c1072-125">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c1072-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

