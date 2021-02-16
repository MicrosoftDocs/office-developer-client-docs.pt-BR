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
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331777"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Propriedade canônica PidLidAppointmentRecur

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica as datas e horas em que uma série recorrente ocorre usando um dos padrões e intervalos de recorrência especificados em [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptRecur  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008216  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica as datas e horas em que uma série recorrente ocorre usando um dos padrões e intervalos de recorrência detalhados [em [MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). O valor dessa propriedade também contém informações sobre exceções modificadas e excluídas; informações como datas, assunto, local e várias outras propriedades de exceções. Os dados binários nesta propriedade para itens de calendário recorrentes são armazenados como a **estrutura AppointmentRecurrencePattern.** Essa propriedade não deve existir em itens de calendário de instância única. 
  
Existem algumas limitações para recorrências:
  
- Várias instâncias não devem iniciar no mesmo dia.
    
- As ocorrências não devem se sobrepor. Especificamente, uma exceção que modifica a data de início de uma instância na série recorrente deve ocorrer em uma data que esteja após o final da instância anterior e o início da próxima instância na série recorrente. O mesmo é verdadeiro se as instâncias anteriores ou próximas da série recorrente são exceções.
    
O cronograma de uma série recorrente é determinado por seu padrão e intervalo de recorrência.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

