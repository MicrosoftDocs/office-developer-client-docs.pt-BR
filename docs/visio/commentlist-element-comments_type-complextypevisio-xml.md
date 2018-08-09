---
title: Elemento CommentList (Comments_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica os comentários em um desenho.
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771540"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a>Elemento CommentList (Comments_Type complexType) ('Visio XML')

Especifica os comentários em um desenho.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Comments.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Coment�rios](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |Especifica as propriedades usadas para identificar os autores e comentários em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[CommentEntry](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |Especifica as propriedades usadas para identificar um comentário em um desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum.
  

