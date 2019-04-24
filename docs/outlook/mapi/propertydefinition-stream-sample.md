---
title: Exemplo de fluxo PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328501"
---
# <a name="propertydefinition-stream-sample"></a>Exemplo de fluxo PropertyDefinition

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico descreve um exemplo de um fluxo do PropertyDefinition. O Stream contém uma definição de um campo definido pelo usuário `TextField1`. O tipo é **texto**e a definição está no formato PropDefV2.
  
## <a name="data-dump"></a>Despejo de dados

O seguinte é um despejo de dados do Stream como seria exibido em um editor binário.
  
|Deslocamento de fluxo|Bytes de dados|Dados ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Veja a seguir uma análise dos dados de exemplo para o fluxo PropertyDefinition:
  
- Versão: offset 0x0, 2 bytes: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: offset 0x2, 4 bytes: 0x1 (1).
    
- FieldDefinitions: offset 0x6, matriz de 1 FieldDefinition Stream.
    
  - Sinalizadores: offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).
    
  - DispId: offset 0xC, 4 bytes: 0x0 (0).
    
  - NmidNameLength: offset 0x10, 2 bytes: 0xA (10).
    
  - NmidName: offset 0x12, matriz de 10 WCHAR. Valor da cadeia de caracteres Unicode: "TextField1".
    
  - NameANSI: offset 0x26, PackedAnsiString Stream.
    
    - Comprimento: offset 0x26, 1 byte: 0xA (10).
      
    - Caracteres: offset 0x27, matriz de 10 caracteres. Valor da cadeia de caracteres ANSI: "TextField1".
    
  - FormulaANSI: offset 0x31, PackedAnsiString Stream.
    
    - Comprimento: offset 0x31, 1 byte: 0x0 (0).
      
    - Caracteres: offset 0x32, matriz de 0 caracteres. Cadeia de caracteres ANSI vazia.
    
  - ValidationRuleANSI: offset 0x32, PackedAnsiString Stream.
    
    - Comprimento: offset 0x32, 1 byte: 0x0 (0).
      
    - Caracteres: offset 0x33, matriz de 0 caracteres. Cadeia de caracteres ANSI vazia.
    
  - ValidationTextANSI: offset 0x33, PackedAnsiString Stream.
    
    - Comprimento: offset 0x33, 1 byte: 0x0 (0).
      
    - Caracteres: offset 0x34, matriz de 0 caracteres. Cadeia de caracteres ANSI vazia.
    
  - ErrorANSI: offset 0x34, PackedAnsiString Stream.
    
    - Comprimento: offset 0x34, 1 byte: 0x0 (0).
      
    - Caracteres: offset 0x35, matriz de 0 caracteres. Cadeia de caracteres ANSI vazia.
    
  - InternalType: offset 0x35, 4 bytes: 0x0 (iTypeString).
    
  - SkipBlocks: offset 0x39, série de fluxos do SkipBlock.
    
  - Primeira SkipBlock
    
    - Tamanho: offset 0x39, 4 bytes: 0x15 (21).
      
    - Content: offset 0x3D, matriz de 21 bytes. Este é o primeiro fluxo de SkipBlock, portanto, esta matriz contém um fluxo FirstSkipBlockContent.
      
      - FieldName: offset 0x3D, PackedUnicodeString Stream.
        
        - Comprimento: offset 0x3D, 1 byte: 0xA (10).
          
        - Caracteres: offset 0x3E, matriz de 10 WCHAR. Valor da cadeia de caracteres Unicode: "TextField1".
    
  - Segunda SkipBlock
    
    - Tamanho: offset 0x52, 4 bytes: 0x0 (0). Este é o fluxo de SkipBlock de terminação.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Estruturas de fluxo](stream-structures.md)
- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)
- [Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)
- [Estrutura de fluxo SkipBlock](skipblock-stream-structure.md)
- [Estrutura de fluxo FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estrutura de fluxo PackedAnsiString](packedansistring-stream-structure.md)
- [Estrutura de fluxo PackedUnicodeString](packedunicodestring-stream-structure.md)

