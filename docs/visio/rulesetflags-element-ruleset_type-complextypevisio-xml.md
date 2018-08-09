---
title: Elemento RuleSetFlags (RuleSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c18d3a84-2088-13f7-7b14-1f4c129537b4
description: Especifica as propriedades de conjunto de regras.
ms.openlocfilehash: f656e8ace045d45460ab353444c39c760448aa7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772819"
---
# <a name="rulesetflags-element-rulesettype-complextype-visio-xml"></a>Elemento RuleSetFlags (RuleSet_Type complexType) ('Visio XML')

Especifica as propriedades de conjunto de regras.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleSetFlags_Type](rulesetflags_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RuleSetFlags" type="RuleSetFlags_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Conjunto de regras](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[RuleSet_Type](ruleset_type-complextypevisio-xml.md) <br/> |Representa um conjunto de regras de validação de diagrama.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Oculto  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica se o conjunto de regras aparece na lista de verificação de regras.  <br/> |Valores do tipo xsd:boolean.  <br/> |
   

