---
title: Propriedade canônica PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316300"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>Propriedade canônica PidTagFolderAssociatedContents

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto da tabela de conteúdo incorporado que fornece informações sobre a tabela de conteúdo associado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|Identificador:  <br/> |0x3610  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela de conteúdo associada representa uma subpasta que não aparece na tabela conteúdo padrão. Ele contém as mensagens associadas, ou ocultas, da pasta. 
  
Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo **PT_OBJECT**, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps; seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** . Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, os aplicativos cliente devem chamar o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable. Para obter mais informações sobre tabelas de conteúdo da pasta, consulte [tabelas de conteúdo](contents-tables.md) e [exibição de uma tabela de conteúdo da pasta](displaying-a-folder-contents-table.md). 
  
O **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), e essa propriedade é semelhante ao uso. Várias propriedades MAPI fornecem acesso a tabelas: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabela de hierarquia  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |Tabela de conteúdo associado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela de anexos  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabela de destinatários  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os itens de compromisso e reunião.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

