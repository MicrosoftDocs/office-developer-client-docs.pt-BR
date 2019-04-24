---
title: Propriedade canônica PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345756"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Propriedade canônica PidLidResponseStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o status de resposta de um participante.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidResponseStatus  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008218  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Comentários

O status da resposta deve ser um dos valores na tabela abaixo.
  
|**Status da resposta**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Nenhuma resposta é necessária para este objeto. Este é o caso de objetos de compromisso e objetos de resposta de reunião.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Esta reunião pertence ao organizador.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Esse valor na reunião do participante indica que o participante aceitou provisoriamente a solicitação de reunião.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Esse valor na reunião do participante t indica que o participante aceitou a solicitação de reunião.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Esse valor na reunião do participante indica que o participante recusou a solicitação de reunião.  <br/> |
|respNotResponded  <br/> |0x00000005  <br/> |Esse valor na reunião do participante indica que o participante ainda não respondeu. Esse valor está na solicitação de reunião, atualização de reunião e cancelamento da reunião.  <br/> |
   
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

