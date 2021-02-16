---
title: Propriedade canônica PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345350"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Propriedade canônica PidLidAppointmentTimeZoneDefinitionRecur

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um fluxo que é mapeado para o formato persistente de uma estrutura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que armazena a descrição para o fuso horário que é usado quando uma solicitação de reunião ou compromisso recorrente é criada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefRecur  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008260  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

As versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e as soluções baseadas no CDO (Collaboration Data Objects) 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam as propriedades **dispidApptTZDefRecur** e **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar se a reunião recorrente deve ser ajustada se as regras do fuso horário mudarem. Essas propriedades devem ser sincronizadas, pois os clientes mais antigos ainda podem manipular a **propriedade dispidTimeZoneStruct.** Para detectar se as duas propriedades estão sincronizadas, o membro **wFlags** da regra que corresponde **a dispidTimeZoneStruct** deve ter o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG definido. Se esse sinalizador não estiver definido ou estiver definido e a regra na propriedade **dispidTimeZoneStruct** não corresponder à regra marcada, a propriedade **dispidApptTZDefRecur** deverá ser descartada e **dispidTimeZoneStruct** deverá ser usada. 
  
Quando você escreve as propriedades **dispidApptTZDefRecur** e **dispidTimeZoneStruct** em uma nova reunião recorrente ou, quando você faz uma escolha arbitrária para usar a propriedade **dispidTimeZoneStruct,** a definição atual para o fuso horário (de acordo com o Registro do Windows) deve ser usada. 
  
Um analisador deve ter cuidado ao ler um fluxo obtido de **dispidApptTZDefRecur** ou quando persistir **TZDEFINITION** para um fluxo para compromisso com uma propriedade binária, como **dispidApptTZDefRecur**. For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** especifica informações de fuso horário que descrevem como converter a data e a hora da reunião em uma série recorrente de e para UTC (Tempo Universal Coordenado). Se essa propriedade estiver definida, mas tiver dados inconsistentes com os dados representados por **dispidTimeZoneStruct**, o cliente deverá usar **dispidTimeZoneStruct** em vez de **dispidApptTZDefRecur**. Se **dispidApptTZDefRecur** não estiver definida, a propriedade **PidLidTimeZoneStruct** será usada. Os campos neste BLOB são codificados em ordem de byte little-endian. 
  
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

