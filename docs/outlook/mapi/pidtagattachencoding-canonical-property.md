---
title: Propriedade canônica PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345490"
---
# <a name="pidtagattachencoding-canonical-property"></a>Propriedade canônica PidTagAttachEncoding

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de objeto ASN.1 que especifica a codificação de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Identificador:  <br/> |0x3702  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade identifica o algoritmo usado para transformar os dados em um anexo.
  
 **Observação** As **PR_ATTACH_ENCODING** e **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) não devem ser confundidas. Eles não estão emparelhados ou relacionados. **PR_ATTACH_TAG** identifica o aplicativo que gerou originalmente o anexo. "Object" tem um significado muito mais geral no identificador de objeto do termo e, em X.400, do que na programação orientada a objeto. 
  
A sintaxe do identificador de objeto e os identificadores de objeto de exemplo são definidos no MAPIOID. Arquivo de header H. Os valores **PR_ATTACH_ENCODING** não são limitados aos definidos em MAPIOID.H. Por exemplo, arquivos Macintosh anexados podem usar um identificador como MacBinary. 
  
Para obter informações completas sobre esses identificadores de objeto, consulte a documentação sobre ASN.1, X.208 e X.209. O identificador de objeto é encontrado no elemento de referência de aplicativo do ambiente FTBP (File Transfer Body Part). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
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

