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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401612"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propriedade canônica PidLidTimeZoneStruct

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um stream que mapeie para o formato persistente de uma estrutura [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , que descreve o fuso horário a ser usado para a hora de início e término de uma solicitação de reunião ou um compromisso recorrente. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidTimeZoneStruct  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008233  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Office Outlook 2003, versões anteriores do Outlook e aplicativos que se baseiam em Collaboration Data Objects (CDO) 1.21 cujos usuários não executou a ferramenta de atualização de calendário fornecida pelo Outlook ou o Exchange Server armazenam a hora de início e a hora de término de um recorrente compromisso ou uma solicitação de reunião, como tempo relativo e armazene o fuso horário em que a solicitação de reunião ou compromisso é criada no **dispidTimeZoneStruct**. No entanto, esse esquema ignora que ao longo do tempo, as regras de fuso horário podem mudar, resultando em alguns compromissos e reuniões que os usuários agendado antes que as regras alteradas e ocorrerem em momentos incorretos. Usuários e administradores que não estejam executando o Windows Vista ou que não têm atualizações automáticas ativadas devem usar o calendário a alteração da Base de ferramentas que são fornecidas pelo Outlook ou o Exchange Server para ajustar o tempo de tais compromissos e solicitações de reunião. Para obter mais informações sobre essas ferramentas de REBASE de calendário e APIs que alterar a calendários base, consulte [About REBASE de calendários programaticamente para o horário de verão](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Use o seguinte formato de pouca-endian durante a análise de um stream obtido a partir de **dispidTimeZoneStruct**ou quando mantendo a estrutura **TZREG** a um fluxo para comprometer à propriedade **dispidTimeZoneStruct** binário. 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Essa propriedade for definida em uma série recorrente para especificar informações de fuso horário e especifica como converter os campos de hora entre hora local e o tempo Universal Coordenado (UTC).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

