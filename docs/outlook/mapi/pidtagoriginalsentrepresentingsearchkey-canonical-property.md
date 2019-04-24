---
title: Propriedade canônica PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340974"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a>Propriedade canônica PidTagOriginalSentRepresentingSearchKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a chave de pesquisa do usuário de mensagens em cujo nome a mensagem original foi enviada.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x005F  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades de endereço do remetente original representado de uma mensagem. Ele é usado em um thread de conversa.
  
Um aplicativo cliente enviando uma mensagem em nome de outro cliente deve definir essa propriedade como o valor da propriedade **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) no primeiro envio da mensagem. Uma vez definido, ele nunca deve ser alterado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.
    
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

