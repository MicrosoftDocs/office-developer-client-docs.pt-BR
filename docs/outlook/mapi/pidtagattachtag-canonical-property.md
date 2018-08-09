---
title: Propriedade canônica PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d8d8d32bddb98e0ac180b0898478c67297980492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769009"
---
# <a name="pidtagattachtag-canonical-property"></a>Propriedade canônica PidTagAttachTag

  
  
**Aplica-se a**: Outlook 
  
Contém um identificador de objeto de ASN. 1 que especifica o aplicativo que forneceu um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_TAG  <br/> |
|Identificador:  <br/> |0x370A  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade identifica o aplicativo que gerou originalmente o anexo.
  
 **Observação** As propriedades **PR_ATTACH_TAG** de **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) e não devem ser confundidas. Eles não são combinados ou relacionados. **PR_ATTACH_ENCODING** identifica o algoritmo usado para transformar os dados em um anexo. "Objeto" tem um significado muito mais geral do identificador de objeto do termo e na utilização de x. 400, que na programação orientado a objetos. 
  
Identificadores de objeto do objeto identificador sintaxe e exemplo forem definidos no MAPIOID. Arquivo de cabeçalho H. Valores para **PR_ATTACH_TAG** não estão limitados àqueles definidos no MAPIOID. H. 
  
Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN. 1, X.208 e 209. O identificador de objeto é encontrado no elemento de referência do aplicativo do ambiente do arquivo transferir corpo parte (FTBP). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

