---
title: Propriedade canônica PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315432"
---
# <a name="pidlidisrecurring-canonical-property"></a>Propriedade canônica PidLidIsRecurring

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o objeto está associado a uma série recorrente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |LID_IS_RECURRING  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000005  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Comentários

Um valor TRUE indica que o objeto representa uma série recorrente ou uma exceção (incluindo uma instância órfã). Um valor FALSE ou a ausência dessa propriedade indica que o objeto representa uma única instância. Observe a diferença entre essa propriedade e a propriedade **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
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

