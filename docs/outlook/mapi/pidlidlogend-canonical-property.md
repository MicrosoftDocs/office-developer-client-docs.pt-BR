---
title: Propriedade canônica PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336922"
---
# <a name="pidlidlogend-canonical-property"></a>Propriedade canônica PidLidLogEnd

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa a data e a hora de término da mensagem de diário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidLogEnd  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Log  <br/> |
|Long ID (LID):  <br/> |0x00008708  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Diário  <br/> |
   
## <a name="remarks"></a>Comentários

A hora em que a atividade terminou em UTC (Tempo Universal Coordenado), que deve ser igual à **propriedade dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) e maior ou igual a **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) propriedade.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para diários.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

