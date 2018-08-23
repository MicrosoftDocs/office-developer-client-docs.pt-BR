---
title: Estrutura de fluxo de PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569194"
---
# <a name="packedunicodestring-stream-structure"></a>Estrutura de fluxo de PackedUnicodeString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A estrutura de fluxo de PackedUnicodeString contém uma representação Unicode (UTF-16) de uma cadeia de caracteres. Esta cadeia de caracteres não será terminada por um caractere nulo. Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem listada abaixo. Os elementos de dados reais que existem dependem do comprimento da cadeia de caracteres na representação UTF-16.
  
- Para uma cadeia de caracteres cuja representação UTF-16 contém menor do que 255 WCHARs, os elementos de dados são os seguintes:
    
  - Duração: BYTE (1 byte), o comprimento, em número de WCHARs, da codificação UTF-16 representação da sequência de caracteres.
    
  - Caracteres: Uma matriz de WCHAR. A contagem dessa matriz é igual do elemento de dados de comprimento. Os dados na matriz são a representação UTF-16 da cadeia de caracteres.
    
- Para uma cadeia de caracteres cuja representação UTF-16 contém WCHARs 255 e 65535, os elementos de dados são os seguintes:
    
  - Prefixo: BYTE (1 byte), o valor de 255 (0xff).
    
  - Duração: WORD (2 bytes), o comprimento, em número de WCHARs, da codificação UTF-16 representação da sequência de caracteres.
    
  - Caracteres: Uma matriz de WCHAR. A contagem dessa matriz é igual do elemento de dados de comprimento. Os dados na matriz são a representação UTF-16 da cadeia de caracteres.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)

