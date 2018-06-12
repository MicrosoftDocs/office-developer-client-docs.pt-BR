---
title: Propriedade canônico de PidTagMessageRecipients
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 980b1b81a0afbfe05fee915ddd730aad31811132
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769484"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Propriedade canônico de PidTagMessageRecipients

  
  
**Aplica-se a**: Outlook 
  
Contém uma tabela das restrições que podem ser aplicadas a uma tabela de conteúdo para localizar todas as mensagens que contêm o destinatários subobjetos que atendam as restrições. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_RECIPIENTS  <br/> |
|Identificador:  <br/> |0x0E12  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo **PT_OBJECT**, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) . Seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** . Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas opcionalmente relatá-la ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) . 
  
Essa propriedade pode ser usada para restrição subobjeto especificando-o na estrutura [SSubRestriction](ssubrestriction.md) . Isso permite que um cliente limitar o modo de exibição de um contêiner para mensagens com destinatários da reunião determinado critério. Uma mensagem qualifica para exibição se pelo menos uma linha em sua tabela de destinatário, ou seja, um destinatário atenda a restrição subobjeto. 
  
 **Observação** Usando os resultados da restrição subobjeto é o equivalente a um [IMAPISession::OpenEntry](imapisession-openentry.md) chama em todas as mensagens na tabela. Dependendo do aplicativo cliente e o número de mensagens a ser pesquisado, ele pode afetar o desempenho. 
  
A propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) e essa propriedade são semelhantes em uso. Várias propriedades MAPI fornecem acesso às tabelas: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Tabela de conteúdo  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Tabela de hierarquia  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabela de conteúdo associado  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Tabela de anexos  <br/> |
|PR_MESSAGE_RECIPIENTS  <br/> |Tabela de destinatários  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.
    
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

