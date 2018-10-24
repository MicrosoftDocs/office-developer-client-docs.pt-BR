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
# <a name="configuring-a-message-service"></a>Configurar um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para configurar todos os provedores de serviço em um serviço de mensagem**
  
- Chame [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Se todos os dados necessários para que a configuração está disponível por meio de programação, você poderá escolher se deseja ou não exibir uma interface de usuário. No entanto, se algumas das informações para um ou mais provedores não estiver disponível, certifique-se de que você defina o sinalizador SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. Suprimindo uma interface de usuário quando os dados de configuração necessárias estão indisponíveis resulta em um serviço de mensagem não configurado.
    
 **Para configurar um provedor de serviços único em um serviço de mensagem**
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar o objeto de status do provedor de serviços. 
    
2. Chame [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para exibir a folha de propriedades do provedor de serviços. 
    
Para obter mais informações sobre como usar objetos de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).
  

