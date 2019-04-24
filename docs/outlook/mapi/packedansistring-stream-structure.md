---
title: Estrutura de fluxo PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348507"
---
# <a name="packedansistring-stream-structure"></a>Estrutura de fluxo PackedAnsiString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A estrutura de fluxo PackedAnsiString contém uma representação ANSI de uma cadeia de caracteres, com base na página de código ANSI do computador em que o Microsoft Outlook está sendo executado. Essa cadeia de caracteres não é terminada por um caractere nulo. Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na ordem listada abaixo. Os elementos de dados reais existentes dependem do comprimento da cadeia de caracteres na representação ANSI.
  
- Para uma cadeia de caracteres cuja representação ANSI contém menos de 255 bytes, os elementos de dados são os seguintes:
    
  - Comprimento: BYTE (1 byte), o comprimento, em número de bytes, da representação ANSI da cadeia de caracteres.
    
  - Caracteres: uma matriz de CHAR. A contagem dessa matriz é igual ao elemento de dados de comprimento. Os dados na matriz são a representação ANSI da cadeia de caracteres.
    
- Para uma cadeia de caracteres cuja representação ANSI contém 255 a 65535 bytes, os elementos de dados são os seguintes:
    
  - Prefixo: BYTE (1 byte), o valor de 255 (0xFF).
    
  - Comprimento: WORD (2 bytes), o comprimento, em número de bytes, da representação ANSI da cadeia de caracteres.
    
  - Caracteres: uma matriz de CHAR. A contagem dessa matriz é igual ao elemento de dados de comprimento. Os dados na matriz são a representação ANSI da cadeia de caracteres.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)

