---
title: Configurar um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564105"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="9d059-103">Configurar um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="9d059-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="9d059-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d059-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9d059-105">**Para configurar todos os provedores de serviço em um serviço de mensagem**</span><span class="sxs-lookup"><span data-stu-id="9d059-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="9d059-106">Chame [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="9d059-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="9d059-107">Se todos os dados necessários para que a configuração está disponível por meio de programação, você poderá escolher se deseja ou não exibir uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="9d059-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="9d059-108">No entanto, se algumas das informações para um ou mais provedores não estiver disponível, certifique-se de que você defina o sinalizador SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="9d059-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="9d059-109">Suprimindo uma interface de usuário quando os dados de configuração necessárias estão indisponíveis resulta em um serviço de mensagem não configurado.</span><span class="sxs-lookup"><span data-stu-id="9d059-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="9d059-110">**Para configurar um provedor de serviços único em um serviço de mensagem**</span><span class="sxs-lookup"><span data-stu-id="9d059-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="9d059-111">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar o objeto de status do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="9d059-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="9d059-112">Chame [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para exibir a folha de propriedades do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="9d059-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="9d059-113">Para obter mais informações sobre como usar objetos de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9d059-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

