---
title: Elemento SnapSettings (Window_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica os objetos que definem o ajuste quando ele está ativo na janela.
ms.openlocfilehash: b4793c6d9c13a922db4d3ed9504a3a08e933230a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334500"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>Elemento SnapSettings (Window_Type complexType) (' Visio XML ')

Especifica os objetos que definem o ajuste quando ele está ativo na janela.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Windows. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Janela](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Representa uma janela aberta em uma instância do Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

Nenhum.
  
## <a name="remarks"></a>Comentários

O valor pode ser uma soma dos valores na tabela a seguir.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Ajustar a nada.  <br/> |
|1  <br/> |Ajustar às subdivisões da régua.  <br/> |
|duas  <br/> |Ajustar à grade.  <br/> |
|quatro  <br/> |Ajustar às guias.  <br/> |
|8  <br/> |Ajustar às alças de seleção.  <br/> |
|dezesseis  <br/> |Ajustar aos vértices.  <br/> |
|32  <br/> |Ajustar aos pontos de conexão.  <br/> |
|256  <br/> |Ajustar às bordas visíveis das formas.  <br/> |
|512  <br/> |Ajustar à caixa de alinhamento.  <br/> |
|1024  <br/> |Ajustar às opções de extensões da forma.  <br/> |
|32768  <br/> |Snap desabilitado.  <br/> |
|65536  <br/> |Ajustar às interseções.  <br/> |
   

