---
title: Propriedade canônica PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355682"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Propriedade canônica PidTagMessageRecipients

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela de restrições que pode ser aplicada a uma tabela de conteúdo para encontrar todas as mensagens que contêm subobjetos de destinatário que atendem às restrições. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Identificador:  <br/> |0x0E12  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser excluída nas [operações IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como uma propriedade do **tipo PT_OBJECT**, ela não pode ser recuperada com êxito pelo [método IMAPIProp::GetProps.](imapiprop-getprops.md) Seu conteúdo deve ser acessado pelo [método IMAPIProp::OpenProperty,](imapiprop-openproperty.md) solicitando o **identificador IID_IMAPITable** interface. Os provedores de serviços devem reportá-lo ao método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas, opcionalmente, pode relaí-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o [método IMessage::GetRecipientTable.](imessage-getrecipienttable.md) 
  
Essa propriedade pode ser usada para restrição de subobjeto especificando-a na [estrutura SSubRestriction.](ssubrestriction.md) Isso permite que um cliente limite a exibição de um contêiner a mensagens com destinatários que atenderem a determinados critérios. Uma mensagem se qualifica para exibição se pelo menos uma linha em sua tabela de destinatários, ou seja, um destinatário satisfaz a restrição de subobjeto. 
  
 **Observação** O uso de resultados de restrição de subobjeto equivale a uma chamada [IMAPISession::OpenEntry](imapisession-openentry.md) em cada mensagem na tabela. Dependendo do aplicativo cliente e do número de mensagens a serem pesquisadas, isso pode afetar o desempenho. 
  
A **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) e essa propriedade são semelhantes em uso. Várias propriedades MAPI fornecem acesso a tabelas: 
  
|**Propriedade**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabela Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabela de conteúdo associada  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela attachment  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Tabela Recipient  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente do fluxo.
    
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

