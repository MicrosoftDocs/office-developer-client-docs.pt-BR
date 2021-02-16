---
title: Tabelas de Pastas de Recebimento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417347"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="3ce14-103">Tabelas de Pastas de Recebimento</span><span class="sxs-lookup"><span data-stu-id="3ce14-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="3ce14-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ce14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ce14-105">Uma tabela de pastas de recebimento contém informações para todas as pastas designadas como pastas de recebimento para um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3ce14-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="3ce14-106">Uma pasta de recebimento é uma pasta onde as mensagens de entrada de uma classe de mensagem específica são colocadas.</span><span class="sxs-lookup"><span data-stu-id="3ce14-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="3ce14-107">Os provedores de repositório de mensagens implementam tabelas de pastas de recebimento e os aplicativos cliente os usam fazendo uma chamada para o método [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="3ce14-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="3ce14-108">As propriedades a seguir compom o conjunto de colunas necessário nas tabelas da pasta de recebimento:</span><span class="sxs-lookup"><span data-stu-id="3ce14-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="3ce14-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ce14-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="3ce14-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ce14-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="3ce14-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3ce14-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ce14-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ce14-112">See also</span></span>



[<span data-ttu-id="3ce14-113">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="3ce14-113">MAPI Tables</span></span>](mapi-tables.md)

