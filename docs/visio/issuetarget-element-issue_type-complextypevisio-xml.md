---
title: Elemento IssueTarget (Issue_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai. Se o destino da questão de validação do pai for um documento, IssueTarget especifica nem uma página nem uma forma.
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772142"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a>Elemento IssueTarget (Issue_Type complexType) ('Visio XML')

Dependendo de destino do pai questão de validação, especifica a página, ou a página e forma, associada a questão de validação do pai. Se o destino da questão de validação do pai for um documento, **IssueTarget** especifica nem uma página nem uma forma. 
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[IssueTarget_Type](issuetarget_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Validation.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
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
|PageID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo da página que está associado a questão de validação do pai. Se o destino for o documento, o valor de PageID pode ser 0xFFFFFFFF.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Identificação da forma  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o identificador exclusivo da forma que está associado com a questão de validação do pai. Se o destino for um documento ou uma página, o valor de identificação da forma pode ser 0xFFFFFFFF.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

