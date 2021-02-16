---
title: Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: As propriedades de fuso horário, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur e PidLidAppointmentTimeZoneDefinitionStartDisplay são propriedades nomeadas como binárias, cada uma contem um fluxo de mapas para o formato persistente de uma estrutura TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316972"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária

As propriedades de fuso horário, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx) e [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) são propriedades nomeadas como binárias, cada uma contem um fluxo de mapas para o formato persistente de uma estrutura [TZDEFINITION](tzdefinition.md). 
  
Este tópico descreve um pouco formato little endian que pode ser usado na persistência do fluxo **TZDEFINITION** para confirmar uma das três propriedades binárias. Usar o mesmo formato endian em um analisador para interpretar um valor de fluxo obtido a partir de uma dessas propriedades. 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

O número de versão principal é usado para alterar uma quebra. Clientes que não estejam familiarizados com o número de versão principal devem tratar a propriedade como se não estivesse lá. Clientes escrevendo a estrutura devem especificar a constante **TZ_BIN_VERSION_MAJOR**. 
  
O número da versão secundária é usado para extensibilidade. Clientes que não são familiarizados com o número de versão secundária devem ler os dados que eles compreendem, e ignorar os dados que podem estar anexados a cada regra do fluxo atual. Clientes escrevendo a estrutura devem especificar a constante **TZ_BIN_VERSION_MINOR**. 
  
Se uma analisador não entende a versão principal do cabeçalho, ele não deve ler o restante da estrutura e se comportar como se os dados estivessem ausentes. Se uma analisador não entende a versão secundária de cabeçalho, deverá usar **cbHeader** para ignorar partes que não entende e avançar para ler as partes do fluxo que ele entende. 
  
O valor de **wFlags** sempre é **TZDEFINITION_FLAG_VALID_KEYNAME**. O nome da chave tem um limite de tamanho de **MAX_PATH**. 
  
Se uma analisador não reconhecer a versão principal de uma regra, o cliente deve ignorar a regra e usar **cbRule** para avançar para a regra seguinte. Se uma analisador não reconhecer a versão secundária de uma regra, o cliente só deve analisar as partes compreensíveis da regra. 
  
Quando uma estrutura **TZDEFINITION** persistir para um fluxo, o analisador não deve tentar gravar as informações que ele não entende. 
  
O número máximo de regras é 1024.
  
Observe que a estrutura[TZREG](tzreg.md) é mantida aqui, diferente de quando ela continua sozinha, por isso o mesmo código mesmo não pode ser usado para análise. 
  
## <a name="see-also"></a>Confira também

- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Ler propriedades de fuso horário de um compromisso](how-to-read-time-zone-properties-from-an-appointment.md)

