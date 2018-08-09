---
title: Propriedade canônica PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770145"
---
# <a name="pidtaguserfields-canonical-property"></a>Propriedade canônica PidTagUserFields

  
  
**Aplica-se a**: Outlook 
  
Contém o nome, tipo de dados e outras informações sobre um campo definido pelo usuário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_USERFIELDS  <br/> |
|Identificador:  <br/> |0x36E3  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pasta MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente. A propriedade **PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md), que contém as definições de campo. Para obter mais informações sobre as estruturas de fluxo de definições de campo, consulte [Estruturas de Stream](stream-structures.md).
  
Para cada pasta, o Outlook armazena as definições de todos os campos definidos pelo usuário nessa pasta na propriedade **PidTagUserFields** de uma mensagem associada da classe de mensagem, IPC.MS. REN. CAMPOS - cada pasta provável que contenha não mais de uma mensagem desta classe na sua tabela de conteúdo associado. 
  
> [!NOTE]
> O conjunto de campos definido pelo usuário em uma pasta pode não necessariamente corresponder os conjuntos de campos definidos pelo usuário em cada um dos seus itens. 
  
O conjunto de campos definido pelo usuário em uma pasta é exibido em vários locais da UI do Outlook, como o seletor de campos da pasta. Propriedade **PidTagUserFields** da mensagem contém um fluxo binário, **FolderUserFields**, que contém as definições de campo da pasta. Para obter mais informações sobre as estruturas de fluxo de definições de campo de pasta, consulte [Pasta estruturas de fluxo de campos](folder-fields-stream-structures.md) e a [Amostra de fluxo de FolderUserFields](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Cabeçalho da seção

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Adicionar uma definição de um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo de PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

