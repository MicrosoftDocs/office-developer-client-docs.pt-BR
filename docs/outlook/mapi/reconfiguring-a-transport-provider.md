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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328410"
---
# <a name="reconfiguring-a-transport-provider"></a>Reconfigurando um provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Você pode usar um objeto de status do provedor de transporte para alterar algumas das propriedades do provedor. O intervalo de propriedades que podem ser alteradas depende das propriedades incluídas na folha de propriedades do provedor e de como essas propriedades são definidas. 
  
 **Para reconfigurar um provedor de transporte ativo**
  
1. Chame [IMAPISession::](imapisession-getstatustable.md) getstatustable para acessar a tabela status. 
    
2. Localize a linha do provedor de transporte a ser reconfigurada criando uma restrição de propriedade que corresponda a **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do provedor de destino. 
    
3. Call [IMAPITable:: FindRow](imapitable-findrow.md) para recuperar a linha apropriada. 
    
4. Verifique se os sinalizadores STATUS_SETTINGS_DIALOG e STATUS_VALIDATE_STATE estão definidos na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do provedor de transporte de destino. Se STATUS_SETTINGS_DIALOG não for definido, o provedor de transporte não exibirá uma folha de propriedades de configuração. Se STATUS_VALIDATE_STATE não estiver definido, você não poderá executar a reconfiguração dinâmica.
    
5. Se STATUS_SETTINGS_DIALOG estiver definido, chame [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para exibir a folha de propriedades do provedor de transporte e permitir que o usuário faça alterações. 
    
6. Depois que o usuário tiver concluído a reconfiguração, chame [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) se STATUS_VALIDATE_STATE estiver definido, passando CONFIG_CHANGED. 
    

