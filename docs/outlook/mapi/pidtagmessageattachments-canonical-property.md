---
title: Propriedade canônica PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342563"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Propriedade canônica PidTagMessageAttachments

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela de anexos de uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Identificador:  <br/> |0x0E13  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser excluída nas [operações IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como uma propriedade do tipo PT_OBJECT, ela não pode ser recuperada com êxito pelo [método IMAPIProp::GetProps.](imapiprop-getprops.md) Seu conteúdo deve ser acessado pelo [método IMAPIProp::OpenProperty,](imapiprop-openproperty.md) solicitando o **identificador IID_IMAPITable** interface. Os provedores de serviços devem reportá-lo ao método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas, opcionalmente, pode relaí-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o [método IMessage::GetAttachmentTable.](imessage-getattachmenttable.md) Para obter mais informações, consulte [Attachment Tables](attachment-tables.md). 
  
Essa propriedade pode ser usada para restrição de subobjeto especificando-a na [estrutura SSubRestriction.](ssubrestriction.md) Isso permite que o cliente limite a exibição de um contêiner a mensagens com anexos que atenderem a determinados critérios. Uma mensagem se qualifica para exibição se pelo menos uma linha em sua tabela de anexos, ou seja, um anexo, satisfaz a restrição de subobjeto. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.
    
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

