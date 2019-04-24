---
title: Elemento SnapAngles (Window_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5997f374-303a-92b6-6dd3-87ef81104af4
description: Contém um conjunto de elementos SnapAngle.
ms.openlocfilehash: 09a975b280a99fdc2535503b587efdd2143cf18b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334633"
---
# <a name="snapangles-element-windowtype-complextype-visio-xml"></a>Elemento SnapAngles (Window_Type complexType) (' Visio XML ')

Contém um conjunto de elementos **SnapAngle**. 
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Windows. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Janela](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Representa uma janela aberta em uma instância do Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[SnapAngle](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[SnapAngle_Type](snapangle_type-complextypevisio-xml.md) <br/> |Contém um número de ponto flutuante que especifica um ângulo de encaixe em graus.  <br/> |
   
### <a name="attributes"></a>Atributos

Nenhum.
  

