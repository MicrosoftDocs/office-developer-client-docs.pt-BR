---
title: Elemento RuleInfo (Issue_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica informações sobre a regra de validação que aborde o problema de validação do pai.
ms.openlocfilehash: ff5a7e4e8918d5ae151a0d4582d1a393509e1b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772806"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a>Elemento RuleInfo (Issue_Type complexType) ('Visio XML')

Especifica informações sobre a regra de validação que aborde o problema de validação do pai.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Problema](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Representa uma questão de validação no documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|RuleID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo da regra de validação que aborde o problema pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RuleSetID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo do conjunto de regras de validação que aborde o problema pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

