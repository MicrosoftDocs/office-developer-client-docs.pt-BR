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
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328180"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="46c46-103">Adicionar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="46c46-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="46c46-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46c46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="46c46-105">**Para adicionar um novo serviço de mensagens a um perfil e acessar o novo serviço de mensagens**</span><span class="sxs-lookup"><span data-stu-id="46c46-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="46c46-106">Chamar [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="46c46-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="46c46-107">O **CreateMsgServiceEx** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="46c46-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="46c46-108">Copia todas as informações relevantes para o serviço de mensagens que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção de provedor.</span><span class="sxs-lookup"><span data-stu-id="46c46-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="46c46-109">Chama a função de ponto de entrada do serviço de mensagens, **MSGSERVICEENTRY**, com o parâmetro _ULCONTEXT_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="46c46-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="46c46-110">Define e recupera a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="46c46-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="46c46-111">**Para acessar qualquer serviço de mensagens recém-adicionado**</span><span class="sxs-lookup"><span data-stu-id="46c46-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="46c46-112">Chame [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="46c46-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="46c46-113">Chame o método imApitable [:: Advise](imapitable-advise.md) da tabela de serviço de mensagens para se registrar para notificações de tabela.</span><span class="sxs-lookup"><span data-stu-id="46c46-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="46c46-114">Quando MAPI envia uma notificação TABLE_ROW_ADDED, localize o identificador de entrada do serviço de mensagens recém-adicionado na estrutura [SRow](srow.md) incluída na estrutura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="46c46-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

