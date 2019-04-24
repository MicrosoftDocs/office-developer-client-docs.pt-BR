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
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357901"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Propriedade canônica PidTagDefaultPostMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de uma classe de mensagem de formulário personalizada.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Identificador:  <br/> |0x36E5  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for definida em uma pasta, o valor deverá conter exatamente a classe de mensagem base (por exemplo, "IPM. Contact "para uma pasta de contatos ou" IPM. Compromisso "para uma pasta de calendário) ou comece com a classe de mensagem base (por exemplo," IPM. Contact. myContact ").
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
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

