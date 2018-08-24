---
title: Propriedade canônica PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fd98044868bbec36ed14fcf90deb2990039244b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573737"
---
# <a name="pidtagattachsize-canonical-property"></a>Propriedade canônica PidTagAttachSize

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a soma, em bytes, dos tamanhos de todas as propriedades em um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_SIZE  <br/> |
|Identificador:  <br/> |0x0E20  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que o anexo subobjetos exponham a propriedade **PR_ATTACH_SIZE** . A soma contida no **PR_ATTACH_SIZE** inclui o tamanho da propriedade **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) ou **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Apropriadamente, **PR_ATTACH_SIZE** é geralmente maior do que o conteúdo do anexo sozinho. 
  
Essa propriedade pode ser usada para verificar o tamanho aproximado do anexo antes de executar uma transferência remota pelo modem e para exibir os indicadores de progresso quando salvar o anexo em disco. É especialmente útil com os objetos OLE anexados. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

