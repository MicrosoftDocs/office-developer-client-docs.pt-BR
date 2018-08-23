---
title: Propriedade canônica PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2b4013b311289816f778d7559ee3bcc7dc061538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574332"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Propriedade canônica PidTagDefaultPostMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de uma classe de mensagem do formulário personalizado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Identificador:  <br/> |0x36E5  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for definida em uma pasta, o valor deve conter exatamente a classe de mensagem de base (por exemplo, "IPM. Contato"para uma pasta de contatos ou"IPM. Compromisso"para uma pasta de calendário), ou começam com a classe de mensagem de base (por exemplo," IPM. Contact.MyContact").
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
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

