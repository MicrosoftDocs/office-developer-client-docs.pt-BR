---
title: Estrutura de fluxo PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422611"
---
# <a name="packedunicodestring-stream-structure"></a>Estrutura de fluxo PackedUnicodeString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A estrutura de fluxo PackedUnicodeString contém uma representação Unicode (UTF-16) de uma cadeia de caracteres. Essa cadeia de caracteres não é terminada por um caractere nulo. Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na ordem listada abaixo. Os elementos de dados reais existentes dependem do comprimento da cadeia de caracteres na representação UTF-16.
  
- Para uma cadeia de caracteres cuja representação UTF-16 contenha menos de 255 WCHAR, os elementos de dados são os seguintes:
    
  - Comprimento: BYTE (1 byte), o comprimento, em número de WCHARs, da representação UTF-16 da cadeia de caracteres.
    
  - Caracteres: uma matriz de WCHAR. A contagem dessa matriz é igual ao elemento de dados de comprimento. Os dados na matriz são a representação UTF-16 da cadeia de caracteres.
    
- Para uma cadeia de caracteres cuja representação UTF-16 contenha 255 a 65535 WCHAR, os elementos de dados são os seguintes:
    
  - Prefixo: BYTE (1 byte), o valor de 255 (0xFF).
    
  - Comprimento: WORD (2 bytes), o comprimento, em número de WCHARs, da representação UTF-16 da cadeia de caracteres.
    
  - Caracteres: uma matriz de WCHAR. A contagem dessa matriz é igual ao elemento de dados de comprimento. Os dados na matriz são a representação UTF-16 da cadeia de caracteres.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)

