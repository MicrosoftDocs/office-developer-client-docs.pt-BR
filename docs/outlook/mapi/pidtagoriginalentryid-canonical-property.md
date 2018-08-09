---
title: Propriedade canônica PidTagOriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d60531b087d00ca63a060a4dbfac559ba3b01788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769567"
---
# <a name="pidtagoriginalentryid-canonical-property"></a>Propriedade canônica PidTagOriginalEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém o identificador de entrada original para uma entrada copiada de um catálogo de endereços a um catálogo de endereços pessoais ou outro catálogo de endereços gravável.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_ENTRYID  <br/> |
|Identificador:  <br/> |0x3A12  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades que contêm informações sobre a fonte original de uma entrada copiada.
  
Para um relatório nonread, essa propriedade contém uma cópia do identificador de entrada do remetente da mensagem original para o qual o relatório é gerado. Quando o destinatário original fizer parte de uma lista de distribuição, o identificador de entrada da lista de distribuição é preservado para o relatório.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.
    
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

