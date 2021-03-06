---
title: Reconfigurando um provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408405"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfigurando um provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode usar o objeto de status de um provedor de transporte para alterar algumas das propriedades do provedor. O intervalo de propriedades que podem ser alteradas depende das propriedades incluídas na folha de propriedades do provedor e de como essas propriedades são definidas. 
  
 **Para reconfigurar um provedor de transporte ativo**
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Localize a linha para o provedor de transporte a ser reconfigurado criando uma restrição de propriedade que corresponde PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do provedor de destino. 
    
3. Chame [IMAPITable::FindRow](imapitable-findrow.md) para recuperar a linha apropriada. 
    
4. Verifique se os sinalizadores STATUS_SETTINGS_DIALOG e STATUS_VALIDATE_STATE estão definidos na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do provedor de transporte de destino. Se STATUS_SETTINGS_DIALOG não estiver definida, o provedor de transporte não exibirá uma folha de propriedades de configuração. Se STATUS_VALIDATE_STATE não estiver definido, não será possível executar a reconfiguração dinâmica.
    
5. Se STATUS_SETTINGS_DIALOG estiver definido, chame [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para exibir a folha de propriedades do provedor de transporte e permitir que o usuário faça alterações. 
    
6. Depois que o usuário terminar a reconfiguração, chame [IMAPIStatus::ValidateState](imapistatus-validatestate.md) se STATUS_VALIDATE_STATE estiver definido, passando CONFIG_CHANGED. 
    

