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
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415177"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propriedade canônica PidTagBodyCrc

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor CRC (verificação de redundância cíclica) no texto da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_BODY_CRC  <br/> |
|Identificador:  <br/> |0x0E1C  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

O armazenamento de mensagens pode usar qualquer algoritmo CRC que gere um PT_LONG valor. Ele deve calcular essa propriedade como parte do método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) quando a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) tiver sido definida pela primeira vez e sempre que tiver sido modificada subsequentemente.
  
Um aplicativo cliente usa **PR_BODY_CRC** para auxiliar na comparação de cadeias de caracteres de texto de mensagem contidas **PR_BODY** propriedades ou suas variantes. Usando essa propriedade, o cliente pode detectar rapidamente e facilmente quando o texto da mensagem foi alterado. Ele pode obter ganhos significativos de desempenho  usando o **PR_BODY_CRC** em vez de obter PR_BODY do armazenamento de mensagens e compará-lo com uma versão local. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

