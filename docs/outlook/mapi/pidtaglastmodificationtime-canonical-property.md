---
title: Propriedade canônico PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: bf58e0598af6eb833b003b824be95f8fb82bd8bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19769431"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propriedade canônico PidTagLastModificationTime

  
  
**Aplica-se a**: Outlook 
  
Contém a data e hora que o objeto ou subobjeto última modificação. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificador:  <br/> |0x3008  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Hora da mensagem  <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa propriedade é definida inicialmente para o mesmo valor que a propriedade **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Anexo subobjetos atualizá-la, conforme necessário, copiando a hora da última modificação mantida pelo sistema de arquivo nativo. Um aplicativo cliente pode definir essa propriedade até a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . A partir do provedor deve atualizar **PR_LAST_MODIFICATION_TIME** durante cada chamada **IMAPIProp::SaveChanges** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

