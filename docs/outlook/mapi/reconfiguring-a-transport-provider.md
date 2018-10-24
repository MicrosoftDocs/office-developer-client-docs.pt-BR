---
title: Reconfigurar um provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5e7c94b387a5fe9f9682854de4097f6f1bbcd786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565596"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfigurar um provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode usar o objeto de status de um provedor de transporte para alterar algumas das propriedades do provedor. As propriedades que são fornecidas com o provedor folha de propriedades e como essas propriedades são definidas depende do intervalo de propriedades que podem ser alteradas. 
  
 **Para reconfigurar um provedor de transporte ativo**
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Localize a linha para o provedor de transporte sejam reconfigurados criando uma restrição de propriedade que corresponda **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do provedor de destino. 
    
3. Chame [IMAPITable:: FindRow](imapitable-findrow.md) para recuperar a linha apropriada. 
    
4. Verifique se os sinalizadores STATUS_SETTINGS_DIALOG e STATUS_VALIDATE_STATE estão definidos na propriedade de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do provedor de transporte de destino. Se STATUS_SETTINGS_DIALOG não estiver definida, o provedor de transporte não exibe uma folha de propriedades de configuração. Se STATUS_VALIDATE_STATE não estiver definida, você não pode executar reconfiguração dinâmica.
    
5. Se STATUS_SETTINGS_DIALOG estiver definida, chame [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para exibir a folha de propriedades do provedor de transporte e permitir que o usuário faça alterações. 
    
6. Após o usuário ter concluído com a reconfiguração, chame [IMAPIStatus::ValidateState](imapistatus-validatestate.md) se STATUS_VALIDATE_STATE for definido, passando CONFIG_CHANGED. 
    

