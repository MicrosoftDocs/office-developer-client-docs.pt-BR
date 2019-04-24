---
title: Elemento PageSheet (Master_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Especifica as propriedades da página de desenho associada ao mestre.
ms.openlocfilehash: 579b2b4f02c79a38842a150b8757329e19e7bb3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361121"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>Elemento PageSheet (Master_Type complexType) (' Visio XML ')

Especifica as propriedades da página de desenho associada ao mestre.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Masters. xml  <br/> |
   
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
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Especifica um mestre em um desenho.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica a identificação da folha de estilos a partir da qual a formatação de preenchimento será herdada. DEVE ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica a identificação da folha de estilos da qual herdar a formatação de linha. DEVE ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Especifica a identificação da folha de estilos a partir da qual a formatação de texto será herdada. DEVE ser o valor do atributo **ID** associado a um **StyleSheet_Type** no desenho.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |opcional  <br/> |A identificação exclusiva do elemento no seu elemento pai.  <br/> |Valores do tipo xsd:string.  <br/> |
   

