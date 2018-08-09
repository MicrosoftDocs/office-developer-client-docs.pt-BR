---
title: Elemento CommentEntry (CommentList_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica as propriedades usadas para identificar um comentário em um desenho.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771535"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Elemento CommentEntry (CommentList_Type complexType) ('Visio XML')

Especifica as propriedades usadas para identificar um comentário em um desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Comments.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Especifica os comentários em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Um valor baseado em um que identifica o autor.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|CommentID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Um valor exclusivo que identifica o comentário em uma página de desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Date  <br/> |XSD: DateTime  <br/> |obrigatório  <br/> |Especifica que um comentário foi criado.  <br/> |Valores do tipo xsd: DateTime.  <br/> |
|Concluído  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Especifica o estado atual do comentário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|EditDate  <br/> |XSD: DateTime  <br/> |opcional  <br/> |Especifica quando um comentário foi alterada pela última vez.  <br/> |Valores do tipo xsd: DateTime.  <br/> |
|PageID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |Um valor que identifica a página de desenho o comentário é no.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Identificação da forma  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Um valor que identifica de forma que o comentário é no. Se nenhuma identificação da forma for especificada, o comentário refere-se à página de desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

