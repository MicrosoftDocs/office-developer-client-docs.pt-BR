---
title: Exemplo de fluxo de FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 76ad693b05e3989bd64ba66565ae4def22110ad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564896"
---
# <a name="folderuserfields-stream-sample"></a>Exemplo de fluxo de FolderUserFields

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico descreve um exemplo de um fluxo de FolderUserFields. O fluxo contém uma definição de um campo definido pelo usuário, `TextField1`. O tipo é **texto**e o fluxo de FolderUserFields contém FolderUserFieldsAnsi e o FolderUserFieldsUnicode partes. Para obter mais informações, consulte [Estruturas de fluxo de campos de pastas](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Despejo de dados

A seguir está um despejo do fluxo de dados como ela seria exibida em um editor de binário.
  
|Deslocamento de fluxo|Bytes de dados|Dados ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

A seguir está uma análise dos dados de amostra para o fluxo de **FolderUserFields** :
  
- FolderUserFieldsAnsi: Deslocamento 0x0.
    
  - FieldDefinitionCount: Deslocamento 0x0, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: Deslocamento 0x4, matriz de fluxos de FolderFieldDefinitionA 2.
    
    O **primeiro elemento da matriz**:
    
    - FieldType: Deslocamento 0x4, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: Deslocamento 0x8, 2 bytes: 0x000A (10)
      
    - FieldName: Deslocamento 0xA, matriz de 10 caracteres. Valor de cadeia de caracteres ANSI: "TextField1".
      
    - Comuns: Deslocamento 0x14.
    
      - PropSetGuid: Deslocamento 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: deslocamento 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: Offset 0x28, 4 bytes: 0x00000000.
        
      - dwBitmap: deslocamento 0x2C, 4 bytes: 0x00000000.
        
      - dwDisplay: deslocamento 0x30, 4 bytes: 0x00000000.
        
      - iFmt: deslocamento 0x34, 4 bytes: 0x00000000.
        
      - wszFormulaLength: deslocamento 0x38, 2 bytes: 0x0000 (0).
        
      - wszFormula: deslocamento 0x3A, matriz de WCHARs 0. Valor de cadeia de caracteres vazia.
    
    O **segundo elemento de matriz**:
    
    - FieldType: Deslocamento 0x3A, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: Deslocamento 0x3E, 2 bytes: 0x0000 (0).
      
    - FieldName: Deslocamento 0x40, matriz de caracteres de 0. Valor de cadeia de caracteres vazia.
      
    - Comuns: Deslocamento 0x40.
    
      - PropSetGuid: Deslocamento 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: deslocamento 0x50, 4 bytes: 0x00000000 (0).
        
      - dwString: deslocamento 0x54, 4 bytes: 0x00000000.
        
      - dwBitmap: deslocamento 0x58, 4 bytes: 0x00000000.
        
      - dwDisplay: deslocamento 0x5C, 4 bytes: 0x00000000.
        
      - iFmt: deslocamento 0x60, 4 bytes: 0x00000000.
        
      - wszFormulaLength: deslocamento 0x64, 2 bytes: 0x0000 (0).
        
      - wszFormula: deslocamento 0x66, matriz de WCHARs 0. Valor de cadeia de caracteres vazia.
    
- FolderUserFieldsUnicode: Deslocamento 0x66.
    
  - FieldDefinitionCount: Deslocamento 0x66, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: Deslocamento 0x6A, matriz de fluxos de FolderFieldDefinitionW 2.
    
    O **primeiro elemento da matriz**:
    
    - FieldType: Deslocamento 0x6A, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: Deslocamento 0x6E, 2 bytes: 0x000A (10).
      
    - FieldName: Deslocamento 0x70, matriz de 10 WCHARs. Valor de cadeia de caracteres Unicode: "TextField1".
      
    - Comuns: Deslocamento 0x84.
    
      - PropSetGuid: Deslocamento 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: deslocamento 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: deslocamento 0x98, 4 bytes: 0x00000000.
        
      - dwBitmap: deslocamento 0x9C, 4 bytes: 0x00000000.
        
      - dwDisplay: deslocamento 0xA0, 4 bytes: 0x00000000.
        
      - iFmt: deslocamento 0xA4, 4 bytes: 0x00000000.
        
      - wszFormulaLength: deslocamento 0xA8, 2 bytes: 0x0000 (0).
        
      - wszFormula: deslocamento 0xAA, matriz de WCHARs 0. Valor de cadeia de caracteres vazia.
    
    O **segundo elemento de matriz**:
    
    - FieldType: Deslocamento 0xAA, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: Deslocamento 0xAE, 2 bytes: 0x0000 (0).
      
    - FieldName: Deslocamento 0xB0, matriz de WCHARs 0. Valor de cadeia de caracteres vazia.
      
    - Comuns: Deslocamento 0xB0.
    
      - PropSetGuid: Deslocamento 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: deslocamento 0xC0, 4 bytes: 0x00000000 (0).
        
      - dwString: deslocamento 0xC4, 4 bytes: 0x00000000.
        
      - dwBitmap: deslocamento 0xC8, 4 bytes: 0x00000000.
        
      - dwDisplay: deslocamento 0xCC, 4 bytes: 0x00000000.
        
      - iFmt: deslocamento 0xD0, 4 bytes: 0x00000000.
        
      - wszFormulaLength: deslocamento 0xD4, 2 bytes: 0x0000 (0).
        
      - wszFormula: deslocamento 0xD6, matriz de WCHARs 0. Valor de cadeia de caracteres vazia.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Estrutura de fluxo de PropertyDefinition](propertydefinition-stream-structure.md)
- [Estrutura de fluxo de FieldDefinition](fielddefinition-stream-structure.md)
- [Estrutura de fluxo de SkipBlock](skipblock-stream-structure.md)
- [Estrutura de fluxo de FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estrutura de fluxo de PackedAnsiString](packedansistring-stream-structure.md)
- [Estrutura de fluxo de PackedUnicodeString](packedunicodestring-stream-structure.md)

