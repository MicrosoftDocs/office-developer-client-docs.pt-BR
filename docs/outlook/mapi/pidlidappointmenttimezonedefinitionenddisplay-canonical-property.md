---
title: Propriedade canônica PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: facbcb9eed18db304cac334be845c0b3869ba508
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574801"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Propriedade canônica PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição para o fuso horário que é usado quando a hora de término de uma única instância compromisso ou solicitação de reunião é selecionada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x0000825F  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Office Outlook 2003 ou anterior e soluções que são baseados em Collaboration Data Objects (CDO) 1.2.1 e que não têm executar a ferramenta de atualização de calendário do Outlook ou o Microsoft Exchange Server, para armazenar a hora de início e hora de término de ocorrência única compromissos e solicitações de reunião no tempo Universal Coordenado (UTC). Esses clientes não armazene qualquer informação para o fuso horário em que a solicitação de reunião ou compromisso é criada.
  
Versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e soluções com base no CDO 1.2.1 que executaram o calendário do Outlook ou o Exchange Server atualizar de uso de ferramenta **dispidApptTZDefEndDisplay** para armazenar o fuso horário para a hora de término. **dispidApptTZDefEndDisplay** mostra o compromisso ou reunião no fuso horário original que ele estava agendado e determina se a hora de término deve ser ajustada se alterar as regras do fuso horário. Se essa propriedade estiver ausente, o fuso horário especificado pela propriedade **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) é usado. Se **dispidApptTZDefStartDisplay** estiver ausente ou inválido, o fuso horário local atual é assumido. **dispidApptTZDefEndDisplay** é usado somente para exibição e não é usado na expansão de recorrência. 
  
Um analisador deve tomar cuidado quando ele lê um stream obtido de **dispidApptTZDefEndDisplay**ou quando ele persiste **TZDEFINITION** a um fluxo de compromisso em uma propriedade binária como **dispidApptTZDefEndDisplay**. Para obter mais informações, consulte [About TZDEFINITION mantendo a um fluxo de confirmar uma propriedade binária](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** Especifica as informações de fuso horário para a propriedade **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). O formato, restrições e computação do **dispidApptTZDefEndDisplay** são os mesmos conforme especificado na propriedade **dispidApptTZDefStartDisplay** . 
  
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

