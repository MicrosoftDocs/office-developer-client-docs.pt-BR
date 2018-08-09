---
title: Propriedade canônica PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769021"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propriedade canônica PidTagBodyCrc

  
  
**Aplica-se a**: Outlook 
  
Contém um valor de verificação (CRC) redundância cíclica no texto da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_BODY_CRC  <br/> |
|Identificador:  <br/> |0x0E1C  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

O armazenamento de mensagens pode usar qualquer algoritmo CRC que gera um valor PT_LONG. Quando a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) tiver sido definida pela primeira vez e sempre que tiver sido modificada posteriormente, ele deverá calcular essa propriedade como parte do método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .
  
Um aplicativo cliente usa **PR_BODY_CRC** para auxiliar na comparação de cadeias de caracteres de texto de mensagem contidas em propriedades **PR_BODY** ou suas respectivas variantes. O uso desta propriedade, o cliente pode rapidez e facilidade detectar quando o texto da mensagem foi alterada. Ele pode aproveitar os ganhos significativos de desempenho usando **PR_BODY_CRC** em vez de obtendo **PR_BODY** de armazenamento de mensagens e comparando-os com uma versão local. 
  
## <a name="related-resources"></a>Recursos relacionados

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

