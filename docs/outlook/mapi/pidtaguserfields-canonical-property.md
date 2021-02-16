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
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360736"
---
# <a name="pidtaguserfields-canonical-property"></a>Propriedade canônica PidTagUserFields

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome, o tipo de dados e outras informações sobre um campo definido pelo usuário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_USERFIELDS  <br/> |
|Identificador:  <br/> |0x36E3  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pasta MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente. A **propriedade PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md), que contém as definições de campo. Para obter mais informações sobre estruturas de fluxo para definições de campo, consulte [Estruturas de fluxo.](stream-structures.md)
  
Para cada pasta, o Outlook armazena as definições de todos os campos definidos pelo usuário nessa pasta na propriedade **PidTagUserFields** de uma mensagem associada da classe de mensagem IPC.MS. REN. USERFIELDS - cada pasta presumida de conter não mais de uma mensagem dessa classe em sua tabela de conteúdo associada. 
  
> [!NOTE]
> O conjunto de campos definidos pelo usuário em uma pasta pode não corresponder necessariamente aos conjuntos de campos definidos pelo usuário em cada um de seus itens. 
  
O conjunto de campos definidos pelo usuário em uma pasta é exibido em vários lugares na interface do usuário do Outlook, como o Selador de Campos da pasta. A propriedade **PidTagUserFields** da mensagem contém um fluxo binário, **FolderUserFields**, que contém as definições de campo de pasta. Para obter mais informações sobre estruturas de fluxo para definições de campo de pasta, consulte [Estruturas](folder-fields-stream-structures.md) de fluxo de campos de pasta e o exemplo de fluxo [FolderUserFields](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Cabeçalho da seção

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Adicionar uma definição para um novo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo propertyDefinition](propertydefinition-stream-sample.md)
  
[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

