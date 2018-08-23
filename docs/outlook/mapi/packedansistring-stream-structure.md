---
title: Estrutura de fluxo de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4e919270efb196cda845581830cc4a918012b385
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578973"
---
# <a name="packedansistring-stream-structure"></a>Estrutura de fluxo de PackedAnsiString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A estrutura de fluxo de PackedAnsiString contém uma representação de ANSI de uma cadeia de caracteres, com base na página de código ANSI do computador no qual está executando o Microsoft Outlook. Esta cadeia de caracteres não será terminada por um caractere nulo. Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem listada abaixo. Os elementos de dados reais que existem dependem do comprimento da cadeia de caracteres na representação ANSI.
  
- Para uma cadeia de caracteres cuja representação ANSI contém menor do que 255 bytes, os elementos de dados são os seguintes:
    
  - Duração: BYTE (1 byte), o comprimento, em número de bytes, da representação da sequência de caracteres ANSI.
    
  - Caracteres: Uma matriz de CHAR. A contagem dessa matriz é igual do elemento de dados de comprimento. Os dados na matriz são a representação de ANSI da cadeia de caracteres.
    
- Para uma cadeia de caracteres cuja representação ANSI contém 255 a 65.535 bytes, os elementos de dados são os seguintes:
    
  - Prefixo: BYTE (1 byte), o valor de 255 (0xff).
    
  - Duração: WORD (2 bytes), o comprimento, em número de bytes, da representação da sequência de caracteres ANSI.
    
  - Caracteres: Uma matriz de CHAR. A contagem dessa matriz é igual do elemento de dados de comprimento. Os dados na matriz são a representação de ANSI da cadeia de caracteres.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Estruturas de fluxo](stream-structures.md)
  
[Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)

