---
title: Propriedade canônica PidTagDisplayTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTo
api_type:
- HeaderDef
ms.assetid: 700cc03b-5d98-40ce-adb5-a11fdac8aa28
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0c7ae8951b02f099161871b17ff59ea23f8fbcc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360785"
---
# <a name="pidtagdisplayto-canonical-property"></a>Propriedade canônica PidTagDisplayTo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista dos nomes para exibição dos destinatários de mensagem principal (Para), separados por ponto-e-vírgula (;). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_TO, PR_DISPLAY_TO_A, PR_DISPLAY_TO_W  <br/> |
|Identificador:  <br/> |0x0E04  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

O armazenamento de mensagens calcula essas propriedades em objetos de mensagem usando o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) O armazenamento de mensagens também mantém essas propriedades para que ela sempre reflita o último estado salvo de uma mensagem. O valor é sincronizado no momento de cada chamada para o [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Se uma mensagem não tiver destinatários primários, o armazenamento de mensagens deverá responder a uma chamada [IMAPIProp::GetProps](imapiprop-getprops.md) com um valor de retorno de S_OK e uma cadeia de caracteres vazia para **PR_DISPLAY_TO**. 
  
Devido à possível necessidade de localização, o MAPI fornece estas diretrizes para todos os nomes de destinatários:
  
- Todos os nomes devem ser localizados. 
    
- O ponto-e-vírgula deve ser o caractere usado para separar nomes no **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) e PR_DISPLAY_TO **propriedades.** Pontos-e-vírgulas não são permitidos em nomes de destinatários em MAPI. 
    
- Os clientes devem traduzir cada ponto-e-vírgula encontrado no **PR_DISPLAY_TO** propriedades relacionadas para um caractere separador localizado antes de tornar as informações visíveis na interface do usuário. 
    
- Ao encaminhar mensagens, os clientes não precisam traduzir os caracteres separadores na linha de destinatário principal. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
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

