---
title: Elemento AuthorEntry (AuthorList_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica propriedades usadas para identificar o autor de um comentário em um desenho.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537903"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>Elemento AuthorEntry (AuthorList_Type complexType) (XML do Visio)

Especifica propriedades usadas para identificar o autor de um comentário em um desenho.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Especifica os autores em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |Valor baseado em um que identifica o autor.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Initials  <br/> |xsd:string  <br/> |opcional  <br/> |As iniciais do autor.  <br/> |Valores do tipo xsd:string.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |O nome do autor.  <br/> |Valores do tipo xsd:string.  <br/> |
|ResolutionID  <br/> |xsd:string  <br/> |opcional  <br/> |Um identificador exclusivo do usuário.  <br/> |Valores do tipo xsd:string.  <br/> |
   

