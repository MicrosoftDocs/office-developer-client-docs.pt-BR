---
title: Elemento REL (Page_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Especifica uma relação a uma parte com a XML da página correspondente.
ms.openlocfilehash: 9fc42527d311faa66b0b4041a0f978818ee84595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772663"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a>Elemento REL (Page_Type complexType) ('Visio XML')

Especifica uma relação a uma parte com a XML da página correspondente.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Pages.XML, masters.xml, recordsets.xml,. XML n º de página, mestre. XML de #  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Especifica uma instância da página que XML armazenado no desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|r: id  <br/> |XSD: String  <br/> Consulte os comentários.  <br/> |obrigatório  <br/> |Especifica uma relação a uma parte.  <br/> |"livrar #"  <br/> Consulte os comentários.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor do atributo **id de r:** deve ser um tipo de **ST_RelationshipID** . O tipo de **ST_RelationshipID** é uma cadeia de caracteres que deve estar no formato 'eliminar #', onde o caractere final deve ser um número. O número deve ser exclusivo entre todos os elementos filho do elemento **Rel** . 
  
Para obter mais informações sobre o tipo de ST_RelationshipID, consulte a [especificação de ISO/IEC 29500 parte 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

