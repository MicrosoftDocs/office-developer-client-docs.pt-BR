---
title: Elemento SnapSettings (DocumentSettings_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Especifica os objetos que as formas ajustadas ajustar quando está ativo na janela.
ms.openlocfilehash: 0e784ddf9d5e04dae20a6a811557455c476b11a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773017"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>Elemento SnapSettings (DocumentSettings_Type complexType) ('Visio XML')

Especifica os objetos que as formas ajustadas ajustar quando está ativo na janela.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Document  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Contém os elementos que especificam as configurações do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

Nenhum.
  
## <a name="remarks"></a>Comentários

O valor pode ser uma soma dos valores na tabela a seguir.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Ajustar a nada.  <br/> |
|1  <br/> |Ajustar às subdivisões da régua.  <br/> |
|2  <br/> |Ajustar à grade.  <br/> |
|4  <br/> |Ajustar às guias.  <br/> |
|8  <br/> |Ajustar às alças de seleção.  <br/> |
|16  <br/> |Ajustar aos vértices.  <br/> |
|32  <br/> |Ajustar aos pontos de conexão.  <br/> |
|256  <br/> |Ajustar às bordas visíveis das formas.  <br/> |
|512  <br/> |Ajustar à caixa de alinhamento.  <br/> |
|1024  <br/> |Ajustar às opções de extensões da forma.  <br/> |
|32768  <br/> |Snap desabilitada.  <br/> |
|65536  <br/> |Ajustar às intersecções.  <br/> |
   

