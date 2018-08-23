---
title: Propriedade canônica PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da38c8f04c0ffe6b4b26551cb23e84275900fcb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563055"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propriedade canônica PidLidAppointmentRecur

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica as datas e horas quando uma série recorrente ocorre usando um dos padrões de recorrência e intervalos que são especificados nas [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptRecur  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008216  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica as datas e horas quando uma série recorrente ocorre usando um dos padrões de recorrência e intervalos detalhado no [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). O valor dessa propriedade também contém informações sobre exceções excluídas e modificadas; informações sobre como datas, assunto, local e várias outras propriedades de exceções. Os dados binários nessa propriedade recorrentes dos itens do calendário são armazenados como a estrutura de **AppointmentRecurrencePattern** . Essa propriedade não deve existir nos itens de calendário de única instância. 
  
Há algumas limitações à recorrências:
  
- Várias instâncias não devem iniciar no mesmo dia.
    
- Ocorrências não devem ser sobrepostos. Especificamente, uma exceção que modifica a data de início de uma instância da série recorrente deve ocorrer em uma data que é após o fim da instância anterior e o início da próxima instância da série recorrente. O mesmo é true se as instâncias anteriores ou próximas da série recorrente são exceções.
    
O agendamento de uma série recorrente é determinado pelo seu padrão de recorrência e o intervalo.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

