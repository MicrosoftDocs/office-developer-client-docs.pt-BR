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
  
Contém uma tabela de restrições que podem ser aplicadas a uma tabela de conteúdo para localizar todas as mensagens que contenham subobjetos de destinatário que atendam às restrições. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Identificador:  <br/> |0x0E12  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo **PT_OBJECT**, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps. Seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** . Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable. 
  
Essa propriedade pode ser usada para restrição de subobjeto especificando-a na estrutura [SSubRestriction](ssubrestriction.md) . Isso permite que um cliente limite o modo de exibição de um contêiner às mensagens com destinatários que atendem aos critérios fornecidos. Uma mensagem é qualificada para exibir se pelo menos uma linha na tabela de destinatários, ou seja, um destinatário satisfizer a restrição de subobjeto. 
  
 **Observação** O uso de resultados de restrição de subobjeto é o equivalente de uma chamada de [IMAPISession:: OpenEntry](imapisession-openentry.md) em cada mensagem da tabela. Dependendo do aplicativo cliente e do número de mensagens a serem pesquisadas, isso pode afetar o desempenho. 
  
A propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) e essa propriedade são similares em uso. Várias propriedades MAPI fornecem acesso a tabelas: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabela de hierarquia  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabela de conteúdo associado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela de anexos  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Tabela de destinatários  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
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

