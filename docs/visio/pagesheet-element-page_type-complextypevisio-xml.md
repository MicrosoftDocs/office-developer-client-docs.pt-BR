---
title: Elemento PageSheet (Page_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Especifica as propriedades da página de desenho associadas à página de desenho.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540620"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a>Elemento PageSheet (Page_Type complexType) (XML do Visio)

Especifica as propriedades da página de desenho associadas à página de desenho.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Contém elementos que definem uma página no documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica a ID da folha de estilos da qual será herdada a formatação de preenchimento. Deve ser o valor do **atributo ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica a ID da folha de estilos da qual será herdada a formatação de linha. Deve ser o valor do **atributo ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica a ID da folha de estilos da qual será herdada a formatação de texto. Deve ser o valor do **atributo ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:string.  <br/> |
   

