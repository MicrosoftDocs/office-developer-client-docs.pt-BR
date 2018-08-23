---
title: Propriedade canônica PidTagDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayBcc
api_type:
- HeaderDef
ms.assetid: ab5bcd67-d54e-46e9-b94e-a652aac3e81c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cd37d72d6a214f91e371b7126c90e3fda25cde2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578896"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Propriedade canônica PidTagDisplayBcc

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de ASCII dos nomes de exibição de qualquer destinatários de cópia oculta (Cco) da mensagem, separados por ponto e vírgula (;).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Identificador:  <br/> |0x0E02  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Message  <br/> |
   
## <a name="remarks"></a>Comentários

O armazenamento de mensagens computa essas propriedades em objetos de mensagem usando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflete o último estado salvo de uma mensagem. O valor é sincronizado no momento de cada chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Se uma mensagem não tiver nenhum destinatários de cópia oculta, o armazenamento de mensagens deve responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno de S_OK e uma sequência vazia para **PR_DISPLAY_BCC**. 
  
Devido a necessidade de possível de localização, MAPI fornece estas diretrizes para todos os nomes de destinatário:
  
- Todos os nomes devem ser capazes de ser localizadas. 
    
- O ponto e vírgula deve ser o caractere usado para separar nomes na **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e propriedades de **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Ponto e vírgula não é permitida em nomes de destinatários em MAPI. 
    
- Os clientes devem traduzir cada ponto e vírgula encontrada nesta propriedade como um caractere separador localizado antes de fazer as informações de propriedade visível na interface do usuário. 
    
- Quando o encaminhamento de mensagens, os clientes não precisará traduzir os caracteres separadores na linha de destinatários de cópia oculta. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Descreve o formato das mensagens usado para enviar informações relacionadas ao compartilhamento de pastas no cliente.
    
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

