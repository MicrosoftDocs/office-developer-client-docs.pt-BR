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
ms.openlocfilehash: f6d0c7c6f6f34330c143781fbac976392ee1c9a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768318"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Propriedade canônica PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**Aplica-se a**: Outlook 
  
Contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição para o fuso horário que é usado quando a hora de início de uma única instância compromisso ou solicitação de reunião é selecionada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x0000825E  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Office Outlook 2003 ou anterior e soluções que são baseados em Collaboration Data Objects (CDO) 1.2.1 e que não têm executar a ferramenta de atualização de calendário do Outlook ou o Microsoft Exchange Server, para armazenar a hora de início e hora de término de ocorrência única compromissos e solicitações de reunião no tempo Universal Coordenado (UTC). Esses clientes não armazene qualquer informação para o fuso horário no qual a solicitação de reunião ou compromisso for criada.
  
Versões do Outlook desde o Microsoft Office Outlook 2007 e soluções com base em CDO 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou o Exchange Server usam essa propriedade para armazenar o fuso horário para a hora de início. A propriedade **dispidApptTZDefStartDisplay** mostra o compromisso ou reunião no fuso horário original que foi agendada. Determina se a hora de início deve ser ajustada se alterar as regras do fuso horário. Se essa propriedade estiver ausente, o fuso horário local atual é assumido. Essa propriedade é usada apenas para exibição e não é usada na expansão de recorrência. 
  
Um analisador deve tomar cuidado quando ele lê um stream obtido essa propriedade, ou quando ele persiste **TZDEFINITION** a um fluxo de compromisso em uma propriedade binária como **dispidApptTZDefStartDisplay**. Para obter mais informações, consulte [About TZDEFINITION mantendo a um fluxo de confirmar uma propriedade binária](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Esta propriedade especifica as informações de fuso horário para a propriedade **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). O valor de **dispidApptTZDefStartDisplay** é usado para converter a data de início e a hora de UTC para o fuso horário local para fins de exibição. Para cada **TZRULE** especificado por esta propriedade, o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG não deve ser definido. Por exemplo, se o **TZRULE** for a regra efetiva, o valor do campo, **TZRULE** deve ser "0x0002"; Caso contrário, ele deve ser "0x0000". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades..
    
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

