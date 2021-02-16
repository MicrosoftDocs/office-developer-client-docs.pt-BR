---
title: Propriedade canônica PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346372"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propriedade canônica PidLidTimeZoneStruct

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um fluxo que é mapeado para o formato persistente de uma estrutura [TZREG,](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) que descreve o fuso horário a ser usado para a hora de início e término de um compromisso recorrente ou solicitação de reunião. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTimeZoneStruct  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008233  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Office Outlook 2003, versões anteriores do Outlook e aplicativos baseados no CDO (Collaboration Data Objects) 1.21 cujos usuários não executaram a ferramenta de atualização de calendário fornecida pelo Outlook ou pelo Exchange Server armazenam a hora de início e a hora de término de um compromisso recorrente ou solicitação de reunião como hora relativa e armazenam o fuso horário onde a solicitação de compromisso ou reunião é criada em **dispidTimeZoneStruct**. No entanto, esse esquema ignora que, ao longo do tempo, as regras de fuso horário podem ser alteradas, resultando em alguns compromissos e reuniões agendadas pelos usuários antes da alteração das regras e em horários incorretos. Os usuários e administradores que não estão executando o Windows Vista ou que não têm atualizações automáticas ativas devem usar as ferramentas de base de calendário fornecidas pelo Outlook ou pelo Exchange Server para ajustar o horário desses compromissos e solicitações de reunião. Para obter mais informações sobre essas ferramentas de base de calendário e APIs que baseiam calendários, consulte Sobre a base de calendários programaticamente para o horário de [verão](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Use o seguinte formato endian ao analisar um fluxo obtido de **dispidTimeZoneStruct** ou ao persistir a estrutura **TZREG** em um fluxo para se comprometer com a propriedade binária **dispidTimeZoneStruct.** 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Essa propriedade é definida em uma série recorrente para especificar informações de fuso horário e especifica como converter campos de tempo entre a hora local e o TEMPO Universal Coordenado (UTC).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

