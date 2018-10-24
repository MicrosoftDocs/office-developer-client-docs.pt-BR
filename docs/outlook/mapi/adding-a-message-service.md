---
title: Adicionar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6a8b0f8fc8c296fe4022ac28623b83d270472ca3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590691"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="da3b3-103">Adicionar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="da3b3-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="da3b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da3b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="da3b3-105">**Para adicionar um novo serviço de mensagem a um perfil e acessar o novo serviço de mensagem**</span><span class="sxs-lookup"><span data-stu-id="da3b3-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="da3b3-106">Chame [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="da3b3-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="da3b3-107">**CreateMsgServiceEx** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="da3b3-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="da3b3-108">Copia todas as informações relevantes para o serviço de mensagem que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção do provedor.</span><span class="sxs-lookup"><span data-stu-id="da3b3-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="da3b3-109">Chama a função de ponto de entrada do serviço de mensagem, **MSGSERVICEENTRY**, com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="da3b3-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="da3b3-110">Define e recupera a mensagem propriedade do serviço **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da3b3-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="da3b3-111">**Para acessar qualquer serviço recém-adicionado mensagem**</span><span class="sxs-lookup"><span data-stu-id="da3b3-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="da3b3-112">Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="da3b3-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="da3b3-113">Chame o método de [IMAPITable::Advise](imapitable-advise.md) de tabela serviço de mensagens para registrar para notificações de tabela.</span><span class="sxs-lookup"><span data-stu-id="da3b3-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="da3b3-114">Quando MAPI envia uma notificação TABLE_ROW_ADDED, localize o identificador de entrada do serviço recém-adicionado mensagem na estrutura [SRow](srow.md) incluída na estrutura de [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="da3b3-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

