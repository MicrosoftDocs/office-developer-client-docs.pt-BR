---
title: Propriedade canônica PidTagExpiryUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1c753bb84ccbfe2fa6869d56806fd042a6d60e9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769217"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Propriedade canônica PidTagExpiryUnits

  
  
**Aplica-se a**: Outlook 
  
Descreve a unidade de tempo quando a propriedade **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) multiplica.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificador:  <br/> |0x3FEE  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, se definida, deve ser um dos seguintes valores:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Descrição (TimeOf)  <br/> |
|0x00000000  <br/> |Minutos, por exemplo, 60 segundos  <br/> |
|0x00000001  <br/> |Horas, por exemplo 60 x 60 segundos  <br/> |
|0x00000002  <br/> |Dia, por exemplo 24 x 60 x 60 segundos  <br/> |
|0x00000003  <br/> |Semana, por exemplo o 7x24x60x60 segundos  <br/> |
   
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

