---
title: Elemento de problema (Issues_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa uma questão de validação no documento.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772125"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a>Elemento de problema (Issues_Type complexType) ('Visio XML')

Representa uma questão de validação no documento.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Problemas](issues-element-validation_type-complextypevisio-xml.md) <br/> |[Issues_Type](issues_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **problema** para o documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[IssueTarget](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai.  <br/> |
|[RuleInfo](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[RuleInfo_Type](ruleinfo_type-complextypevisio-xml.md) <br/> |Especifica informações sobre a regra de validação que aborde o problema de validação do pai.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo da questão de validação.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Ignorado  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica informações sobre a regra de validação que aborde o problema de validação do pai.  <br/> |Valores do tipo xsd:boolean.  <br/> |
   

