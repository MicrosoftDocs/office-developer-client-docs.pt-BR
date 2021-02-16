---
title: Elemento Rule (RuleSet_Type complexType) (VISio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa uma regra de validação única em um conjunto de regras de validação de diagrama.
ms.openlocfilehash: 0d848ce3309d7dfc5a89b201be30ce060ec6f88f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541705"
---
# <a name="rule-element-ruleset_type-complextype-visio-xml"></a>Elemento Rule (RuleSet_Type complexType) (VISio XML)

Representa uma regra de validação única em um conjunto de regras de validação de diagrama.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rule_Type](rule_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RuleSet](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa um conjunto de regras de validação de diagrama.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RuleFilter](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[RuleFilter_Type](rulefilter_type-complextypevisio-xml.md) <br/> |Especifica a expressão lógica que determina se a regra de validação deve ser aplicada a um objeto de destino.  <br/> |
|[RuleTest](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[RuleTest_Type](ruletest_type-complextypevisio-xml.md) <br/> |Especifica a expressão lógica que determina se o objeto de destino satisfaz a regra de validação.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Categoria  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o texto exibido na coluna **Categoria** da janela Problemas. O padrão é uma cadeia de caracteres vazia.  <br/> |Valores do tipo xsd:string.  <br/> |
|Descrição  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica a descrição da regra de validação que aparece na interface do usuário. O padrão é "Desconhecido".  <br/> |Valores do tipo xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo para a regra de validação.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Ignorado  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se a regra de validação é ignorada no momento. O padrão é False.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|NameU  <br/> |xsd:string  <br/> |obrigatório  <br/> |Especifica o nome universal da regra de validação.  <br/> |Valores do tipo xsd:string.  <br/> |
|RuleTarget  <br/> |xsd:int  <br/> |opcional  <br/> |Especifica o tipo de objeto ao qual a regra de validação se aplica.  <br/> |Valores do tipo xsd:int.  <br/> |
   

