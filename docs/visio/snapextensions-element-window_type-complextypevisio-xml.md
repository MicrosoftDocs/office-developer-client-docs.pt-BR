---
title: Elemento SnapExtensions (Window_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa. O valor pode ser uma soma dos valores na tabela a seguir.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540319"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>Elemento SnapExtensions (Window_Type complexType) (XML do Visio)

Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa. O valor pode ser uma soma dos valores na tabela a seguir.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Windows. xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Janela](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>Elementos filho

Nenhum.
  
### <a name="attributes"></a>Atributos

Nenhum
  
## <a name="remarks"></a>Comentários

O valor do elemento **SnapExtensions** pode ser uma soma dos valores na tabela a seguir. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |Ajustar a nada.  <br/> |
|1  <br/> |Ajustar à extensão da caixa de alinhamento.  <br/> |
|duas  <br/> |Ajustar à extensão do eixo central.  <br/> |
|quatro  <br/> |Ajustar à extensão da tangente da curva.  <br/> |
|8   <br/> |Ajustar à extensão do ponto de extremidade.  <br/> |
|dezesseis  <br/> |Ajustar à extensão intermediária.  <br/> |
|32  <br/> |Ajustar à extensão linear.  <br/> |
|64  <br/> |Ajustar à extensão da curva.  <br/> |
|128  <br/> |Ajustar à extensão perpendicular de ponto de extremidade.  <br/> |
|256  <br/> |Ajustar à extensão perpendicular de ponto central.  <br/> |
|512  <br/> |Ajustar à extensão horizontal do ponto de extremidade.  <br/> |
|1024  <br/> |Ajustar à extensão vertical do ponto de extremidade.  <br/> |
|2048  <br/> |Ajustar à extensão do centro da elipse.  <br/> |
|4096  <br/> |Ajuste à extensão de ângulos isométrica.  <br/> |
   

