---
title: Elemento IssueTarget (Issue_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Dependendo do destino da questão de validação pai, especifica a página ou a página e a forma, associadas à questão de validação pai. Se o destino da questão de validação pai for um documento, IssueTarget especifica nem uma página nem uma forma.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542951"
---
# <a name="issuetarget-element-issue_type-complextype-visio-xml"></a>Elemento IssueTarget (Issue_Type complexType) (XML do Visio)

Dependendo do destino da questão de validação pai, especifica a página ou a página e a forma, associadas à questão de validação pai. Se o destino da questão de validação pai for um documento, **IssueTarget** especifica nem uma página nem uma forma. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |validation.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Problema](issue-element-issues_type-complextypevisio-xml.md) <br/> |[Issue_Type](issue_type-complextypevisio-xml.md) <br/> |Representa uma única questão de validação no documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo da página que está associada à questão de validação pai. Se o destino for o documento, o valor de PageID poderá ser 0xFFFFFFFF.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo da forma que está associada à questão de validação pai. Se o destino for o documento ou uma página, o valor de ShapeID poderá ser 0xFFFFFFFF.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

