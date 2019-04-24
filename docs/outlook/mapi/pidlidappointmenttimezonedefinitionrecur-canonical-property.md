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
  
Contém um Stream que mapeia para o formato persistente de uma estrutura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição do fuso horário usado quando um compromisso ou uma solicitação de reunião recorrente é criada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefRecur  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008260  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e soluções baseadas em Collaboration Data Objects (CDO) 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam o **dispidApptTZDefRecur** e ** dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) Propriedades para determinar se a reunião recorrente deve ser ajustada se as regras do fuso horário forem alteradas. Essas propriedades devem ser sincronizadas, pois os clientes mais antigos ainda podem manipular a propriedade **dispidTimeZoneStruct** . Para detectar se as duas propriedades estão sincronizadas, o membro **wFlags** da regra que corresponde a **dispidTimeZoneStruct** deve ter o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG definido. Se esse sinalizador não estiver definido ou se for definido e a regra na propriedade **dispidTimeZoneStruct** não corresponder à regra marcada, a propriedade **dispidApptTZDefRecur** deverá ser descartada e o **dispidTimeZoneStruct** deverá ser usado. 
  
Quando você escreve as propriedades **dispidApptTZDefRecur** e **dispidTimeZoneStruct** para uma nova reunião recorrente, ou, quando você faz uma escolha arbitrária para usar a propriedade **dispidTimeZoneStruct** , a definição atual para o fuso horário ( de acordo com o registro do Windows) deve ser usado. 
  
Um analisador deve ser cuidadoso quando lê um fluxo obtido de **dispidApptTZDefRecur**ou quando ele persiste **TZDEFINITION** para um Stream de compromisso para uma propriedade binária, como **dispidApptTZDefRecur**. Para obter mais informações, consulte [sobre a persistência de TZDEFINITION em um Stream para confirmar uma propriedade binária](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** especifica informações de fuso horário que descrevem como converter a data e a hora da reunião em uma série recorrente para e do UTC (tempo Universal Coordenado). Se essa propriedade for definida, mas ela tiver dados inconsistentes com os dados representados por **dispidTimeZoneStruct**, o cliente deverá usar o **dispidTimeZoneStruct** em vez do **dispidApptTZDefRecur**. Se **dispidApptTZDefRecur** não for definido, a propriedade **PidLidTimeZoneStruct** será usada em vez disso. Os campos neste BLOB são codificados em ordem de byte little-endian. 
  
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

