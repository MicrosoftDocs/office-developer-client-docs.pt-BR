---
title: Propriedade canônica PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f30a5848e07de03e61d3a63188aa7b608504ff24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573730"
---
# <a name="pidtagsensitivity-canonical-property"></a>Propriedade canônica PidTagSensitivity

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que indica a opinião do remetente da mensagem da sensibilidade de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SENSITIVITY  <br/> |
|Identificador:  <br/> |0x0036  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os objetos de mensagem exponham essa propriedade.
  
Essa propriedade pode ter exatamente um dos seguintes valores:
  
SENSITIVITY_NONE 
  
> A mensagem não tem nenhuma sensibilidade especial.
    
SENSITIVITY_PERSONAL 
  
> A mensagem é pessoal.
    
SENSITIVITY_PRIVATE 
  
> A mensagem é particular.
    
SENSITIVITY_COMPANY_CONFIDENTIAL 
  
> A mensagem é designada confidencial da empresa.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
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

