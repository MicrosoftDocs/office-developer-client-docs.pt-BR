---
title: Elemento REL (Solution_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Especifica uma relação a uma parte com a solução que XML associada a essa solução.
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772665"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a>Elemento REL (Solution_Type complexType) ('Visio XML')

Especifica uma relação a uma parte com a solução que XML associada a essa solução.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Solution](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |Especifica uma instância da solução que XML armazenado no desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|r: id  <br/> |XSD: String  <br/> Consulte os comentários.  <br/> |obrigatório  <br/> |Especifica uma relação a uma parte.  <br/> |"livrar #"  <br/> Consulte os comentários.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** . O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número. O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** . 
  
Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

