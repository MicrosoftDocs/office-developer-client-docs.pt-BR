---
title: Propriedade canônica PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332855"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Propriedade canônica PidTagContainerHierarchy

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um objeto de tabela de hierarquia incorporado que fornece informações sobre os contêineres filhos. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Identificador:  <br/> |0x360E  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Contêiner  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo **PT_OBJECT**, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps; seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface IID_IMAPITable. Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable. Para obter mais informações, consulte [tabelas de hierarquia](hierarchy-tables.md). 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), e essa propriedade é semelhante ao uso. Várias propriedades MAPI fornecem acesso a tabelas: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Tabela de hierarquia  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabela de conteúdo associado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela de anexos  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabela de destinatários  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.
    
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

