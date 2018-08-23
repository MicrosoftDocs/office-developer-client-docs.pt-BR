---
title: Propriedade canônica PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f8260b5b7c1dd3fd6608c2fd17471d21ad362ece
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568991"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>Propriedade canônica PidTagDeferredSendUnits

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a unidade de tempo pelo qual o valor da propriedade **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) deve ser multiplicado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|Identificador:  <br/> |0x3FEC  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Se definido, esta propriedade deve ter um dos seguintes valores:
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |Descrição  <br/> |
|0  <br/> |Minutos, por exemplo, 60 segundos  <br/> |
|1  <br/> |Horas, por exemplo 60 x 60 segundos  <br/> |
|2  <br/> |Dia, por exemplo 24 x 60 x 60 segundos  <br/> |
|3  <br/> |Semana, por exemplo o 7x24x60x60 segundos  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
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

