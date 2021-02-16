---
title: Configurando um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434505"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="127cc-103">Configurando um serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="127cc-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="127cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="127cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="127cc-105">**Para configurar todos os provedores de serviços em um serviço de mensagens**</span><span class="sxs-lookup"><span data-stu-id="127cc-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="127cc-106">Chame [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="127cc-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="127cc-107">Se todos os dados necessários para a configuração estão disponíveis programaticamente, você pode escolher se exibirá ou não uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="127cc-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="127cc-108">No entanto, se algumas das informações de um ou mais provedores não estão disponíveis, certifique-se de definir o SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS sinalizador.</span><span class="sxs-lookup"><span data-stu-id="127cc-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="127cc-109">Suprimir uma interface do usuário quando os dados de configuração necessários não estão disponíveis resulta em um serviço de mensagens não configurado.</span><span class="sxs-lookup"><span data-stu-id="127cc-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="127cc-110">**Para configurar um único provedor de serviços em um serviço de mensagens**</span><span class="sxs-lookup"><span data-stu-id="127cc-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="127cc-111">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar o objeto de status do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="127cc-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="127cc-112">Chame [IMAPIStatus::SettingsDialog para](imapistatus-settingsdialog.md) exibir a folha de propriedades do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="127cc-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="127cc-113">Para obter mais informações sobre como usar objetos de status, consulte [Status Table and Status Objects](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="127cc-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

