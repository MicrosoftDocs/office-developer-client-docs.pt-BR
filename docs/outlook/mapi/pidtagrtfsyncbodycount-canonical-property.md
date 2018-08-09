---
title: Propriedade canônica PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 09274c21df3a93abc19aa8158da976e2d16f3e7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769899"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>Propriedade canônica PidTagRtfSyncBodyCount

  
  
**Aplica-se a**: Outlook 
  
Contém uma contagem dos caracteres significativos do texto da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|Identificador:  <br/> |0x1007  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensagem MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A função [RTFSync](rtfsync.md) calcula a contagem de caracteres no texto usando apenas aqueles que ele considera como significativo à mensagem. Por exemplo, alguns espaços em branco e outros caracteres ignorável forem omitidos da contagem. 
  
Essa propriedade é uma propriedade de auxiliar formato Rich Text (RTF). Essas propriedades são usadas pela função **RTFSync** e não se destina a ser usado diretamente por aplicativos do cliente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.
    
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
