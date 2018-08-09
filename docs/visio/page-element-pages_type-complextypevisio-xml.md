---
title: Elemento de página (Pages_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Contém os elementos que definem uma página do documento.
ms.openlocfilehash: 368c50a25a09d5f4fd808f3f019b074b7f6d246d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772437"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Elemento de página (Pages_Type complexType) ('Visio XML')

Contém os elementos que definem uma página do documento.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Pages.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Contém os elementos de **página** do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Contém os elementos que definem a folha da página para um elemento de **página** .  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Background  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Um sinalizador que indica se a página é uma página de plano de fundo.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|BackPage  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação da página de plano de fundo nesta página.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se o nome tiver sido personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Indica se o nome universal foi personalizado pelo usuário.  <br/> |Valores do tipo xsd:Boolean.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |O nome do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |opcional  <br/> |O nome universal do elemento.  <br/> |Valores do tipo xsd: String.  <br/> |
|ReviewerID  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação do revisor associado com sobreposição de marcação.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD:Double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo modo de exibição (janela) pressupõe quando ele é aberto inicialmente.  <br/> |Valores do tipo xsd:double.  <br/> |
|ViewCenterY  <br/> |XSD:Double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo modo de exibição (janela) pressupõe quando ele é aberto inicialmente.  <br/> |Valores do tipo xsd:double.  <br/> |
|ViewScale  <br/> |XSD:Double  <br/> |opcional  <br/> |O fator de ampliação padrão para usar quando uma nova exibição (janela) da página é aberta. Por exemplo, 1 = 100%; 1,5 = 150% e assim por diante.  <br/> |Valores do tipo xsd:double.  <br/> |
   

