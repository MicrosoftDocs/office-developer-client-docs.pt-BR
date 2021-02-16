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
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361079"
---
# <a name="pidtagattachtag-canonical-property"></a>Propriedade canônica PidTagAttachTag

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de objeto ASN.1 especificando o aplicativo que forneceu um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_TAG  <br/> |
|Identificador:  <br/> |0x370A  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade identifica o aplicativo que gerou originalmente o anexo.
  
 **Observação** As **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  e PR_ATTACH_TAG propriedades não devem ser confundidas. Eles não estão emparelhados ou relacionados. **PR_ATTACH_ENCODING** identifica o algoritmo usado para transformar os dados em um anexo. "Object" tem um significado muito mais geral no identificador de objeto do termo e no uso de X.400 do que na programação orientada a objeto. 
  
A sintaxe do identificador de objeto e os identificadores de objeto de exemplo são definidos no MAPIOID. Arquivo de header H. Os valores **PR_ATTACH_TAG** não são limitados aos definidos em MAPIOID.H. 
  
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



[Propriedade canônica PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

