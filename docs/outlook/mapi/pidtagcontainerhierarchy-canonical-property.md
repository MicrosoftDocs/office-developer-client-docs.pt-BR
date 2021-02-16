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
  
Contém um objeto de tabela de hierarquia incorporado que fornece informações sobre os contêineres filho. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Identificador:  <br/> |0x360E  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Contêiner  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser excluída nas [operações IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como uma propriedade do **tipo PT_OBJECT**, ela não pode ser recuperada com êxito pelo [método IMAPIProp::GetProps;](imapiprop-getprops.md) seu conteúdo deve ser acessado pelo [método IMAPIProp::OpenProperty,](imapiprop-openproperty.md) solicitando o identificador IID_IMAPITable interface. Os provedores de serviços devem reportá-lo para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas, opcionalmente, pode reportá-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o [método IMAPIContainer::GetHierarchyTable.](imapicontainer-gethierarchytable.md) Para obter mais informações, consulte [Tabelas de Hierarquia.](hierarchy-tables.md) 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) e essa propriedade são semelhantes no uso. Várias propriedades MAPI fornecem acesso a tabelas: 
  
|**Propriedade**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Tabela Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabela de conteúdo associada  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Tabela recipient  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.
    
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

