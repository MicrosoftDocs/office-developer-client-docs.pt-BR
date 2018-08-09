---
title: Elemento AuthorEntry (AuthorList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica as propriedades usadas para identificar o autor de um comentário em um desenho.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771281"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Elemento AuthorEntry (AuthorList_Type complexType) ('Visio XML')

Especifica as propriedades usadas para identificar o autor de um comentário em um desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Comments.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Especifica os autores em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Um valor baseado em um que identifica o autor.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Initials  <br/> |XSD: String  <br/> |opcional  <br/> |As iniciais do autor.  <br/> |Valores do tipo xsd: String.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |O nome do autor.  <br/> |Valores do tipo xsd: String.  <br/> |
|ResolutionID  <br/> |XSD: String  <br/> |opcional  <br/> |Um identificador exclusivo para o autor.  <br/> |Valores do tipo xsd: String.  <br/> |
   

