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
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436332"
---
# <a name="pidtagresourcemethods-canonical-property"></a>Propriedade canônica PidTagResourceMethods

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de sinalizadores que indicam os métodos na interface **IMAPIStatus** que são suportados pelo objeto de status. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_METHODS  <br/> |
|Identificador:  <br/> |0x3E02  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade indica quais dos métodos na implementação de **IMAPIStatus** de um objeto de status são suportados. Os objetos de status podem retornar MAPI_E_NO_SUPPORT de métodos sem suporte. 
  
Os clientes usam a propriedade PR_RESOURCE_METHODS **de** um objeto de status para evitar fazer chamadas para métodos sem suporte. Se o sinalizador que corresponde a um método específico for definido, o método existirá e poderá ser chamado. Se esse sinalizador estiver claro, o método não deve ser chamado. 
  
Os objetos de status implementados pelo MAPI suportam os seguintes métodos:
  
|**Objeto Status**|**Métodos com suporte**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**Somente ValidateState**  <br/> |
|MapI address book  <br/> |**Somente ValidateState**  <br/> |
|Spooler MAPI  <br/> |**ValidateState** e **FlushQueues** <br/> |
   
Um ou mais dos sinalizadores a seguir podem ser definidos **PR_RESOURCE_METHODS:**
  
STATUS_CHANGE_PASSWORD 
  
> Indica que o [método IMAPIStatus::ChangePassword](imapistatus-changepassword.md) é suportado. 
    
STATUS_FLUSH_QUEUES 
  
> Indica que o [método IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) é suportado. 
    
STATUS_SETTINGS_DIALOG 
  
> Indica que o [método IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) é suportado. 
    
STATUS_VALIDATE_STATE 
  
> Indica que o [método IMAPIStatus::ValidateState](imapistatus-validatestate.md) é suportado. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

