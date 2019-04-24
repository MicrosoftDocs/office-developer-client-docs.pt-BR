---
title: Propriedade canônica PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355456"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a>Propriedade canônica PidTagOriginalDisplayName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de exibição original de uma entrada copiada de um catálogo de endereços para um catálogo de endereços pessoal ou outro catálogo de endereços gravável.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W  <br/> |
|Identificador:  <br/> |0x3A13  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades contêm informações sobre a fonte original de uma entrada copiada.
  
Para um relatório não lido, essas propriedades contêm uma cópia do nome de exibição do destinatário da mensagem original para o qual o relatório é gerado. Quando o destinatário original faz parte de uma lista de distribuição, o nome de exibição da lista de distribuição é preservado para o relatório.
  
Um aplicativo cliente pode usar essas propriedades para impedir a alteração ou "falsificação" de entradas, dando uma cópia não modificada do nome de exibição a ser comparado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

