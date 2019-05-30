---
title: Elemento de página (Pages_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contém elementos que definem uma página no documento.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538022"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Elemento de página (Pages_Type complexType) (XML do Visio)

Contém elementos que definem uma página no documento.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Pages. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contém os elementos de **página** do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contém elementos que definem a folha de página de um elemento de **página** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Tela de fundo  <br/> |xsd:boolean  <br/> |opcional  <br/> |Um sinalizador que indica se a página é uma página de plano de fundo.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID da página de plano de fundo desta página.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A identificação exclusiva do elemento no seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se o nome foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |opcional  <br/> |Indica se o nome Universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd:string.  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID do revisor associado com a sobreposição de marcação.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo modo de exibição (janela) assume quando é aberto inicialmente.  <br/> |Valores do tipo xsd: Double.  <br/> |
|ViewCenterY  <br/> |xsd: Double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo modo de exibição (janela) assume quando é aberto inicialmente.  <br/> |Valores do tipo xsd: Double.  <br/> |
|ViewScale  <br/> |xsd: Double  <br/> |opcional  <br/> |O fator de ampliação padrão a ser usado quando um novo modo de exibição (janela) da página é aberto. Por exemplo, 1 = 100%; 1,5 = 150%, e assim por diante.  <br/> |Valores do tipo xsd: Double.  <br/> |
   

