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
ms.openlocfilehash: 74669d102462e1a825568615d1d30346e99e90a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360813"
---
# <a name="pidtagdisplaybcc-canonical-property"></a>Propriedade canônica PidTagDisplayBcc

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista ASCII dos nomes de exibição de destinatários de mensagens com cópia oculta (Cco), separados por ponto e vírgula (;).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_BCC, PR_DISPLAY_BCC_A, PR_DISPLAY_BCC_W  <br/> |
|Identificador:  <br/> |0x0E02  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

O repositório de mensagens computa essas propriedades em objetos de mensagem usando o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . O repositório de mensagens também mantém essas propriedades para que ela sempre reflita o último estado salvo de uma mensagem. O valor é sincronizado no momento de cada chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
Se uma mensagem não tiver destinatários de cópia carbono oculta, o repositório de mensagens deverá responder a uma chamada a [IMAPIProp::](imapiprop-getprops.md) GetProps com um valor de retorno de S_OK e uma cadeia de caracteres vazia para o **PR_DISPLAY_BCC**. 
  
Devido à possível necessidade de localização, a MAPI fornece essas diretrizes para todos os nomes de destinatários:
  
- Todos os nomes devem ser capazes de ser localizados. 
    
- O ponto e vírgula deve ser o caractere usado para separar nomes nas propriedades **PR_DISPLAY_BCC**, **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)). Pontos-e-vírgulas não são permitidos em nomes de destinatários no MAPI. 
    
- Os clientes devem traduzir cada ponto-e-vírgula encontrado nesta propriedade para um caractere separador localizado antes de tornar as informações de propriedade visíveis na interface do usuário. 
    
- Ao encaminhar mensagens, os clientes não precisam traduzir os caracteres separadores na linha de destinatários de cópia carbono oculta. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Descreve o formato das mensagens usadas para enviar informações relacionadas às pastas de compartilhamento no cliente.
    
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

