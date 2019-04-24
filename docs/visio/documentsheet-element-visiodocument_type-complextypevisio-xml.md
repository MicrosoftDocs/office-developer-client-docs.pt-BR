---
title: Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Especifica uma estrutura DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356361"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>Elemento DocumentSheet (VisioDocument_Type complexType) ('Visio XML')

Especifica uma estrutura DocumentSheet.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |O elemento raiz de um documento do Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma célula em uma DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|IsCustomName  <br/> |xsd:boolean  <br/> |opcional  <br/> |Descreve se o nome foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |opcional  <br/> |Descreve se o nome universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome dependente de idioma da DocumentSheet.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome independente de idioma da DocumentSheet.  <br/> |Valores do tipo xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |Cadeia de caracteres opcional. Um GUID (identificador global exclusivo) que identifica a forma.  <br/> |Valores do tipo xsd:string.  <br/> |
   

