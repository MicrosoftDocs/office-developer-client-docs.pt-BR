---
title: Elemento CommentList (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica os comentários em um desenho.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395165"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a>Elemento CommentList (Comments_Type complexType) ('Visio XML')

Especifica os comentários em um desenho.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Comments](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |Especifica propriedades usadas para identificar os autores e comentários em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[CommentEntry](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |Especifica propriedades usadas para identificar um comentário em um desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum
  

