---
title: Propriedade canônica PidTagStoreState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341150"
---
# <a name="pidtagstorestate-canonical-property"></a>Propriedade canônica PidTagStoreState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um sinalizador que descreve o estado do repositório de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_STATE  <br/> |
|Identificador:  <br/> |0x340E  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Repositório de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é dinâmica e pode ser alterada com base em ações do usuário, diferente da propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
O seguinte valor pode ser definido:
  
STORE_HAS_SEARCHES 
  
> O usuário criou uma ou mais pesquisas ativas no repositório.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica operações permitidas para os principais objetos do repositório de mensagens.
    
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

