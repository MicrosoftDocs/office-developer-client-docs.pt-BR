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
# <a name="configuring-a-message-service"></a>Configurando um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para configurar todos os provedores de serviços em um serviço de mensagens**
  
- Chame [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Se todos os dados necessários para a configuração estão disponíveis programaticamente, você pode escolher se exibirá ou não uma interface do usuário. No entanto, se algumas das informações de um ou mais provedores não estão disponíveis, certifique-se de definir o SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS sinalizador. Suprimir uma interface do usuário quando os dados de configuração necessários não estão disponíveis resulta em um serviço de mensagens não configurado.
    
 **Para configurar um único provedor de serviços em um serviço de mensagens**
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar o objeto de status do provedor de serviços. 
    
2. Chame [IMAPIStatus::SettingsDialog para](imapistatus-settingsdialog.md) exibir a folha de propriedades do provedor de serviços. 
    
Para obter mais informações sobre como usar objetos de status, consulte [Status Table and Status Objects](status-table-and-status-objects.md).
  

