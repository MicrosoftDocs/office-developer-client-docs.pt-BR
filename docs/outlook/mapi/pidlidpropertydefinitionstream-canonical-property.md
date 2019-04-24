---
title: Propriedade canônica PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315936"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Propriedade canônica PidLidPropertyDefinitionStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa definições de campos definidos pelo usuário e configurações de associação de dados de campos internos de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidPropDefStream  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008540  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Configuração de tempo de execução  <br/> |
   
## <a name="remarks"></a>Comentários

O valor da propriedade **PidLidPropertyDefinitionStream** é salvo como parte da definição de formulário personalizada para a mensagem. 
  
O valor dessa propriedade é um fluxo binário. Para obter informações sobre a estrutura desse fluxo, consulte [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Campos e itens do Outlook](outlook-items-and-fields.md)
  
[Adicionar uma definição para um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemplo de fluxo PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

