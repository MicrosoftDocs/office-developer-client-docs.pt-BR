---
title: Elemento validation (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Armazena informações sobre a validação de diagrama do documento.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329077"
---
# <a name="validation-element-visio-xml"></a>Elemento validation (' Visio XML ')

Armazena informações sobre a validação de diagrama do documento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Validation_Type](validation_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum.
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Issues](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |Contém todos os elementos **Issue** do documento.  <br/> |
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Inclui um elemento **RuleSet** para cada conjunto de regras de validação no documento.  <br/> |
|[Validationproperties](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[ValidationProperties_Type](validationproperties_type-complextypevisio-xml.md) <br/> |Encapsula as propriedades relacionadas à validação do documento.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhuma.
  

