---
title: Propriedade canônica PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d2926b09dd3dfd89ab771206e0c8848415238eba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585476"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Propriedade canônica PidTagAttachDataObject

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto attachment costumam ser acessado por meio da interface de vinculação e incorporação de objetos (OLE) **IStorage** . 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o anexo, quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**. O tipo de codificação de OLE pode ser determinado de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para um anexo associado com o valor **ATTACH_EMBEDDED_MSG** , a interface [IMessage:IMAPIProp](imessageimapiprop.md) pode ser usada para acesso mais rápido. 
  
Para um objeto OLE dinâmico incorporado, a propriedade **PR_ATTACH_DATA_OBJ** contém suas próprias informações de renderização e a propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) deve ser inexistente ou está vazio. 
  
Para um anexo de arquivo de documento OLE, o provedor de armazenamento de mensagem deve responder a uma chamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) em **PR_ATTACH_DATA_OBJ** e, opcionalmente, pode responder a uma chamada em **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). As propriedades **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas representações da mesma propriedade. 
  
Para um objeto de armazenamento, como um arquivo composto no formato de arquivo de documento OLE 2.0, alguns provedores de serviços permitem que ele seja aberto com a interface MAPI **IStreamDocfile** , uma subclasse de **IStream** sem membros adicionais, projetado para otimizar o desempenho. A economia potencial é suficiente para justificar a tentativa de abrir **PR_ATTACH_DATA_OBJ** por meio de **IStreamDocfile**. Se **MAPI_E_INTERFACE_NOT_SUPPORTED** for retornado, o cliente pode abrir **PR_ATTACH_DATA_BIN** com **IStream**. 
  
Se o aplicativo cliente ou o provedor de serviço não pode abrir um Subobjeto anexo usando **PR_ATTACH_DATA_OBJ** com a Ajuda de **PR_ATTACH_METHOD**, ele deve usar **PR_ATTACH_DATA_BIN**. 
  
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

