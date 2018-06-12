---
title: Adição de um serviço de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766118"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="63b71-103">Adição de um serviço de mensagem</span><span class="sxs-lookup"><span data-stu-id="63b71-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="63b71-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63b71-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="63b71-105">**Para adicionar um novo serviço de mensagem a um perfil e acessar o novo serviço de mensagem**</span><span class="sxs-lookup"><span data-stu-id="63b71-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="63b71-106">Chame [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="63b71-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="63b71-107">**CreateMsgServiceEx** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="63b71-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="63b71-108">Copia todas as informações relevantes para o serviço de mensagem que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção do provedor.</span><span class="sxs-lookup"><span data-stu-id="63b71-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="63b71-109">Chama a função de ponto de entrada do serviço de mensagem, **MSGSERVICEENTRY**, com o parâmetro _ulContext_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="63b71-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="63b71-110">Define e recupera a mensagem propriedade do serviço **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63b71-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="63b71-111">**Para acessar qualquer serviço recém-adicionado mensagem**</span><span class="sxs-lookup"><span data-stu-id="63b71-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="63b71-112">Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b71-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="63b71-113">Chame o método de [IMAPITable::Advise](imapitable-advise.md) de tabela serviço de mensagens para registrar para notificações de tabela.</span><span class="sxs-lookup"><span data-stu-id="63b71-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="63b71-114">Quando MAPI envia uma notificação TABLE_ROW_ADDED, localize o identificador de entrada do serviço recém-adicionado mensagem na estrutura [SRow](srow.md) incluída na estrutura de [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="63b71-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

