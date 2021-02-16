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
  
Contém um fluxo que é mapeado para o formato persistente de uma estrutura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que armazena a descrição para o fuso horário que é usado quando a hora de início de um compromisso de instância única ou solicitação de reunião é selecionada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000825E  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Office Outlook 2003 ou anterior, e soluções baseadas no CDO (Collaboration Data Objects) 1.2.1 e que não executaram a ferramenta de atualização de calendário para o Outlook ou o Microsoft Exchange Server, armazene a hora de início e a hora de término de compromissos de instância única e solicitações de reunião em TEMPO Universal Coordenado (UTC). Esses clientes não armazenam informações para o fuso horário no qual a solicitação de compromisso ou reunião é criada.
  
As versões do Outlook desde o Microsoft Office Outlook 2007 e as soluções baseadas no CDO 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam essa propriedade para armazenar o fuso horário para a hora de início. A **propriedade dispidApptTZDefStartDisplay** mostra o compromisso ou a reunião no fuso horário original que foi agendado. Ele determina se a hora de início deve ser ajustada se as regras do fuso horário mudarem. Se essa propriedade estiver ausente, o fuso horário local atual será assumido. Essa propriedade é usada apenas para fins de exibição e não é usada na expansão de recorrência. 
  
Um analisador deve ter cuidado ao ler um fluxo obtido dessa propriedade ou quando persistir **TZDEFINITION** em um fluxo para compromisso com uma propriedade binária, como **dispidApptTZDefStartDisplay**. For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Esta propriedade especifica informações de fuso horário para **a propriedade dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). O valor de **dispidApptTZDefStartDisplay** é usado para converter a data e a hora de início de UTC no fuso horário local para fins de exibição. Para cada **TZRULE** especificado por essa propriedade, o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG não deve ser definido. Por exemplo, se **o TZRULE** for a regra efetiva, o valor do campo, **TZRULE** deverá ser "0x0002"; caso contrário, ele deve ser "0x0000". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

