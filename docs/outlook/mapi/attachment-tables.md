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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427440"
---
# <a name="attachment-tables"></a>Tabelas de anexos

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de anexos contém informações sobre todos os objetos anexos que estão associados a uma mensagem enviada ou uma mensagem em composição. 
  
Somente anexos que foram salvos por meio de uma chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem são incluídos na tabela. As tabelas de anexos são implementadas por provedores de armazenamento de mensagens e usadas por aplicativos cliente e provedores de transporte. 
  
Uma tabela de anexos pode ser acessada chamando um dos seguintes:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), solicitando a **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) propriedade.
    
As tabelas de anexos são dinâmicas.
  
Os provedores de armazenamento de mensagens não são obrigados a dar suporte à classificação em suas tabelas de anexos. Se a classificação não for suportada, a tabela deverá ser apresentada em ordem pela posição de renderização — a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Os provedores de armazenamento de mensagens também não são obrigados a dar suporte a restrições em suas tabelas de anexos. Provedores que não suportam restrições retornam MAPI_E_NO_SUPPORT de suas implementações de [IMAPITable::Restrict](imapitable-restrict.md) e [IMAPITable::FindRow](imapitable-findrow.md).
  
As tabelas de anexos podem ser pequenas; há apenas quatro colunas no conjunto de colunas necessário:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** não étransmitível e contém um valor para identificar exclusivamente um anexo em uma mensagem. Essa propriedade geralmente é usada como um índice nas linhas da tabela. **PR_ATTACH_NUM** tempo de vida curto; só é válida enquanto a mensagem que contém o anexo está aberta. Seu valor permanecerá constante enquanto a tabela de anexos for aberta. 
  
 **PR_INSTANCE_KEY** é necessário em quase todas as tabelas. Ele é usado para identificar exclusivamente uma linha específica. 
  
 **PR_RECORD_KEY** é comumente usado para identificar exclusivamente um objeto para fins de comparação. Ao **PR_ATTACH_NUM**, **PR_RECORD_KEY** tem o mesmo escopo que um identificador de entrada de longo prazo; ele permanece disponível e válido mesmo depois que a mensagem é fechada e reaberta. Para obter mais informações sobre o uso de chaves de registro em MAPI, consulte [Registro MAPI e chaves de pesquisa.](mapi-record-and-search-keys.md)
  
 **PR_RENDERING_POSITION** indica como um anexo deve ser exibido em uma mensagem de rich text. Ele pode ser definido como um deslocamento em caracteres, com o primeiro caractere do conteúdo da mensagem como armazenado na propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sendo deslocada 0 ou como -1 (0xFFFFFFFF), indicando que o anexo não deve ser renderizado dentro do texto da mensagem. Não definir **PR_RENDERING_POSITION** também é uma opção. 
  
Quando uma tabela de anexos é ordenada pela posição de renderização, o provedor de armazenamento de mensagens a trata como um valor assinado (PT_LONG). Portanto, anexos com posições de renderização de -1 são organizados antes de anexos com posições de renderização que refletem deslocamentos válidos. 
  
Para obter mais informações sobre como renderizar um anexo em uma mensagem de texto sem texto, consulte [Renderização de um anexo em texto sem texto simples.](rendering-an-attachment-in-plain-text.md) 
  
Para obter informações sobre como renderizar um anexo em texto formatado, como Rich Text Format (RTF), consulte Renderização de um [anexo em texto RTF.](rendering-an-attachment-in-rtf-text.md)
  
Alguns dos provedores de armazenamento de mensagens de propriedades normalmente incluem em uma tabela de anexos porque eles são fáceis de calcular ou recuperar são:
  
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

