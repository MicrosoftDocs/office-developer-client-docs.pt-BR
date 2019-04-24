---
title: Elemento RuleTest (Rule_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.
ms.openlocfilehash: 8fd37040bec383ab61edfa62a09bb766ed8cd3c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319079"
---
# <a name="ruletest-element-ruletype-complextype-visio-xml"></a>Elemento RuleTest (Rule_Type complexType) (' Visio XML ')

Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Rule](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |Representa uma regra de validação única em um conjunto de regras de validação de diagrama.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Fórmula  <br/> |xsd:string  <br/> |opcional  <br/> |Representa a fórmula do elemento.  <br/> |Valores da cadeia de caracteres xsd:.  <br/> |
   

