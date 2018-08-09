---
title: Elemento RefBy (Trigger_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Especifica uma referência a uma página de desenho.
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772652"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a>Elemento RefBy (Trigger_Type complexType) ('Visio XML')

Especifica uma referência a uma página de desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> ||
   
## <a name="definition"></a>Definição

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Trigger](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.  <br/> |
|[Trigger](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.  <br/> |
|[Trigger](trigger-elementvisio-xml.md) <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Especifica o atributo ID de uma página de desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|T  <br/> |XSD: String  <br/> |obrigatório  <br/> |Especifica o tipo de referência.  <br/> |Valores do tipo xsd: String.  <br/> |
   

