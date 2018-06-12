---
title: Sobre TZDEFINITION mantendo a um fluxo ao confirmar em uma propriedade binária
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: As propriedades de fuso horário, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur e PidLidAppointmentTimeZoneDefinitionStartDisplay são binário denominado propriedades, cada um deles contém um stream que mapeie para o formato persistente de uma estrutura TZDEFINITION.
ms.openlocfilehash: 8e00c7203e2a0adfdf9ff3e6dadff6485c8b5111
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765786"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>Sobre TZDEFINITION mantendo a um fluxo ao confirmar em uma propriedade binária

As propriedades de fuso horário, [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)e [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) são binário denominado propriedades, cada um deles contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](tzdefinition.md) . 
  
Este tópico descreve um pouco formato endian que pode ser usado quando mantendo **TZDEFINITION** a um fluxo para comprometer a uma das três propriedades binárias. Use o mesmo formato endian em um analisador para interpretar um valor de stream obtido de uma dessas propriedades. 
  
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

O número de versão principal é usado para fazer uma quebra de alteração. Clientes que não estiver familiarizados com o número da versão principal devem tratar a propriedade como se ele não estiver lá. Gravando a estrutura de clientes devem especificar a constante **TZ_BIN_VERSION_MAJOR**. 
  
O número da versão secundária é usado para fornecer extensibilidade. Clientes que não estiver familiarizados com o número da versão secundária devem ler os dados que eles entender e ignoram os dados que podem ser acrescentados para cada regra ou para o fluxo geral. Gravando a estrutura de clientes devem especificar a constante **TZ_BIN_VERSION_MINOR**. 
  
Se um analisador não entender a versão principal do cabeçalho, ela não deve ler o restante da estrutura e se comportam como se os dados estão ausentes. Se um analisador não entender a versão secundária do cabeçalho, ele deve usar **cbHeader** para ignorar as partes que ele não entende e avanço para ler as partes do stream que ela compreende. 
  
O valor de **wFlags** é sempre **TZDEFINITION_FLAG_VALID_KEYNAME**. O nome da chave tem um tamanho máximo de **MAX_PATH**. 
  
Se um analisador não reconhece a versão principal de uma regra, o cliente deve ignorar a regra e use **cbRule** para ir para a próxima regra. Se um analisador não reconhece a versão secundária de uma regra, o cliente só deve analisar as partes da regra que ela compreende. 
  
Quando mantendo uma estrutura **TZDEFINITION** a um fluxo, um analisador não deve tentar gravar todas as informações que ele não entende. 
  
O número máximo de regras é 1024.
  
Observe que a estrutura [TZREG](tzreg.md) é persistente aqui diferentemente vez quando persistentes sozinhos, portanto o mesmo código não pode ser usado para analisá-lo. 
  
## <a name="see-also"></a>Confira também

- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Ler as propriedades de fuso horário de um compromisso](how-to-read-time-zone-properties-from-an-appointment.md)

