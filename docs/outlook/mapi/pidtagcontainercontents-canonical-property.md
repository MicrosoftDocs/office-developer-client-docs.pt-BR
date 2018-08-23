---
title: Propriedade canônica PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d6a2f7b8b4f5345faa54e24c359f15ee181a7f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575480"
---
# <a name="pidtagcontainercontents-canonical-property"></a>Propriedade canônica PidTagContainerContents

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto table de conteúdo incorporado que fornece informações sobre um contêiner.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Identificador:  <br/> |0x360F  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo PT_OBJECT, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) ; seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface IID_IMAPITable. Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas pode, opcionalmente, relatá-la ou não se não estiver definida. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) . Para obter mais informações, consulte [As tabelas de conteúdo](contents-tables.md). 
  
Essa propriedade, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) e **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) são semelhantes em uso. Várias propriedades MAPI fornecem acesso às tabelas: 
  
|**Propriedade**|**Table**|
|:-----|:-----|
|PidTagContainerContents  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabela de hierarquia  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabela de conteúdo associado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela de anexos  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabela de destinatários  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
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
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

