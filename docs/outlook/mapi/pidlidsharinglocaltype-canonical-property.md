---
title: Propriedade canônica PidLidSharingLocalType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingLocalType
api_type:
- COM
ms.assetid: 6ac438a1-d36f-424f-b4b4-d6f2d26fd350
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aa1f76a3f410294de9c7ebfb3e64bbb1cd6cc25c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394710"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a>Propriedade canônica PidLidSharingLocalType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o valor da propriedade **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) da pasta que está sendo compartilhada. Esta é uma propriedade de uma mensagem de compartilhamento.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidSharingLocalType  <br/> |
|Propriedade definida:  <br/> |PSETID_Sharing  <br/> |
|ID de longo (LID):  <br/> |0x00008A14  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser um destes procedimentos:
  
- "FALHA DE PÁGINA INVÁLIDA. Compromisso"
    
- "FALHA DE PÁGINA INVÁLIDA. Contato"
    
- "FALHA DE PÁGINA INVÁLIDA. Tarefa"
    
- "FALHA DE PÁGINA INVÁLIDA. StickyNote"
    
- "FALHA DE PÁGINA INVÁLIDA. Diário"
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Compartilha pastas de caixa de correio entre clientes.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

