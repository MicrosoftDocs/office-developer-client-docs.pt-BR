---
title: Estrutura de fluxo de PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768202"
---
# <a name="packedunicodestring-stream-structure"></a>Estrutura de fluxo de PackedUnicodeString

  
  
**Aplica-se a**: Outlook 
  
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

