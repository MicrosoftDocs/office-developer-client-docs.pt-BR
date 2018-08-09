---
title: Tabelas de filas de saída
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 10890c1fe430ddbc45c16908df3ac340284c9f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768190"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="10aac-103">Tabelas de filas de saída</span><span class="sxs-lookup"><span data-stu-id="10aac-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="10aac-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10aac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10aac-105">Uma tabela de fila de saída contém informações sobre todas as mensagens de saída para um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="10aac-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="10aac-106">Provedores de armazenamento de mensagem implementam tabelas de fila de saída para o MAPI spooler usar.</span><span class="sxs-lookup"><span data-stu-id="10aac-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="10aac-107">Repositórios que não têm suporte para o envio ou recebimento de mensagens não precisa implementar nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="10aac-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="10aac-108">Para acessar uma tabela de fila de saída, o MAPI spooler chama o método [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="10aac-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="10aac-109">Não há um requisito para que as mensagens sejam preprocessadas e enviadas para o provedor de transporte na mesma ordem em que foram enviadas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="10aac-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="10aac-110">O MAPI spooler foi projetado para aceitar mensagens de armazenamento de mensagens em ordem crescente de tempo de envio.</span><span class="sxs-lookup"><span data-stu-id="10aac-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="10aac-111">Devido a esse requisito, pode haver algumas atraso antes de algumas mensagens aparecem na tabela de fila de saída.</span><span class="sxs-lookup"><span data-stu-id="10aac-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="10aac-112">Repositórios de mensagem seja devem permitir a classificação na tabela de fila de saída para que o MAPI spooler pode classificar as mensagens por hora de envio, ou a ordem de classificação padrão deve ser por hora de envio de em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="10aac-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="10aac-113">A tabela de fila de saída deve enviar notificações quando o conteúdo da fila é alterado.</span><span class="sxs-lookup"><span data-stu-id="10aac-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="10aac-114">As seguintes propriedades compõem a coluna necessária definida nas tabelas de fila de saída:</span><span class="sxs-lookup"><span data-stu-id="10aac-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10aac-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="10aac-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="10aac-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="10aac-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="10aac-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="10aac-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="10aac-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="10aac-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="10aac-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="10aac-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="10aac-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="10aac-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="10aac-126">Para obter mais informações sobre como a tabela de fila de saída é usada, consulte [Enviando mensagens por provedores de repositório de mensagem usando](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="10aac-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10aac-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="10aac-127">See also</span></span>



[<span data-ttu-id="10aac-128">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="10aac-128">MAPI Tables</span></span>](mapi-tables.md)

