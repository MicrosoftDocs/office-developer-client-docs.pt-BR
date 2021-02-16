---
title: Elemento Window (Windows_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Representa uma janela aberta em uma instância do Microsoft Visio. Esse elemento contém as informações necessárias para criar exatamente uma janela da interface do usuário no espaço de trabalho do aplicativo quando o arquivo é inicialmente aberto pelo Visio.
ms.openlocfilehash: 2700ee7a9a17460f6ac707f5b1a8f35d622e33e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538456"
---
# <a name="window-element-windows_type-complextype-visio-xml"></a>Elemento Window (Windows_Type complexType) (Visio XML)

Representa uma janela aberta em uma instância do Microsoft Visio. Esse elemento contém as informações necessárias para criar exatamente uma janela da interface do usuário no espaço de trabalho do aplicativo quando o arquivo é inicialmente aberto pelo Visio.
  
## <a name="element-information"></a>Informações de elemento

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contém os **elementos Window** de um documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica se o recurso de grade dinâmica está habilitado para um documento ou janela.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica os objetos que definem a associação quando ela está habilitada no documento.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Especifica se os pontos de conexão são mostrados em uma janela.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Especifica se uma grade é mostrada na janela de desenho.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Especifica se as guias são mostradas na janela de desenho.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Especifica se as quebras de página são mostradas em uma janela.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Especifica se as réguas são mostradas na janela de desenho.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contém um conjunto de elementos **SnapAngle**.  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica se uma configuração de extensão de ajuste específica está habilitada ou desabilitada da janela ativa.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica os objetos que definem o ajuste quando ele está ativo na janela.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Especifica o grupo de janelas de estêncil mescladas do qual a janela é membro.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contém um inteiro que especifica a posição relativa de um estêncil dentro de um grupo em uma janela.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Especifica a largura do controle guia de página de uma janela de desenho (como uma fração da largura total da janela de desenho).  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Contêiner  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |ID do contêiner: Página, Planilha ou Mestre. Relevante e necessário somente se **ContainerType** for especificado.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |opcional  <br/> |Pode ser um dos seguintes valores: Documento, Página ou Mestre. Relevante somente quando **WindowType** é especificado como Desenho ou Planilha.  <br/> |Valores do tipo xsd:token.  <br/> |
|Document  <br/> |xsd:string  <br/> |opcional  <br/> |Caminho do arquivo do documento exibido nesta janela.  <br/> |Valores do tipo xsd:string.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |ID mestra se esta janela estiver exibindo um mestre.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Page  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |ID da página se essa janela estiver exibindo uma página. Relevante somente quando **WindowType** é especificado como Drawing e **ContainerType** é especificado como Page.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |ID da janela na qual essa janela de estêncil está contida. Relevante somente quando **WindowType** é especificado como estêncil.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |xsd:boolean  <br/> |opcional  <br/> |Sinalizador somente leitura se esse estêncil não for um estêncil de documento.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Planilha  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |ID da planilha no contêiner. Relevante somente quando o contêiner é especificado como Planilha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo ponto de exibição (janela) assume quando é aberto inicialmente.  <br/> |Valores do tipo xsd:double.  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo ponto de exibição (janela) assume quando é aberto inicialmente.  <br/> |Valores do tipo xsd:double.  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |opcional  <br/> |O fator de ampliação padrão a ser usado quando um novo modo de exibição (janela) da página é aberto. Por exemplo, 1 = 100%; 1,5 = 150% e assim por diante.  <br/> |Valores do tipo xsd:double.  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Altura do retângulo da janela.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |opcional  <br/> |Coordenada esquerda do retângulo da janela.  <br/> |Valores do tipo xsd:short.  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Um inteiro especificando sinalizadores de bits.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |opcional  <br/> |Coordenada superior do retângulo da janela.  <br/> |Valores do tipo xsd:short.  <br/> |
|WindowType  <br/> |xsd:token  <br/> |obrigatório  <br/> |Um valor enumerado que pode ser um dos seguintes: Desenho, Planilha, Estêncil ou Ícone.  <br/> |Valores do tipo xsd:token.  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Largura do retângulo da janela.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

