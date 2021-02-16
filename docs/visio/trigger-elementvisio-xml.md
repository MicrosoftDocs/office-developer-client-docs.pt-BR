---
title: Elemento Trigger (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Fornece instruções ao Microsoft Visio para recalcular uma relação entre partes do documento em um arquivo do Visio.
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542902"
---
# <a name="trigger-element-visio-xml"></a>Elemento Trigger (XML do Visio)

Fornece instruções ao Microsoft Visio para recalcular uma relação entre partes do documento em um arquivo do Visio.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica os elementos da célula que fornecem informações para a definição de uma forma.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Define a estrutura DocumentSheet.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Representa um estilo definido em um documento.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associadas ao mestre.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associadas à página de desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma referência a uma página no desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |obrigatório  <br/> |O nome da fórmula a ser chamada quando o gatilho for ativado.  <br/> Consulte a seção Comentários.  <br/> |Valores do tipo xsd:string.  <br/> |
   
## <a name="remarks"></a>Comentários

O **atributo N** desse elemento **Trigger** deve ser um de um conjunto limitado de valores que correspondem às instruções de disparo. Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse **elemento Trigger.** 
  
|**Valor**|**Elemento pai**|**Descrição**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função HASCATEGORIES.**  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando existe uma referência entre partes usando uma **função BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página sempre que a página ou qualquer uma de suas formas contidas usa uma **função RGB.**  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando existe uma referência entre partes usando uma **função DOCCREATION.**  <br/> |
|RecalcData1  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função DATA1.**  <br/> |
|RecalcData2  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função DATA2.**  <br/> |
|RecalcData3  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função DATA3.**  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando existe uma referência entre partes usando uma **função DOCLASTEDIT.**  <br/> |
|RecalcID  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função de ID.**  <br/> |
|RecalcMasterName  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função MASTERNAME.**  <br/> |
|RecalcName  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função NAME.**  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página se a página ou qualquer uma de suas formas que contêm tiver uma **função NOW** ou **RAND.**  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando existe uma referência entre partes usando uma **função PAGECOUNT.**  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função PAGENAME.**  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando existe uma referência entre partes usando uma **função PAGENUMBER.**  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma função **POINTALONGPATH**, **PATHLENGTH** ou **PATHSEGMENT.**  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando existe uma referência entre partes usando uma **função DOCLASTPRINT.**  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando existe uma referência entre partes usando uma **função DOCLASTSAVE.**  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando existe uma referência entre partes usando uma função **CATEGORY**, **CREATOR**, **DESCRIPTION**, **KEYWORDS**, **SUBJECT** ou **TITLE.**  <br/> |
|RecalcType  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função TYPE.**  <br/> |
|RelChanged  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência entre partes usando uma **função CONTAINERMEMBERCOUNT.**  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando existe uma referência entre partes usando uma **função CONTAINERSHEETREF.**  <br/> |
|Path  <br/> |[Formato](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando existe uma referência entre partes usando uma função **POINTALONGPATH**, **PATHLENGTH** ou **PATHSEGMENT.**  <br/> |
   

