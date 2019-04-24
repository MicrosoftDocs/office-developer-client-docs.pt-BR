---
title: Propriedade canônica PidLidNonSendToTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bdfbd553e130a4e463017168a76dc94fc0df827b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331364"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a>Propriedade canônica PidLidNonSendToTrackStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o valor para cada participante listado na propriedade **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidNonSendToTrackStatus  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008543  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é obrigatória somente quando a propriedade **dispidNonSendableTo** é definida. O número de valores nessa propriedade deve ser igual ao número de valores em **dispidNonSendableTo**. Cada valor PT_LONG nessa propriedade corresponde ao participante na propriedade **dispidNonSendableTo** no mesmo índice. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definição e referências de conjunto de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

