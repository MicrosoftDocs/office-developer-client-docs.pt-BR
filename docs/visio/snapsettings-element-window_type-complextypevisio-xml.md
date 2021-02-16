---
title: Elemento SnapSettings (Window_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Especifica os objetos que definem o ajuste quando ele está ativo na janela.
ms.openlocfilehash: 0fbe54f56f79d84e6c6bd8ddc11aa28b7e5ba1dc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540312"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a>Elemento SnapSettings (Window_Type complexType) (XML do Visio)

Especifica os objetos que definem o ajuste quando ele está ativo na janela.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |windows.xml  <br/> |
   
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
|0  <br/> |Ajustar a nada.  <br/> |
|1   <br/> |Ajustar às subdivisões de régua.  <br/> |
|2   <br/> |Ajustar à grade.  <br/> |
|4   <br/> |Ajustar às guias.  <br/> |
|8   <br/> |Ajustar às alças de seleção.  <br/> |
|16   <br/> |Ajustar aos vértices.  <br/> |
|32  <br/> |Ajustar aos pontos de conexão.  <br/> |
|256  <br/> |Ajustar às bordas visíveis das formas.  <br/> |
|512  <br/> |Ajustar à caixa de alinhamento.  <br/> |
|1024  <br/> |Ajustar às opções de extensões da forma.  <br/> |
|32768  <br/> |Ajustar desabilitado.  <br/> |
|65536  <br/> |Ajustar às interseções.  <br/> |
   

