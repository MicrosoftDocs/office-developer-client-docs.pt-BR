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
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339281"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Propriedade canônica PidTagAttachDataObject

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto Attachment normalmente acessado por meio da interface **IStorage** de vinculação e incorporaÇão de objetos (OLE). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade contém o anexo quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**. O tipo de codificação OLE pode ser determinado de **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para um anexo associado ao valor **ATTACH_EMBEDDED_MSG** , a interface [IMessage: IMAPIProp](imessageimapiprop.md) pode ser usada para acesso mais rápido. 
  
Para um objeto OLE dinâmico incorporado, a propriedade **PR_ATTACH_DATA_OBJ** contém suas próprias informações de renderização, e a propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) deve estar inexistente ou vazia. 
  
Para um anexo de arquivo de documento OLE, o provedor do repositório de mensagens deve responder a uma chamada de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) no **PR_ATTACH_DATA_OBJ** e, opcionalmente, responder a uma chamada no **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). As propriedades **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** compartilham o mesmo identificador de propriedade e, portanto, são duas rendições da mesma propriedade. 
  
Para um objeto de armazenamento, como um arquivo composto no formato de DOCFILE do OLE 2,0, alguns provedores de serviços permitem que ele seja aberto com a interface MAPI **IStreamDocfile** , uma subclasse de **IStream** sem membros adicionais, projetadas para otimizar o desempenho. O possível salvamento é suficiente para justificar a tentativa de abrir o **PR_ATTACH_DATA_OBJ** através do **IStreamDocfile**. Se **MAPI_E_INTERFACE_NOT_SUPPORTED** for retornado, o cliente poderá abrir **PR_ATTACH_DATA_BIN** com **IStream**. 
  
Se o aplicativo cliente ou provedor de serviços não puder abrir um subobjeto Attachment usando **PR_ATTACH_DATA_OBJ** com a ajuda do **PR_ATTACH_METHOD**, ele deverá usar o **PR_ATTACH_DATA_BIN**. 
  
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

