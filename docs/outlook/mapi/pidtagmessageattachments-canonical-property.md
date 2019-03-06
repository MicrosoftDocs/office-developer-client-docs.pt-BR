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
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413970"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Propriedade canônica PidTagMessageAttachments

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela de anexos para uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Identificador:  <br/> |0x0E13  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo PT_OBJECT, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps. Seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** . Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMessage::](imessage-getattachmenttable.md) GetAttachmentTable. Para obter mais informações, consulte [tabelas de anexo](attachment-tables.md). 
  
Essa propriedade pode ser usada para restrição de subobjeto especificando-a na estrutura [SSubRestriction](ssubrestriction.md) . Isso permite que o cliente limite o modo de exibição de um contêiner às mensagens com anexos que atendam aos critérios fornecidos. Uma mensagem é qualificada para exibir se pelo menos uma linha na tabela de anexos, ou seja, um anexo, satisfizer a restrição de subobjeto. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

