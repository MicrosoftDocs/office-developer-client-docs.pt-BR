---
title: Tabelas de anexo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2fd79cfe18e7d39f26563c87b8fb15553bf32ddf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766193"
---
# <a name="attachment-tables"></a>Tabelas de anexo

**Aplica-se a**: Outlook 
  
Uma tabela de anexo contém informações sobre todos os objetos attachment que estão associados uma mensagem enviada ou uma mensagem de composição. 
  
Somente os anexos que foram salvos por meio de uma chamada ao método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem são incluídos na tabela. Tabelas do anexo são implementadas pelos provedores de repositório de mensagem e usadas por aplicativos cliente e provedores de transporte. 
  
Uma tabela de anexos pode ser acessada chamando um destes procedimentos:
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md), solicitando a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).
    
Tabelas do anexo são dinâmicas.
  
Provedores de armazenamento de mensagens não são necessárias para dar suporte a classificação em suas tabelas de anexo. Se não há suporte para a classificação, a tabela deve ser apresentada na ordem por posição de renderização — a propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
  
Provedores de armazenamento de mensagem também não são necessários para dar suporte a restrições em suas tabelas de anexo. Provedores que não oferecem suporte a restrições retornam MAPI_E_NO_SUPPORT de suas implementações de [IMAPITable:: Restrict](imapitable-restrict.md) e [IMAPITable:: FindRow](imapitable-findrow.md).
  
Tabelas de anexo podem ser pequenas; Há apenas quatro colunas no conjunto de coluna necessária:
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** é nontransmittable e contém um valor para identificar exclusivamente um anexo em uma mensagem. Essa propriedade é frequentemente usada como um índice para as linhas da tabela. **PR_ATTACH_NUM** tem uma vida útil curta; ele só será válido enquanto a mensagem contendo o anexo está aberta. Seu valor é garantido permanecem constantes desde que a tabela de anexo está aberta. 
  
 **PR_INSTANCE_KEY** é necessário em quase todas as tabelas. Ele é usado para identificar exclusivamente uma linha específica. 
  
 **PR_RECORD_KEY** geralmente é usada para identificar exclusivamente um objeto para fins de comparação. Diferentemente **PR_ATTACH_NUM**, **PR_RECORD_KEY** tem o mesmo escopo como um identificador de entrada de longo prazo; ele permanece válido e disponíveis, mesmo depois que a mensagem é fechada e reabri-lo. Para obter mais informações sobre o uso das chaves de registro no MAPI, consulte [o registro de MAPI e chaves de pesquisa](mapi-record-and-search-keys.md).
  
 **PR_RENDERING_POSITION** indica como um anexo deve ser exibido em uma mensagem de rich text. Ela pode ser definida para um deslocamento em caracteres, com o primeiro caractere do conteúdo da mensagem, conforme armazenado na propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sendo deslocamento 0, ou -1 (0xFFFFFFFF), indicando que o anexo não deve ser renderizado dentro da mensagem texto é que mudaram. Não definindo **PR_RENDERING_POSITION** também é uma opção. 
  
Quando uma tabela de anexo é classificada por posição de renderização, o provedor de armazenamento de mensagens a tratará como um valor assinado (PT_LONG). Portanto, os anexos com as posições de renderização de -1 são classificados antes dos anexos com as posições de renderização que reflitam deslocamentos válidos. 
  
Para obter mais informações sobre o processamento de um anexo em uma mensagem de texto sem formatação, consulte a [renderização de um anexo em texto sem formatação](rendering-an-attachment-in-plain-text.md). 
  
Para obter informações sobre o processamento de um anexo em texto formatado como formato Rich Text (RTF), consulte a [renderização de um anexo em texto RTF](rendering-an-attachment-in-rtf-text.md).
  
Algumas das propriedades de provedores de armazenamento de mensagem geralmente incluem em uma tabela de anexos, porque eles são fáceis de calcular ou recuperar são:
  
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

