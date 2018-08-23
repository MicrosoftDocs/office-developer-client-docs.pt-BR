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
ms.openlocfilehash: 7348d0395952036ee6b356b013072324b64e4b98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570818"
---
# <a name="pidtagstorestate-canonical-property"></a>Propriedade canônica PidTagStoreState

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um sinalizador que descreve o estado do armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_STORE_STATE  <br/> |
|Identificador:  <br/> |0x340E  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é dinâmica e pode ser alterado com base nas ações do usuário, ao contrário da propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
O seguinte valor pode ser definido:
  
STORE_HAS_SEARCHES 
  
> O usuário criou um ou mais pesquisas ativas no repositório.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica as operações permitidas para os objetos do repositório de mensagem principal.
    
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

