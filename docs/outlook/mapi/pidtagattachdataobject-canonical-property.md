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
  
Contém um objeto attachment normalmente acessado por meio da interface **IStorage** OLE (Object Linking and Embedding). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade retém o anexo quando o valor da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) é **ATTACH_EMBEDDED_MSG** ou **ATTACH_OLE**. O tipo de codificação OLE pode ser determinado PR_ATTACH_TAG **(** [PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Para um anexo associado ao valor **ATTACH_EMBEDDED_MSG,** a interface [IMessage:IMAPIProp](imessageimapiprop.md) pode ser usada para acesso mais rápido. 
  
Para um objeto OLE dinâmico incorporado, **a** propriedade PR_ATTACH_DATA_OBJ contém suas próprias informações de renderização e a propriedade **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) deve ser inexistente ou vazio. 
  
Para um anexo de arquivo de documento OLE, o provedor de armazenamento de mensagens deve responder a uma chamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) no **PR_ATTACH_DATA_OBJ** e, opcionalmente, pode responder a uma chamada no **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). As **PR_ATTACH_DATA_BIN** e **PR_ATTACH_DATA_OBJ** propriedades compartilham o mesmo identificador de propriedade e, portanto, são duas representações da mesma propriedade. 
  
Para um objeto de armazenamento, como um arquivo composto no formato docfile OLE 2.0, alguns provedores de serviços permitem que ele seja aberto com a interface **IStreamDocfile** MAPI, uma subclasse **de IStream** sem membros adicionais, projetada para otimizar o desempenho. O possível salvar é suficiente para justificar a tentativa de abrir **PR_ATTACH_DATA_OBJ** por **meio de IStreamDocfile**. Se **MAPI_E_INTERFACE_NOT_SUPPORTED** for retornado, o cliente poderá **abri-PR_ATTACH_DATA_BIN** com **IStream.** 
  
Se o aplicativo cliente ou o provedor de serviços não puder abrir um subobjeto de anexo usando o **PR_ATTACH_DATA_OBJ** com a ajuda do **PR_ATTACH_METHOD**, ele deverá **usar** PR_ATTACH_DATA_BIN . 
  
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

