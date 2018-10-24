---
title: Receber tabelas de pastas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573177"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="6fbbb-103">Receber tabelas de pastas</span><span class="sxs-lookup"><span data-stu-id="6fbbb-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="6fbbb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fbbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fbbb-105">Uma tabela de pasta de recebimento contém informações para todas as pastas designadas como pastas de recebimento para um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6fbbb-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="6fbbb-106">Uma pasta de recebimento é uma pasta em que as mensagens recebidas de uma classe de mensagem específica são colocadas.</span><span class="sxs-lookup"><span data-stu-id="6fbbb-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="6fbbb-107">Tabelas de pasta de recebimento de implementar de provedores de repositório de mensagem e aplicativos cliente usá-las fazendo uma chamada ao método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="6fbbb-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="6fbbb-108">A seguintes propriedades formam a coluna necessária definir em receber tabelas de pasta:</span><span class="sxs-lookup"><span data-stu-id="6fbbb-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="6fbbb-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fbbb-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="6fbbb-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fbbb-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="6fbbb-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fbbb-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6fbbb-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fbbb-112">See also</span></span>



[<span data-ttu-id="6fbbb-113">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="6fbbb-113">MAPI Tables</span></span>](mapi-tables.md)

