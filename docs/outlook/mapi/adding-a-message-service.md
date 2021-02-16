---
title: Adicionando um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407232"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="c1844-103">Adicionando um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="c1844-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="c1844-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1844-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c1844-105">**Para adicionar um novo serviço de mensagens a um perfil e acessar o novo serviço de mensagens**</span><span class="sxs-lookup"><span data-stu-id="c1844-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="c1844-106">Chame [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="c1844-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="c1844-107">**CreateMsgServiceEx** executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c1844-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="c1844-108">Copia todas as informações relevantes para o serviço de mensagens que está no MAPISVC. Arquivo INF, criando uma seção de perfil para cada seção do provedor.</span><span class="sxs-lookup"><span data-stu-id="c1844-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="c1844-109">Chama a função de ponto de entrada do serviço de mensagens, **MSGSERVICEENTRY**, com o  _parâmetro ulContext_ definido como MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="c1844-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="c1844-110">Define e recupera a propriedade PR_SERVICE_UID **(** [PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c1844-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="c1844-111">**Para acessar qualquer serviço de mensagem recém-adicionado**</span><span class="sxs-lookup"><span data-stu-id="c1844-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="c1844-112">Chame [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para recuperar a tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c1844-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="c1844-113">Chame o método [IMAPITable::Advise](imapitable-advise.md) da tabela de serviço de mensagens para se registrar para notificações de tabela.</span><span class="sxs-lookup"><span data-stu-id="c1844-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="c1844-114">Quando o MAPI envia uma TABLE_ROW_ADDED, localize o identificador de entrada do serviço de mensagens recém-adicionado na estrutura [SRow](srow.md) incluída na estrutura [TABLE_NOTIFICATION](table_notification.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="c1844-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

