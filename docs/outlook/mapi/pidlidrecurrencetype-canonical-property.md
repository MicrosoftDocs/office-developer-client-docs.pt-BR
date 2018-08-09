---
title: Propriedade canônica PidLidRecurrenceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrenceType
api_type:
- COM
ms.assetid: 81ad2e8a-661f-4fc7-bee4-848db3285e31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9fecd67c370333064fd593634ad2a924a3005d28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768594"
---
# <a name="pidlidrecurrencetype-canonical-property"></a>Propriedade canônica PidLidRecurrenceType

  
  
**Aplica-se a**: Outlook 
  
Especifica o tipo de recorrência da série recorrente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidRecurType  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008231  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade especifica o tipo de recorrência da série recorrente usando um dos valores listados abaixo.
  
|**Status**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|rectypeNone  <br/> |0  <br/> |Compromisso de uma única instância.  <br/> |
|rectypeDaily  <br/> |1  <br/> |Um padrão de recorrência diária.  <br/> |
|rectypeWeekly  <br/> |2  <br/> |Um padrão de recorrência semanal.  <br/> |
|rectypeMonthly  <br/> |3  <br/> |Um padrão de recorrência mensal.  <br/> |
|rectypeYearly  <br/> |4  <br/> |Um padrão de recorrência anual.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

