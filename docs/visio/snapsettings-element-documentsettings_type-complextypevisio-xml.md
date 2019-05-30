---
title: Elemento SnapSettings (DocumentSettings_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Especifica os objetos que definem o ajuste quando ele está ativo na janela.
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540291"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>Elemento SnapSettings (DocumentSettings_Type complexType) (XML do Visio)

Especifica os objetos que definem o ajuste quando ele está ativo na janela.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |document.xml  <br/> |
   
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
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contém elementos que especificam configurações de documentos.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

Nenhum
  
## <a name="remarks"></a>Comentários

O valor pode ser uma soma dos valores na tabela a seguir.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Ajustar a nada.  <br/> |
|1  <br/> |Ajustar às subdivisões da régua.  <br/> |
|duas  <br/> |Ajustar à grade.  <br/> |
|quatro  <br/> |Ajustar às guias.  <br/> |
|8   <br/> |Ajustar às alças de seleção.  <br/> |
|dezesseis  <br/> |Ajustar aos vértices.  <br/> |
|32  <br/> |Ajustar aos pontos de conexão.  <br/> |
|256  <br/> |Ajustar às bordas visíveis das formas.  <br/> |
|512  <br/> |Ajustar à caixa de alinhamento.  <br/> |
|1024  <br/> |Ajustar às opções de extensões da forma.  <br/> |
|32768  <br/> |Snap desabilitado.  <br/> |
|65536  <br/> |Ajustar às interseções.  <br/> |
   

