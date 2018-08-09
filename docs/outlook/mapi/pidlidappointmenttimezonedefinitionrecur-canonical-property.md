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
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768329"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Propriedade canônica PidLidAppointmentTimeZoneDefinitionRecur

  
  
**Aplica-se a**: Outlook 
  
Contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição para o fuso horário que é usado quando uma solicitação de reunião ou um compromisso recorrente é criada. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptTZDefRecur  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008260  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e soluções baseadas em Collaboration Data Objects (CDO) 1.2.1 que executaram o calendário do Outlook ou o Exchange Server atualizar o uso da ferramenta de **dispidApptTZDefRecur** e ** dispidTimeZoneStruct** propriedades ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar se a reunião recorrente deve ser ajustada se alterar as regras do fuso horário. Essas propriedades devem ser sincronizadas, pois clientes mais antigos ainda podem manipular a propriedade **dispidTimeZoneStruct** . Para detectar se as duas propriedades são sincronizadas, o membro **wFlags** para a regra que corresponde a **dispidTimeZoneStruct** deve ter o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG definido. Se esse sinalizador não estiver definida, ou seja definido e a regra na propriedade **dispidTimeZoneStruct** não coincide com a regra marcada, a propriedade **dispidApptTZDefRecur** deverão ser descartada e **dispidTimeZoneStruct** deve ser usada em vez disso. 
  
Quando você escreve **dispidApptTZDefRecur** tanto o **dispidTimeZoneStruct** propriedades para uma nova reunião recorrente ou, quando você faz uma opção arbitrária para usar a propriedade **dispidTimeZoneStruct** , a definição atual para o (de fuso horário de acordo com o registro do Windows) deve ser usado. 
  
Um analisador deve tomar cuidado quando ele lê um fluxo que for obtido de **dispidApptTZDefRecur**ou quando ele persiste **TZDEFINITION** a um fluxo de compromisso em uma propriedade binária como **dispidApptTZDefRecur**. Para obter mais informações, consulte [About TZDEFINITION mantendo a um fluxo de confirmar uma propriedade binária](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** Especifica as informações de fuso horário que descrevem como converter a data da reunião e a hora em uma série recorrente para e do tempo Universal Coordenado (UTC). Se essa propriedade estiver definida, mas ela tem dados inconsistente com os dados representados pela **dispidTimeZoneStruct**, o cliente deve usar **dispidTimeZoneStruct** em vez de **dispidApptTZDefRecur**. Se **dispidApptTZDefRecur** não estiver definida, a propriedade **PidLidTimeZoneStruct** será usada. Os campos neste BLOB são codificados em ordem de bytes endian pouco. 
  
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

