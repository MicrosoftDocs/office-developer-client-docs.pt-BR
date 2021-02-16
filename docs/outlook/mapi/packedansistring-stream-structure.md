---
title: Estrutura de fluxo de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404502"
---
# <a name="packedansistring-stream-structure"></a>Estrutura de fluxo de PackedAnsiString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A estrutura de fluxo PackedAnsiString contém uma representação ANSI de uma cadeia de caracteres, com base na página de código ANSI do computador no qual o Microsoft Outlook está sendo executado. Essa cadeia de caracteres não é encerrada por um caractere nulo. Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na ordem listada abaixo. Os elementos de dados reais existentes dependem do comprimento da cadeia de caracteres na representação ANSI.
  
- Para uma cadeia de caracteres cuja representação ANSI contém menos de 255 bytes, os elementos de dados são:
    
  - Comprimento: BYTE (1 byte), o comprimento, em número de bytes, da representação ANSI da cadeia de caracteres.
    
  - Caracteres: uma matriz de CHAR. A contagem dessa matriz é igual ao elemento de dados Length. Os dados na matriz são a representação ANSI da cadeia de caracteres.
    
- Para uma cadeia de caracteres cuja representação ANSI contém de 255 a 65535 bytes, os elementos de dados são:
    
  - Prefixo: BYTE (1 byte), o valor de 255 (0xff).
    
  - Comprimento: WORD (2 bytes), o comprimento, em número de bytes, da representação ANSI da cadeia de caracteres.
    
  - Caracteres: uma matriz de CHAR. A contagem dessa matriz é igual ao elemento de dados Length. Os dados na matriz são a representação ANSI da cadeia de caracteres.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de Fluxo de FieldDefinition](fielddefinition-stream-structure.md)

