---
title: Propriedade canônica PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2e1cff8148815c3e03b92e4d57d1c6a303943c9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578161"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propriedade canônica PidTagResourceMethods

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask dos sinalizadores que indicam os métodos na interface do **IMAPIStatus** que são compatíveis com o objeto de status. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificador:  <br/> |0x3E02  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade indica que os métodos de implementação de um objeto status de **IMAPIStatus** são suportados. Objetos de status são permitidos para retornar MAPI_E_NO_SUPPORT de métodos não suportados. 
  
Clientes usam status **PR_RESOURCE_METHODS** propriedade de um objeto para evitar fazer chamadas para os métodos sem suporte. Se o sinalizador que corresponde a um determinado método for definido, o método existe e pode ser chamado. Se esse sinalizador estiver desmarcada, o método não deve ser chamado. 
  
Os objetos de status implementadas pelo suporte a MAPI os seguintes métodos:
  
|**Objeto de status**|**Métodos com suporte**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState** apenas  <br/> |
|Catálogo de endereços MAPI  <br/> |**ValidateState** apenas  <br/> |
|Spooler MAPI  <br/> |**ValidateState** e **FlushQueues** <br/> |
   
Um ou mais dos seguintes sinalizadores podem ser definido em **PR_RESOURCE_METHODS**:
  
STATUS_CHANGE_PASSWORD 
  
> Indica que o método [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) é suportado. 
    
STATUS_FLUSH_QUEUES 
  
> Indica que o método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) é suportado. 
    
STATUS_SETTINGS_DIALOG 
  
> Indica que o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) é suportado. 
    
STATUS_VALIDATE_STATE 
  
> Indica que o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) é suportado. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

