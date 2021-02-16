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
  
Contém dados de anexo binário geralmente acessados por meio da interface **IStream** de Vínculo e Incorporação de Objeto (OLE). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o anexo quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é ATTACH_BY_VALUE, que é o método de anexo comum e o único necessário para ter suporte. **PR_ATTACH_DATA_BIN** também mantém um anexo OLE 1.0 **OLESTREAM** **quando** o valor de PR_ATTACH_METHOD é ATTACH_OLE. 
  
 **Os anexos OLESTREAM** podem ser copiados para um arquivo chamando o método **OLE IStream::CopyTo.** O tipo de codificação OLE pode ser determinado na propriedade **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para um anexo de arquivo de documento OLE, o provedor de armazenamento de mensagens deve responder a uma chamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **no PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) e, opcionalmente, pode responder a uma chamada em **PR_ATTACH_DATA_BIN**. Observe que **PR_ATTACH_DATA_BIN** **e PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas representações da mesma propriedade. 
  
Para um objeto de armazenamento, como um arquivo composto no formato docfile OLE 2.0, alguns provedores de serviços permitem que ele seja aberto com a interface **IStreamDocfile** MAPI para melhorar o desempenho. Um provedor que dá **suporte a IStreamDocfile** deve expô-lo **PR_ATTACH_DATA_OBJ** e, opcionalmente, pode expô-lo **em PR_ATTACH_DATA_BIN**. 
  
Para obter mais informações sobre interfaces e formatos OLE, consulte [OLE e Transferência de Dados.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx) 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
## <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

