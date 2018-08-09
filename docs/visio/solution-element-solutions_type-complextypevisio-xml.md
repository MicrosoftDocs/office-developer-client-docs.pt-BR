---
title: Elemento Solution (Solutions_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Especifica uma instância da solução que XML armazenado no desenho.
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773032"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a>Elemento Solution (Solutions_Type complexType) ('Visio XML')

Especifica uma instância da solução que XML armazenado no desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Solutions.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Soluções](solutions-elementvisio-xml.md) <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |Armazena as propriedades das soluções armazenadas no documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Rel](rel-element-solution_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |Especifica a relação a uma parte com a solução que XML associada a essa solução.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Nome  <br/> |XSD: String  <br/> |obrigatório  <br/> |O nome da solução.  <br/> |Valores do tipo xsd: String.  <br/> |
   

