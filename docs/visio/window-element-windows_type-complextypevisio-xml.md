---
title: Elemento da janela (Windows_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: >-
  Representa uma janela aberta em uma estância do Microsoft Visio.
   Esse elemento contém as informações necessárias para recriar exatamente uma janela de interface de usuário no espaço de trabalho do aplicativo quando o arquivo é aberto inicialmente pelo Visio.
ms.openlocfilehash: 762b689d625c7865696a0bf8bb8c4acc25e3d8eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773287"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Elemento da janela (Windows_Type complexType) ('Visio XML')

Representa uma janela aberta em uma estância do Microsoft Visio.
 Esse elemento contém as informações necessárias para recriar exatamente uma janela de interface de usuário no espaço de trabalho do aplicativo quando o arquivo é aberto inicialmente pelo Visio.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Windows.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Contém os elementos de **janela** para um documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Especifica se o recurso de grade dinâmica está habilitado para um documento ou janela.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Especifica os objetos que formas coladas a quando a colagem está habilitada no documento.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Especifica se os pontos de conexão são exibidos em uma janela.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Especifica se uma grade é mostrada na janela de desenho.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Especifica se as guias são exibidos na janela de desenho.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Especifica se as quebras de página são exibidas em uma janela.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Especifica se as réguas são exibidas na janela de desenho.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Contém uma coleção de elementos de **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Especifica se uma configuração de extensão de snap específico está habilitada ou desabilitada para a janela ativa.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Especifica os objetos que as formas ajustadas ajustar quando está ativo na janela.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Especifica o grupo do windows de estêncil mesclado do qual a janela é um membro.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Contém um número inteiro que especifica a posição relativa de um estêncil dentro de um grupo em uma janela.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Especifica a largura do controle guia página de uma janela de desenho (como uma fração da largura total da janela de desenho).  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |ID do contêiner: página, mestre ou planilha. Somente relevantes e necessário se **ContainerType** for especificado.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |XSD:token  <br/> |opcional  <br/> |Pode ser um dos seguintes valores: documento, página ou mestre. Relevante apenas quando **WindowType** é especificado como o desenho ou planilha.  <br/> |Valores do tipo xsd:token.  <br/> |
|Document  <br/> |XSD: String  <br/> |opcional  <br/> |Caminho de arquivo do documento exibido nessa janela.  <br/> |Valores do tipo xsd: String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A ID exclusiva do elemento dentro de seu elemento pai.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |ID do mestre se esta janela estiver exibindo um mestre.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Page  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |ID da página se esta janela estiver exibindo uma página. Relevante apenas quando o **WindowType** é especificado como o desenho e **ContainerType** é especificado como página.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |ID da janela em que essa janela estêncil está contida. Relevante somente quando **WindowType** é especificado como o estêncil.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Sinalizador de somente leitura se este estêncil não for um estêncil do documento.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|Planilha  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |ID da folha no contêiner. Relevante somente quando o contêiner é especificado como folha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD:Double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo modo de exibição (janela) pressupõe quando ele é aberto inicialmente.  <br/> |Valores do tipo xsd:double.  <br/> |
|ViewCenterY  <br/> |XSD:Double  <br/> |opcional  <br/> |**ViewCenterX** e **ViewCenterY** especificam um ponto central em uma página que um novo modo de exibição (janela) pressupõe quando ele é aberto inicialmente.  <br/> |Valores do tipo xsd:double.  <br/> |
|ViewScale  <br/> |XSD:Double  <br/> |opcional  <br/> |O fator de ampliação padrão para usar quando uma nova exibição (janela) da página é aberta. Por exemplo, 1 = 100%; 1,5 = 150% e assim por diante.  <br/> |Valores do tipo xsd:double.  <br/> |
|WindowHeight  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Altura do retângulo janela.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |XSD:Short  <br/> |opcional  <br/> |Coordenada esquerda do retângulo janela.  <br/> |Valores do tipo xsd:short.  <br/> |
|WindowState  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Um inteiro especificando sinalizadores de bit.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |XSD:Short  <br/> |opcional  <br/> |Coordenada superior do retângulo janela.  <br/> |Valores do tipo xsd:short.  <br/> |
|WindowType  <br/> |XSD:token  <br/> |obrigatório  <br/> |Um valor enumerado que pode ser uma das seguintes opções: ícone, planilha, estêncil ou desenho.  <br/> |Valores do tipo xsd:token.  <br/> |
|WindowWidth  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Largura do retângulo janela.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
   

