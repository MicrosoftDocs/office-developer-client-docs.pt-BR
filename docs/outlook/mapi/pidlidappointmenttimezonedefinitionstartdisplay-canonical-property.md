---
title: Propriedade canônica PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345014"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propriedade canônica PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um Stream que mapeia para o formato persistente de uma estrutura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição do fuso horário usado quando o horário de início de um compromisso ou solicitação de reunião de instância única é selecionado. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000825E  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Office Outlook 2003 ou anterior, e soluções baseadas em Collaboration Data Objects (CDO) 1.2.1 e que não executaram a ferramenta de atualização de calendário para Outlook ou Microsoft Exchange Server, armazenam a hora de início e a hora de término de uma única instância compromissos e solicitações de reunião no tempo universal coordenado (UTC). Esses clientes não armazenam informações sobre o fuso horário em que o compromisso ou solicitação de reunião foi criado.
  
Versões do Outlook desde o Microsoft Office Outlook 2007 e soluções baseadas no CDO 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam essa propriedade para armazenar o fuso horário para a hora de início. A propriedade **dispidApptTZDefStartDisplay** mostra o compromisso ou a reunião no fuso horário original em que foi agendado. Ele determina se a hora de início deve ser ajustada se as regras do fuso horário forem alteradas. Se essa propriedade estiver ausente, será considerado o fuso horário local atual. Essa propriedade é usada apenas para fins de exibição e não é usada em expansão de recorrência. 
  
Um analisador deve ser cuidadoso quando lê um fluxo obtido dessa propriedade ou quando ele persiste **TZDEFINITION** para um Stream de compromisso para uma propriedade binária, como **dispidApptTZDefStartDisplay**. Para obter mais informações, consulte [sobre a persistência de TZDEFINITION em um Stream para confirmar uma propriedade binária](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Esta propriedade especifica informações de fuso horário para a propriedade **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). O valor de **dispidApptTZDefStartDisplay** é usado para converter a data de início e a hora do UTC para o fuso horário local para fins de exibição. Para cada **TZRULE** especificado por essa propriedade, o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG não deve ser definido. Por exemplo, se **TZRULE** for a regra efetiva, o valor do campo **TZRULE** deverá ser "0x0002"; caso contrário, ele deve ser "0x0000". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas..
    
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

