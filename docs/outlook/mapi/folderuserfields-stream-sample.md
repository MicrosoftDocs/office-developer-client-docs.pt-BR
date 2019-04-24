---
title: Exemplo de fluxo FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281363"
---
# <a name="folderuserfields-stream-sample"></a>Exemplo de fluxo FolderUserFields

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico descreve um exemplo de um fluxo do FolderUserFields. O Stream contém uma definição de um campo definido pelo usuário `TextField1`. O tipo é **Text**e o Stream FolderUserFields contém as partes FolderUserFieldsAnsi e FolderUserFieldsUnicode. Para obter mais informações, consulte [estruturas de fluxo de campos de pasta](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Despejo de dados

O seguinte é um despejo de dados do Stream como seria exibido em um editor binário.
  
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
   

Veja a seguir uma análise dos dados de exemplo para o fluxo **FolderUserFields** :
  
- FolderUserFieldsAnsi: offset 0x0.
    
  - FieldDefinitionCount: offset 0x0, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: offset 0x4, matriz de 2 fluxos de FolderFieldDefinitionA.
    
    **Primeiro elemento de matriz**:
    
    - FieldType: offset 0x4, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: offset 0x8, 2 bytes: 0x000A (10)
      
    - FieldName: offset 0xA, matriz de 10 caracteres. Valor da cadeia de caracteres ANSI: "TextField1".
      
    - Comum: offset 0x14.
    
      - PropSetGuid: offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: offset 0x28, 4 bytes: 0x00000000.
        
      - dwBitmap: offset 0x2C, 4 bytes: 0x00000000.
        
      - dwDisplay: offset 0x30, 4 bytes: 0x00000000.
        
      - iFmt: offset 0x34, 4 bytes: 0x00000000.
        
      - wszFormulaLength: offset 0x38, 2 bytes: 0x0000 (0).
        
      - wszFormula: offset 0x3A, matriz de 0 WCHAR. Valor de cadeia de caracteres vazia.
    
    **Segundo elemento de matriz**:
    
    - FieldType: offset 0x3A, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: offset 0x3E, 2 bytes: 0x0000 (0).
      
    - FieldName: offset 0x40, matriz de 0 caracteres. Valor de cadeia de caracteres vazia.
      
    - Comum: offset 0x40.
    
      - PropSetGuid: offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: offset 0x50, 4 bytes: 0x00000000 (0).
        
      - dwString: offset 0x54, 4 bytes: 0x00000000.
        
      - dwBitmap: offset 0x58, 4 bytes: 0x00000000.
        
      - dwDisplay: offset 0x5C, 4 bytes: 0x00000000.
        
      - iFmt: offset 0x60, 4 bytes: 0x00000000.
        
      - wszFormulaLength: offset 0x64, 2 bytes: 0x0000 (0).
        
      - wszFormula: offset 0x66, matriz de 0 WCHAR. Valor de cadeia de caracteres vazia.
    
- FolderUserFieldsUnicode: offset 0x66.
    
  - FieldDefinitionCount: offset 0x66, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: offset 0x6A, matriz de 2 FolderFieldDefinitionW Streams.
    
    **Primeiro elemento de matriz**:
    
    - FieldType: offset 0x6A, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: offset 0x6E, 2 bytes: 0x000A (10).
      
    - FieldName: offset 0x70, matriz de 10 WCHAR. Valor da cadeia de caracteres Unicode: "TextField1".
      
    - Comum: offset 0x84.
    
      - PropSetGuid: offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: offset 0x98, 4 bytes: 0x00000000.
        
      - dwBitmap: offset 0x9C, 4 bytes: 0x00000000.
        
      - dwDisplay: offset 0xA0, 4 bytes: 0x00000000.
        
      - iFmt: offset 0xA4, 4 bytes: 0x00000000.
        
      - wszFormulaLength: offset 0xA8, 2 bytes: 0x0000 (0).
        
      - wszFormula: offset 0xAA, matriz de 0 WCHAR. Valor de cadeia de caracteres vazia.
    
    **Segundo elemento de matriz**:
    
    - FieldType: offset 0xAA, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: offset 0xAE, 2 bytes: 0x0000 (0).
      
    - FieldName: offset 0xB0, matriz de 0 WCHAR. Valor de cadeia de caracteres vazia.
      
    - Comum: offset 0xB0.
    
      - PropSetGuid: offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: offset 0xC0, 4 bytes: 0x00000000 (0).
        
      - dwString: offset 0xC4, 4 bytes: 0x00000000.
        
      - dwBitmap: offset 0xC8, 4 bytes: 0x00000000.
        
      - dwDisplay: offset 0xCC, 4 bytes: 0x00000000.
        
      - iFmt: offset 0xD0, 4 bytes: 0x00000000.
        
      - wszFormulaLength: offset 0xD4, 2 bytes: 0x0000 (0).
        
      - wszFormula: offset 0xD6, matriz de 0 WCHAR. Valor de cadeia de caracteres vazia.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)
- [Estrutura de fluxo FieldDefinition](fielddefinition-stream-structure.md)
- [Estrutura de fluxo SkipBlock](skipblock-stream-structure.md)
- [Estrutura de fluxo FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Estrutura de fluxo PackedAnsiString](packedansistring-stream-structure.md)
- [Estrutura de fluxo PackedUnicodeString](packedunicodestring-stream-structure.md)

