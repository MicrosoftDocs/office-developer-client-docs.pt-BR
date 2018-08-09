---
title: Elemento de regra (RuleSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa uma regra de validação única em um conjunto de regras de validação de diagrama.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772803"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a>Elemento de regra (RuleSet_Type complexType) ('Visio XML')

Representa uma regra de validação única em um conjunto de regras de validação de diagrama.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Conjunto de regras](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa um conjunto de regras de validação de diagrama.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Category  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica o texto exibido na coluna **categoria** da janela questões. O padrão é uma cadeia de caracteres vazia.  <br/> |Valores do tipo xsd: String.  <br/> |
|Descrição  <br/> |XSD: String  <br/> |opcional  <br/> |Especifica a descrição da regra de validação que aparece na interface do usuário. O padrão é "Desconhecido".  <br/> |Valores do tipo xsd: String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo para a regra de validação.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Ignorado  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se a regra de validação no momento é ignorada. O padrão é False.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|NameU  <br/> |XSD: String  <br/> |obrigatório  <br/> |Especifica o nome universal da regra de validação.  <br/> |Valores do tipo xsd: String.  <br/> |
|RuleTarget  <br/> |XSD:int  <br/> |opcional  <br/> |Especifica o tipo de objeto ao qual se aplica a regra de validação.  <br/> |Valores do tipo xsd:int.  <br/> |
   

