---
title: Elemento RuleSet (RuleSets_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa um conjunto de regras de validação de diagrama.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541635"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a>Elemento RuleSet (RuleSets_Type complexType) (XML do Visio)

Representa um conjunto de regras de validação de diagrama.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RuleSets](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[RuleSets_Type](rulesets_type-complextypevisio-xml.md) <br/> |Inclui um elemento **RuleSet** para cada conjunto de regras de validação no documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Representa uma regra de validação única em um conjunto de regras de validação de diagrama.  <br/> |
|[RuleSetFlags](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |Especifica as propriedades do conjunto de regras.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Descrição  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica a descrição que aparece na interface do usuário para o conjunto de regras de validação. O padrão é uma cadeia de caracteres vazia.  <br/> |Valores do tipo xsd:string.  <br/> |
|Habilitado  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se as regras no conjunto de regras de validação especificado são verificadas quando a validação é disparada para o documento atual. O padrão é True.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo do conjunto de regras de validação.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome local do conjunto de regras de validação. O padrão é o valor do atributo nameu.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica o nome universal do conjunto de regras de validação.  <br/> |Valores do tipo xsd:string.  <br/> |
   

