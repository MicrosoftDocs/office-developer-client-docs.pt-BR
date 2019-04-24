---
title: Propriedade canônica PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356543"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Propriedade canônica PidTagAttachDataBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém dados de anexo binários normalmente acessados por meio da interface de vinculação e incorporação de objetos (OLE) **IStream** . 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o anexo quando o valor da propriedade **PR_ATTACH_METHOD** ([PIDTAGATTACHMETHOD](pidtagattachmethod-canonical-property.md)) é ATTACH_BY_VALUE, que é o método de anexo usual e o único necessário para ter suporte. **PR_ATTACH_DATA_BIN** também mantém um anexo de **OLESTREAM** OLE 1,0 quando o valor de **PR_ATTACH_METHOD** for ATTACH_OLE. 
  
 Os anexos de **OLESTREAM** podem ser copiados em um arquivo chamando o método OLE **IStream:: CopyTo** . O tipo de codificação OLE pode ser determinado a partir da propriedade **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para um anexo de arquivo de documento OLE, o provedor do repositório de mensagens deve responder a uma chamada de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) no **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) e, opcionalmente, responder a uma chamada no **PR_ATTACH_DATA_BIN **. Observe que **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas rendições da mesma propriedade. 
  
Para um objeto de armazenamento, como um arquivo composto no formato de DOCFILE OLE 2,0, alguns provedores de serviços permitem que ele seja aberto com a interface MAPI **IStreamDocfile** para melhorar o desempenho. Um provedor que dá suporte a **IStreamDocfile** deve expô-lo no **PR_ATTACH_DATA_OBJ** e pode, opcionalmente, expô-lo em **PR_ATTACH_DATA_BIN**. 
  
Para obter mais informações sobre interfaces e formatos OLE, consulte [OLE e transferência de dados](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
## <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

