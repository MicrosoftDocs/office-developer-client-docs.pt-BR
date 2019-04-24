---
title: Tabelas de anexos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318134"
---
# <a name="attachment-tables"></a>Tabelas de anexos

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de anexo contém informações sobre todos os objetos Attachment que estão associados a uma mensagem enviada ou uma mensagem em composição. 
  
Somente anexos que foram salvos por meio de uma chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem são incluídos na tabela. As tabelas de anexo são implementadas por provedores de repositórios de mensagens e usadas por aplicativos cliente e provedores de transporte. 
  
Uma tabela de anexo pode ser acessada chamando-se um dos seguintes:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md), solicitando a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
As tabelas de anexo são dinâmicas.
  
Os provedores de repositórios de mensagens não são necessários para dar suporte à classificação em suas tabelas de anexo. Se a classificação não for suportada, a tabela deve ser apresentada em ordem por processamento de posição, a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Os provedores de repositórios de mensagens também não são necessários para dar suporte a restrições em suas tabelas de anexo. Provedores que não dão suporte a restrições retornam MAPI_E_NO_SUPPORT de suas implementações de imApitable [:: Restrict](imapitable-restrict.md) e IMAPITable [:: FindRow](imapitable-findrow.md).
  
As tabelas de anexo podem ser pequenas; Há apenas quatro colunas no conjunto de colunas obrigatório:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** é nontransmittable e contém um valor para identificar exclusivamente um anexo em uma mensagem. Essa propriedade é geralmente usada como um índice nas linhas da tabela. O **PR_ATTACH_NUM** tem uma curta duração; Ela só será válida enquanto a mensagem que contém o anexo estiver aberta. O valor é garantido para permanecer constante, desde que a tabela de anexos esteja aberta. 
  
 **PR_INSTANCE_KEY** é necessário em quase todas as tabelas. É usado para identificar exclusivamente uma linha específica. 
  
 **PR_RECORD_KEY** é comumente usado para identificar exclusivamente um objeto para fins de comparação. Ao contrário de **PR_ATTACH_NUM**, **PR_RECORD_KEY** tem o mesmo escopo de um identificador de entrada de longo prazo; Ele permanece disponível e é válido mesmo depois que a mensagem é fechada e reaberta. Para obter mais informações sobre o uso de chaves de registro em MAPI, consulte [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** indica como um anexo deve ser exibido em uma mensagem de Rich Text. Ele pode ser definido como um deslocamento em caracteres, com o primeiro caractere do conteúdo da mensagem, conforme armazenado na propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) deslocada 0 ou como-1 (0xFFFFFFFF), indicando que o anexo não deve ser renderizado dentro da mensagem texto. Não definir **PR_RENDERING_POSITION** também é uma opção. 
  
Quando uma tabela de anexo é classificada pela posição de renderização, o provedor do repositório de mensagens a trata como um valor assinado (PT_LONG). Portanto, os anexos com posições de renderização de-1 são classificados antes dos anexos com posições de renderização que refletem deslocamentos válidos. 
  
Para obter mais informações sobre como renderizar um anexo em uma mensagem de texto sem formatação, consulte [renderizar um anexo em texto sem formatação](rendering-an-attachment-in-plain-text.md). 
  
Para obter informações sobre como renderizar um anexo em texto formatado, como Rich Text Format (RTF), confira [renderizar um anexo no texto RTF](rendering-an-attachment-in-rtf-text.md).
  
Algumas das propriedades dos provedores de repositório de mensagens normalmente incluem em uma tabela de anexos porque elas são fáceis de calcular ou recuperar são:
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

