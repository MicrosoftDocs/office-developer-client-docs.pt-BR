---
title: Propriedade canônica PidTagDisplayCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayCc
api_type:
- HeaderDef
ms.assetid: 00377e78-a208-4942-a7a6-893b2a71ab0b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6257557a8848c1abbaf8ceb15f719c50e4fec8c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769193"
---
# <a name="pidtagdisplaycc-canonical-property"></a>Propriedade canônica PidTagDisplayCc

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista de ASCII dos nomes de exibição de qualquer destinatários de cópia carbono (CC) da mensagem, separados por ponto e vírgula (;). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_CC, PR_DISPLAY_CC_A, PR_DISPLAY_CC_W  <br/> |
|Identificador:  <br/> |0x0E03  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Comentários

O armazenamento de mensagens computa essas propriedades em objetos de mensagem usando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflete o último estado salvo de uma mensagem. O valor é sincronizado no momento de cada chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md). 
  
Se uma mensagem não tiver cópia carbono destinatários, o armazenamento de mensagens deve responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno de S_OK e uma sequência vazia para essas propriedades. 
  
Devido a necessidade de possível de localização, MAPI fornece estas diretrizes para todos os nomes de destinatário:
  
- Todos os nomes devem ser capazes de ser localizadas. 
    
- O ponto e vírgula deve ser o caractere usado para separar nomes na **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC**e propriedades de **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Ponto e vírgula não é permitida em nomes de destinatários em MAPI. 
    
- Os clientes devem traduzir cada ponto e vírgula encontrada nesta propriedade como um caractere separador localizado antes de fazer as informações de propriedade visível na interface do usuário. 
    
- Quando o encaminhamento de mensagens, os clientes não precisará traduzir os caracteres separadores na linha de destinatário de cópia carbono. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
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

