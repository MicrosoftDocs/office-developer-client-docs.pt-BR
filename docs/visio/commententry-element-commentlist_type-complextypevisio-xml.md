---
title: Elemento CommentEntry (CommentList_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica propriedades usadas para identificar um comentário em um desenho.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540109"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>Elemento CommentEntry (CommentList_Type complexType) (XML do Visio)

Especifica propriedades usadas para identificar um comentário em um desenho.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Especifica os comentários em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Valor baseado em um que identifica o autor.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Um valor exclusivo que identifica o comentário em uma página de desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Data  <br/> |xsd:dateTime  <br/> |obrigatório  <br/> |Especifica quando um comentário foi criado.  <br/> |Valores do tipo xsd:dateTime.  <br/> |
|Done  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica o estado atual do comentário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |opcional  <br/> |Especifica quando um comentário foi alterado pela última vez.  <br/> |Valores do tipo xsd:dateTime.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Um valor que identifica a página de desenho em que o comentário está ativo.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Um valor que identifica a forma em que o comentário está. Se nenhum ShapeID for especificado, o comentário se refere à página de desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

