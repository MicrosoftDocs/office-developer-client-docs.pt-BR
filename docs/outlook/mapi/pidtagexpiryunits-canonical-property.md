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
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316405"
---
# <a name="pidtagexpiryunits-canonical-property"></a>Propriedade canônica PidTagExpiryUnits

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve a unidade de tempo quando a **PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) se multiplica.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EXPIRY_UNITS  <br/> |
|Identificador:  <br/> |0x3FEE  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade, se definida, deve ser um dos seguintes valores:
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |Description (TimeOf)  <br/> |
|0x00000000  <br/> |Minutos, por exemplo, 60 segundos  <br/> |
|0x00000001  <br/> |Horas, por exemplo, 60 x 60 segundos  <br/> |
|0x00000002  <br/> |Day, for example 24x60x60 seconds  <br/> |
|0x00000003  <br/> |Semana, por exemplo, 7x24x60x60 segundos  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
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

