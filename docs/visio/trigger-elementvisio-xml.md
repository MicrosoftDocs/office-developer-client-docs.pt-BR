---
title: Elemento Trigger ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.
ms.openlocfilehash: 909fff3ccec176cd3ce327fc208c176a68764fe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773190"
---
# <a name="trigger-element-visio-xml"></a>Elemento Trigger ('Visio XML')

Fornece instruções para o Microsoft Visio recalcular uma relação entre as partes de documentos em um arquivo do Visio.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |# XML do mestre, página # XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Especifica os elementos de célula que fornecem informações para a definição de uma forma.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Define a estrutura DocumentSheet.  <br/> |
|[Folha de estilos](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Representa um estilo definido em um documento.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associados com o mestre.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Especifica as propriedades da página de desenho associado à página de desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Especifica uma página de toa referência no desenho.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |XSD: String  <br/> |obrigatório  <br/> |O nome da fórmula a ser chamado quando o gatilho é ativado.  <br/> Consulte a seção comentários.  <br/> |Valores do tipo xsd: String.  <br/> |
   
## <a name="remarks"></a>Comentários

O atributo **N** deste elemento **gatilho** deve ser um conjunto limitado de valores que correspondem aos gatilho instruções. Consulte a tabela abaixo para determinar os valores do atributo **N** que são permitidos para esse elemento **gatilho** . 
  
|**Valor**|**Elemento pai**|**Descrição**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando uma função **HASCATEGORIES** existe.  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Existe um gatilho que aparece em uma página quando uma referência cruzada partes usando uma função **BKGPAGENAME**  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página sempre que a página ou qualquer uma das suas formas contidas usa uma função **RGB** .  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando uma referência cruzada partes usando uma função **DOCCREATION** existe.  <br/> |
|RecalcData1  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência cruzada partes usando uma função **DATA1** .  <br/> |
|RecalcData2  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência cruzada partes usando uma função **DATA2** .  <br/> |
|RecalcData3  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando existe uma referência cruzada partes usando uma função **DATA3** .  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando uma referência cruzada partes usando uma função **DOCLASTEDIT** existe.  <br/> |
|RecalcID  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando uma **ID** de função existe.  <br/> |
|RecalcMasterName  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando uma função **MASTERNAME** existe.  <br/> |
|RecalcName  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando um **nome** de função existe.  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página, se a página ou em qualquer uma das suas formas contendo tiver um **agora** ou uma função **RAND** .  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando uma referência cruzada partes usando uma função **PAGECOUNT** existe.  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando uma função **PAGENAME** existe.  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando uma referência cruzada partes usando uma função **PAGENUMBER** existe.  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando uma função **POINTALONGPATH**, **PATHLENGTH**ou **PATHSEGMENT** existe.  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando uma referência cruzada partes usando uma função **DOCLASTPRINT** existe.  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando uma referência cruzada partes usando uma função **DOCLASTSAVE** existe.  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em um documento quando uma referência cruzada partes usando uma função de **categoria**, **criador**, **Descrição**, **palavras-chave**, **assunto**ou **título** existe.  <br/> |
|RecalcType  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando um **tipo** de função existe.  <br/> |
|RelChanged  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma forma quando uma referência cruzada partes usando uma função **CONTAINERMEMBERCOUNT** existe.  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando uma referência cruzada partes usando uma função **CONTAINERSHEETREF** existe.  <br/> |
|Path  <br/> |[Forma](shape-element-shapes_type-complextypevisio-xml.md) <br/> |Um gatilho que aparece em uma página quando uma referência cruzada partes usando uma função **POINTALONGPATH**, **PATHLENGTH**ou **PATHSEGMENT** existe.  <br/> |
   

