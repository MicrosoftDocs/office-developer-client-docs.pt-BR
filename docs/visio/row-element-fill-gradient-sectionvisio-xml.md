---
title: Elemento Row (seção Fill Gradient) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.
ms.openlocfilehash: 55ec3b58f57d1fb008825c1a5a4156e5aec59552
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358515"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a>Elemento Row (seção Fill Gradient) (' Visio XML ')

Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.
  
## <a name="element-information"></a>Informações do elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Contém a cor, transparência e posição de uma marca de gradiente para um gradiente de preenchimento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Cell](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Especifica uma única propriedade.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |opcional  <br/> |Especifica se uma linha que seria herdada de uma forma mestra foi excluída.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica o identificador baseado em um da linha. Ele deve ser unqiue e maior que outros identificadores na mesma seção. O atributo IX é usado somente para as seções caractere, conexão, campo, FillGradient, geometria, camada, LineGradient, parágrafo, revisor, rabisco e guias. Uma linha pode ter apenas um dos atributos IX ou N.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome exclusivo dependente de idioma da linha.  <br/> |Valores do tipo xsd:string.  <br/> |
|N  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o nome exclusivo independente do idioma da linha. O atributo N é usado apenas para as seções usuário, propriedade, ações, controle, conexão, hiperlink e ActionTag. Uma linha pode ter apenas um dos atributos IX ou N.  <br/> |Valores do tipo xsd:string.  <br/> |
|T  <br/> |xsd:string  <br/> |opcional  <br/> |Especifica o tipo de caminho geométrico representado pela linha e usado na visualização de geometria. O atributo T é usado apenas para a seção Geometry.  <br/> |Valores do tipo xsd:string.  <br/> |
   

