---
title: Exemplo de fluxo de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770198"
---
# <a name="propertydefinition-stream-sample"></a>Exemplo de fluxo de PropertyDefinition

**Aplica-se a**: Outlook 
  
Este tópico descreve um exemplo de um stream PropertyDefinition. O fluxo contém uma definição de um campo definido pelo usuário, `TextField1`. O tipo é **texto**e a definição está no formato PropDefV2.
  
## <a name="data-dump"></a>Despejo de dados

A seguir está um despejo do fluxo de dados como ela seria exibida em um editor de binário.
  
|Deslocamento de fluxo|Bytes de dados|Dados ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
A seguir está uma análise dos dados de amostra para o fluxo de PropertyDefinition:
  
- Versão: Deslocamento 0x0, 2 bytes: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: Deslocamento 0x2, 4 bytes: 0x1 (1).
    
- FieldDefinitions: Deslocamento 0x6, matriz de fluxo de FieldDefinition 1.
    
  - Sinalizadores: Deslocamento 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: Deslocamento 0xA, 2 bytes: 0x8 (**VT_BSTR**).
    
  - DispId: Deslocamento 0xC, 4 bytes: 0x0 (0).
    
  - NmidNameLength: Deslocamento 0x10, 2 bytes: 0xA (10).
    
  - NmidName: Deslocamento 0x12, matriz de 10 WCHARs. Valor de cadeia de caracteres Unicode: "TextField1".
    
  - NameANSI: Deslocamento 0x26, PackedAnsiString stream.
    
    - Duração: Deslocamento 0x26, 1 byte: 0xA (10).
      
    - Caracteres: Deslocamento 0x27, matriz de 10 caracteres. Valor de cadeia de caracteres ANSI: "TextField1".
    
  - FormulaANSI: Deslocamento 0x31, PackedAnsiString stream.
    
    - Duração: Deslocamento 0x31, 1 byte: 0x0 (0).
      
    - Caracteres: Deslocamento 0x32, matriz de caracteres de 0. Cadeia de caracteres vazia do ANSI.
    
  - ValidationRuleANSI: Deslocamento 0x32, PackedAnsiString stream.
    
    - Duração: Deslocamento 0x32, 1 byte: 0x0 (0).
      
    - Caracteres: Deslocamento 0x33, matriz de caracteres de 0. Cadeia de caracteres vazia do ANSI.
    
  - ValidationTextANSI: Deslocamento 0x33, PackedAnsiString stream.
    
    - Duração: Deslocamento 0x33, 1 byte: 0x0 (0).
      
    - Caracteres: Deslocamento 0x34, matriz de caracteres de 0. Cadeia de caracteres vazia do ANSI.
    
  - ErrorANSI: Deslocamento 0x34, PackedAnsiString stream.
    
    - Duração: Deslocamento 0x34, 1 byte: 0x0 (0).
      
    - Caracteres: Deslocamento 0x35, matriz de caracteres de 0. Cadeia de caracteres vazia do ANSI.
    
  - InternalType: Deslocamento 0x35, 4 bytes: 0x0 (iTypeString).
    
  - SkipBlocks: Deslocamento 0x39, série de fluxos de SkipBlock.
    
  - Primeiro SkipBlock
    
    - Tamanho: Deslocamento 0x39, 4 bytes: 0x15 (21).
      
    - Conteúdo: Deslocamento 0x3D, a matriz de bytes 21. Isso é o primeiro fluxo do SkipBlock, essa matriz contém um fluxo de FirstSkipBlockContent.
      
      - FieldName: Deslocamento 0x3D, PackedUnicodeString stream.
        
        - Duração: Deslocamento 0x3D, 1 byte: 0xA (10).
          
        - Caracteres: Deslocamento 0x3E, matriz de 10 WCHARs. Valor de cadeia de caracteres Unicode: "TextField1".
    
  - Segundo SkipBlock
    
    - Tamanho: Deslocamento 0x52, 4 bytes: 0x0 (0). Este é o fluxo de SkipBlock terminação.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do outlook](outlook-items-and-fields.md)
- [Estruturas de fluxo](stream-structures.md)
- [Estrutura de fluxo de PropertyDefinition](propertydefinition-stream-structure.md)
- [Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)
- [Estrutura de fluxo de SkipBlock](skipblock-stream-structure.md)
- [Estrutura de fluxo de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estrutura de fluxo de PackedAnsiString](packedansistring-stream-structure.md)
- [Estrutura de fluxo de PackedUnicodeString](packedunicodestring-stream-structure.md)

