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
ms.openlocfilehash: 629746cedf8c6f4a8c960912a9ab1bcdc7a09e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574143"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Propriedade canônica PidTagAttachDataBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os dados de anexo binário costumam ser acessados por meio da interface de vinculação e incorporação de objetos (OLE) **IStream** . 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o anexo, quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é ATTACH_BY_VALUE, que é o método de anexo usual e a única pessoa que devem ser suportados. **PR_ATTACH_DATA_BIN** também contém um anexo OLE 1.0 **OLESTREAM** quando o valor de **PR_ATTACH_METHOD** é ATTACH_OLE. 
  
 Anexos de **OLESTREAM** podem ser copiados em um arquivo, chamando o método OLE **IStream::CopyTo** . O tipo de codificação de OLE pode ser determinado da propriedade **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para um anexo de arquivo de documento OLE, o provedor de armazenamento de mensagem deve responder a uma chamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) e, opcionalmente, pode responder a uma chamada em **PR_ATTACH_DATA_BIN **. Observe que **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas representações da mesma propriedade. 
  
Para um objeto de armazenamento, como um arquivo composto no formato de arquivo de documento OLE 2.0, alguns provedores de serviços permitem que ele seja aberto com a interface do MAPI **IStreamDocfile** para melhorar o desempenho. Um provedor que ofereça suporte a **IStreamDocfile** deve expor no **PR_ATTACH_DATA_OBJ** e, opcionalmente, pode expor-lo em **PR_ATTACH_DATA_BIN**. 
  
Para obter mais informações sobre formatos e interfaces OLE, consulte [OLE e transferência de dados](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
## <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

