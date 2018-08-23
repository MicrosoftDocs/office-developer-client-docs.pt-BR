---
title: Propriedade canônica PidTagAccessLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ddb667715903656291a21ebb835690768146ee9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575221"
---
# <a name="pidtagaccesslevel-canonical-property"></a>Propriedade canônica PidTagAccessLevel

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o nível de acesso do cliente para o objeto.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ACCESS_LEVEL  <br/> |
|Identificador:  <br/> |0x0FF7  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Propriedades de controle de acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura para o cliente. Ele deve ser um dos seguintes valores:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |Somente leitura  <br/> |
|0x00000001  <br/> |Modify  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

