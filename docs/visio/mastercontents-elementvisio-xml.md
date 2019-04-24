---
title: Elemento MasterContents (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Especifica informações sobre as formas de um mestre em um desenho.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341353"
---
# <a name="mastercontents-element-visio-xml"></a>Elemento MasterContents (' Visio XML ')

Especifica informações sobre as formas de um mestre em um desenho. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[PageContents_Type](pagecontents_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Master #. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

Nenhum.
  
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Contém um elemento **Connect** para cada conexão entre duas formas em um desenho.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos **Shape** .  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhuma.
  

