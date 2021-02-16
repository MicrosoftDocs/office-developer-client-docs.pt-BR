---
title: Novo no Visio para desenvolvedores
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: Este documento fornece uma exibição de nível superior dos aprimoramentos e adições para desenvolvedores no Visio 2013. Para desenvolvedores que estão prontos para começar a trabalhar na plataforma visio, ele fornece detalhes suficientes para começar a codificar contra o Visio 2013.
ms.openlocfilehash: df4bc1fa493ee3976c99802400ee52691d05d20a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319814"
---
# <a name="new-in-visio-for-developers"></a>Novo no Visio para desenvolvedores

Este documento fornece uma exibição de nível superior dos aprimoramentos e adições para desenvolvedores no Visio 2013. Para desenvolvedores que estão prontos para começar a trabalhar na plataforma visio, ele fornece detalhes suficientes para começar a codificar contra o Visio 2013.
  
## <a name="introduction"></a>Introdução
<a name="vis15_WhatsNew_Intro"> </a>

O Visio 2013 fornece uma plataforma única e poderosa para suas soluções de desenho personalizadas. Novos objetos, coleções, propriedades, métodos, enumerações e eventos, junto com novas células e funções ShapeSheet, oferecem a você mais opções para a definição do comportamento dos elementos em suas soluções.
  
Entre os novos recursos de interesse para desenvolvedores no Visio 2013 estão o novo formato de arquivo; atualizações robustas para temas; alterar o recurso de forma (permitindo que você substitua formas por outro); novos efeitos de forma; melhorias de comentário; coautor no SharePoint Server 2013; recorte de imagem personalizável; geometria relativa; suporte para dados do Business Connectivity Services (BCS); atualizações dos Serviços do Visio no Microsoft SharePoint Server 2013; e um recurso de página duplicado. Este tópico oferece um breve resumo de cada um desses recursos e menciona alguns dos novos objetos e membros do Visio associados aos recursos e expostos no Visual Basic for Applications (VBA). Para obter informações sobre esses recursos e exemplos de código de acompanhamento, consulte a Central de Desenvolvedores do [Visio.](https://msdn.microsoft.com/office/aa905478.aspx)
  
> [!NOTE]
> O Visio 2013 inclui muitas células, linhas e funções do ShapeSheet novas para dar suporte aos novos recursos no Visio. For more information about what's new in the ShapeSheet for Visio 2013, see the article [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md). 
  
## <a name="new-file-format"></a>Novo formato de arquivo
<a name="vis15_WhatsNew_NewFF"> </a>

O Visio 2013 apresenta um novo formato de arquivo, com base no padrão Open Packaging Conventions (OPC) (ISO 29500, Parte 2) e os elementos XML do formato de arquivo anterior XML do Visio (.vdx). É um formato de arquivo recortado baseado em XML semelhante aos formatos de arquivo usados em outros aplicativos.
  
Como o novo formato de arquivo é suportado pelos Serviços do Visio 2013 e do Visio no Microsoft SharePoint Server 2013, você pode salvar um desenho do Visio diretamente em uma biblioteca do SharePoint Server, sem precisar publicar o arquivo como um Desenho da Web do Visio (.vdw). Mesmo assim, os Serviços do Visio ainda podem ler e exibir arquivos de Desenho da Web do Visio.
  
O novo formato de arquivo inclui os tipos de arquivo a seguir (por extensão):
  
- . vsdx (desenho do Visio)
    
- . vsdm (desenho habilitados para macro do Visio)
    
- vssx (estêncil do Visio)
    
- . vssm (estêncil habilitados para macro do Visio)
    
- . vstx (modelo do Visio)
    
- . vstm (modelo habilitado para macro do Visio)
    
Usando o suporte existente para leitura e escrita no pacote de formato de arquivo (como [System.IO.Packaging)](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) e para análise de XML ( [System.Xml. Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ), você pode trabalhar programaticamente com os novos formatos de arquivo. 
  
O Visio 2013 mantém a capacidade de ler os formatos de arquivo antigos (.vsd, .vss, .vst, .vdx, .vsx, .vtx, .vdw, .vwi). O Visio 2013 não salva no formato de arquivo XML anterior do Visio (.vdx). As soluções ou ferramentas que consomem os arquivos de formato de arquivo XML anterior do Visio (.vdx) talvez precisem ser refatoradas para ler o novo formato de arquivo e seus esquemas.
  
Visio Services mantém a capacidade de exibir o formato de desenho da Web do Visio (. vdw) no navegador. Ele agora também processa as novas Visio desenho (. vsdx) e os formatos Visio habilitado para macro desenho (. vsdm).
  
## <a name="themes"></a>Temas
<a name="vis15_WhatsNew_Themes"> </a>

Os temas foram reprojetados no Visio 2013, utilizando uma variedade maior de efeitos e estilos, incluindo a integração de efeitos de Shape Art. Agora, os usuários decidem sobre um estilo abrangente ao aplicar um tema, personalizam o diagrama com variantes de tema e realçam formas individuais com os Estilos Rápidos. Os desenvolvedores de ShapeSheet podem aproveitar as vantagens desses recursos com as novas funções e células no ShapeSheet.
  
Você também pode manipular temas no nível do objeto [Page](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx), [Shape](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) e [Selection](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx). As novas APIs para o trabalho com temas incluem o método [Page.SetTheme](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx), o método [Page.SetThemeVariant](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx), o método [Shape.SetQuickStyle](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) e o método [Selection.SetQuickStyle](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx). 
  
Para uma lista detalhada das novas APIs no Visio 2013, consulte a seção de alterações do modelo de objeto do [Visio](#vis15_WhatsNew_NewOM) neste artigo. Para obter mais informações sobre as novas células ShapeSheet no Visio 2013, consulte o artigo Novidades para desenvolvedores do [Visio ShapeSheet.](what-s-new-for-visio-shapesheet-developers.md)
  
## <a name="change-shape"></a>Alterar forma
<a name="vis15_WhatsNew_ChangeShapes"> </a>

O Visio 2013 inclui uma API de substituição de forma que permite trocar uma ou mais formas por outra forma contida em um estêncil, mantendo alguns dos valores locais da forma original, como a forma de texto da forma, os dados da forma ou a formatação da forma. Os desenvolvedores de forma podem atualizar as configurações do ShapeSheet das formas personalizadas para especificar o comportamento de Alterar Forma para as formas. Entre as novas APIs, estão os métodos [Shape.ReplaceShapes](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) e [Selection.ReplaceShapes](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) e o evento [ReplaceShape](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx). 
  
Para uma lista detalhada das novas APIs no Visio 2013, consulte a seção de alterações do modelo de objeto do [Visio](#vis15_WhatsNew_NewOM) neste artigo. Para obter mais informações sobre as novas células ShapeSheet no Visio 2013, consulte o artigo Novidades para desenvolvedores do [Visio ShapeSheet.](what-s-new-for-visio-shapesheet-developers.md)
  
## <a name="shape-effects"></a>Efeitos de forma
<a name="vis15_WhatsNew_ShapeEffects"> </a>

Novos efeitos de forma como o bisel, rotação 3-D, brilho, reflexo e esboço foram adicionados ao Visio 2013. O ShapeSheet inclui novas células para trabalhar com esses efeitos.
  
Para obter mais informações sobre as novas células ShapeSheet no Visio 2013, consulte o artigo Novidades para desenvolvedores do [Visio ShapeSheet.](what-s-new-for-visio-shapesheet-developers.md)
  
## <a name="commenting"></a>Comentários
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 inclui uma nova estrutura de comentário. Comentários agora podem ser associados uma determinada forma ou página. O Visio 2013 inclui dois novos objetos, [Comentários](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) e [Comentário.](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) As novas APIs para acessar comentários programaticamente incluem as propriedades [Document.Comments](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx), [Page.Comments](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx), [Shape.Comments](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) e [Page.ShapeComments](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx). 
  
Os Serviços do Visio incluem APIs JavaScript para ler os comentários de uma página ou forma em um diagrama.
  
Para uma lista detalhada das novas APIs no Visio 2013, consulte a seção de alterações do modelo de objeto do [Visio](#vis15_WhatsNew_NewOM) neste artigo. 
  
> [!NOTE]
> Os comentários não podem mais ser acessados por meio do ShapeSheet. 
  
## <a name="coauthoring"></a>Coautoria
<a name="vis15_WhatsNew_Coauthoring"> </a>

O Visio 2013 inclui a capacidade de coautor de diagramas armazenados no SharePoint ou no Microsoft OneDrive. Os desenvolvedores têm acesso ao evento [Document.AfterDocumentMerge](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx), que oferece informações sobre alterações de diagrama devido à coautoria. Os desenvolvedores de solução também têm a capacidade de desabilitar a coautoria para o ajuste às necessidades personalizadas usando a célula [NoCoauth](nocoauth-cell-document-properties-section.md) no ShapeSheet do Documento. 
  
Para uma lista detalhada das novas APIs no Visio 2013, consulte a seção de alterações do modelo de objeto do [Visio](#vis15_WhatsNew_NewOM) neste artigo. 
  
## <a name="customizable-image-clipping"></a>Recortes de imagem personalizáveis
<a name="vis15_WhatsNew_ClipImages"> </a>

O Visio 2013 suporta a definição de um caminho para Recortes de imagem personalizáveis para cortar as imagens em qualquer forma. Isso estende os recursos do Visio 2010, que suportava o recorte de imagens de forma retangular. Essa funcionalidade está disponível no ShapeSheet usando a célula [ClippingPath](clippingpath-cell-foreign-image-info-section.md) na seção **Foreign Image Info**. 
  
Para obter mais informações sobre as novas células ShapeSheet no Visio 2013, consulte o artigo Novidades para desenvolvedores do [Visio ShapeSheet.](what-s-new-for-visio-shapesheet-developers.md)
  
## <a name="relative-geometries"></a>Geometrias relativas
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

Em versões anteriores do Visio, a geometria da forma era definida por fórmulas que dependiam da altura ou largura da forma. Por exemplo, no Visio 2010, os vértices de muitas formas internas do Visio foram definidos multiplicando a altura ou a largura da forma por uma constante. Essas formas tinham **seções Geometry** que incluíam [linhas MoveTo](moveto-row-geometry-section.md) ou [LineTo](lineto-row-geometry-section.md) (por exemplo) com fórmulas como  `Width*1` e  `Height*0` .
  
Agora, o Visio 2013 suporta a geometria relativa na ShapeSheet. Os desenvolvedores de forma pode usar geometrias relativas para especificar geometrias como valores ou fórmulas simples, que multiplicam pela altura ou pela largura automaticamente. Os vértices de forma podem ser expressos como constantes, por exemplo, removendo a necessidade de expressar vértices como múltiplos da largura ou da altura da forma. Isso facilita para que os desenvolvedores criem formas, com um desempenho melhor e tamanhos de arquivo menores. As novas linhas incluem as linhas [RelMoveTo](relmoveto-row-geometry-section.md) e [RelLineTo](rellineto-row-geometry-section.md) onde os valores de célula **X** e **Y** são automaticamente multiplicados pela largura ou altura da forma (respectivamente). 
  
Para obter mais informações sobre as novas linhas ShapeSheet no Visio 2013, consulte o artigo Novidades para desenvolvedores do [Visio ShapeSheet.](what-s-new-for-visio-shapesheet-developers.md)
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Suporte a dados BCS (Serviços de Conectividade Corporativos)
<a name="vis15_WhatsNew_BCS"> </a>

Os diagramas do Visio 2013 agora podem ser conectados a listas externas em servidores do SharePoint Server 2013. Uma lista externa é uma fonte de conteúdo externa ao SharePoint (por exemplo, uma tabela do SQL Server) que foi conectada a uma lista do SharePoint usando o Microsoft Business Connectivity Services (BCS). Visio Services suporta a capacidade de atualizar os diagramas do Visio como as atualizações de dados.
  
Para obter mais informações sobre as novidades nos Serviços do Visio, consulte o artigo Serviços do [Visio no SharePoint 2013.](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx) For more information about Business Connectivity Services (BCS), see [Business Connectivity Services in SharePoint 2013](https://msdn.microsoft.com/library/jj163782%28office.15%29.aspx).
  
## <a name="improvements-in-visio-services"></a>Melhorias nos Serviços do Visio
<a name="vis15_WhatsNew_VisioServices"> </a>

Os Serviços do Visio no Microsoft SharePoint Server 2013 incluem muitas melhorias. Conforme mencionado anteriormente, os Serviços do Visio suportam o novo formato de arquivo do Visio (.vsdx e .vsdm). Os Serviços do Visio expandiram a atualização e o recálculo de dados, incluindo a capacidade de recalcular fórmulas em um diagrama inteiro. 
  
Para obter mais informações sobre as novidades nos Serviços do Visio, consulte o artigo Serviços do [Visio no SharePoint 2013.](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)
  
## <a name="duplicate-page"></a>Duplicar página
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Agora você pode copiar uma página e todas as suas formas dentro do mesmo documento no Visio 2013. Da mesma forma, o objeto **Page** tem um novo método, [Duplicate](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx), que duplica a página e retorna um novo objeto **Page**. 
  
## <a name="visio-object-model-changes"></a>Alterações no modelo de objeto do Visio
<a name="vis15_WhatsNew_NewOM"> </a>

Novos objetos, propriedades, métodos e eventos foram adicionados ao modelo de objeto do Visio para fornecer suporte de programação para novos recursos do Visio 2013. Além disso, as melhorias no modelo de objeto abordam solicitações frequentes de desenvolvedor para alterações na plataforma visio.
  
### <a name="new-members"></a>Novos membros

Os membros a seguir foram adicionados a objetos existentes no modelo de objeto do Visio.
  
 **Tabela 1. Aprimoramentos do modelo de objeto do Visio**
  
|**Objeto ou coleção**|**Novos membros**|
|:-----|:-----|
|[Objeto Application (Visio)](https://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Evento Application.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Evento Application.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Evento Application.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Evento Application.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[Objeto ApplicationSettings (Visio)](https://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[Propriedade ApplicationSettings.EnterCommitsText (Visio)](https://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[Propriedade ApplicationSettings.SVGExportFormat (Visio)](https://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Objeto Document (Visio)](https://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Evento Document.AfterDocumentMerge (Visio)](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Propriedade Document.Comments (Visio)](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Propriedade Document.CompatibilityMode (Visio)](https://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Objeto Documents (Visio)](https://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Evento Documents.AfterDocumentMerge (Visio)](https://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Evento Documents.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Evento Documents.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Evento Documents.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Evento Documents.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[Objeto InvisibleApp (Visio)](https://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[Evento InvisibleApp.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[Evento InvisibleApp.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[Evento InvisibleApp.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[Evento InvisibleApp.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Objeto Page (Visio)](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Evento Page.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Evento Page.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Propriedade Page.Comments (Visio)](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Método Page.Duplicate (Visio)](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Método Page.GetTheme (Visio)](https://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Método Page.GetThemeVariant (Visio)](https://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Evento Page.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Evento Page.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Método Page.SetTheme (Visio)](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Método Page.SetThemeVariant (Visio)](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Propriedade Page.ShapeComments (Visio)](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Objeto Pages (Visio)](https://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Evento Pages.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Evento Pages.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Evento Pages.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Evento Pages.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Objeto Selection (Visio)](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Método Selection.ReplaceShape (Visio)](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Método Selection.SetQuickStyle (Visio)](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Objeto Shape (Visio)](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Método Shape.ChangePicture (Visio)](https://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Propriedade Shape.Comments (Visio)](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Método Shape.ReplaceShape (Visio)](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Método Shape.SetQuickStyle (Visio)](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>Novos objetos e enumerações

Os seguintes objetos foram adicionados ao modelo de objeto do Visio.
  
 **Tabela 2. Adições de modelo de objeto do Visio**
  
|**Object**|**Propriedades**|**Métodos**|
|:-----|:-----|:-----|
|[Objeto CoauthMergeEvent (Visio)](https://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[Propriedade CoauthMergeEvent.BaseDocument (Visio)](https://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [Propriedade CoauthMergeEvent.DownloadDocument (Visio)](https://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [Propriedade CoauthMergeEvent.ObjectType (Visio)](https://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [Propriedade CoauthMergeEvent.Stat (Visio)](https://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [Propriedade CoauthMergeEvent.WorkingDocument (Visio)](https://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |Nenhum  <br/> |
|[Objeto Comment (Visio)](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Propriedade Comment.AssociatedObject (Visio)](https://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Propriedade Comment.AuthorInitials (Visio)](https://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Propriedade Comment.AuthorName (Visio)](https://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Propriedade Comment.AuthorSipAddress (Visio)](https://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Propriedade Comment.AuthorSMTPAddress (Visio)](https://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Propriedade Comment.Collapsed (Visio)](https://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Propriedade Comment.CreateDate (Visio)](https://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Comment.Document (Visio)](https://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Propriedade Comment.EditDate (Visio)](https://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Propriedade Comment.ObjectType (Visio)](https://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Propriedade Comment.Stat (Visio)](https://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Propriedade Comment.Text (Visio)](https://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Método Comment.Delete (Visio)](https://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Objeto Comments (Visio)](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Propriedade Comments.Count (Visio)](https://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Comments.Document (Visio)](https://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Propriedade Comments.Item (Visio)](https://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Propriedade Comments.ObjectType (Visio)](https://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Propriedade Comments.Stat (Visio)](https://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Método Comments.Add (Visio)](https://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Método Comments.DeleteAll (Visio)](https://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[Objeto ReplaceShapesEvent (Visio)](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[Propriedade ReplaceShapesEvent.ObjectType (Visio)](https://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [Propriedade ReplaceShapesEvent.ReplaceFlags (Visio)](https://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [Propriedade ReplaceShapesEvent.ReplacementMaster (Visio)](https://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [Propriedade ReplaceShapesEvent.SelectionSource (Visio)](https://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [Propriedade ReplaceShapesEvent.Stat (Visio)](https://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |Nenhum  <br/> |
   
A tabela a seguir lista as novas enumerações e constantes introduzidas no Visio 2013.
  
 **Tabela 3. Adições de enumeração do Visio**
  
|**Enumeração**|**Descrição**|
|:-----|:-----|
|[Enumeração VisQuickStyleColors (Visio)](https://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |Especifica nomes designados para cores contidas em um tema.  <br/> |
|[Enumeração VisQuickStyleMatrixIndices (Visio)](https://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |Especifica nomes designados para os temas e variações fornecidos com o Visio 2013.  <br/> |
|[Enumeração VisReplaceFlags (Visio)](https://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |Especifica comportamentos para uma operação Alterar Forma.  <br/> |
|[Enumeração visSVGExportFormat (Visio)](https://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |Especifica a inclusão e a exclusão de marcação do Visio durante a exportação de um diagrama para o SVG.  <br/> |
   
### <a name="deprecated-objects-and-members"></a>Objetos e membros substituídos

A tabela a seguir lista os objetos e membros preterido introduzidos no Visio 2013. Somente os membros de objeto substituídos são listados na coluna **Membros preteridos**. 
  
 **Tabela 4. Substituições do modelo de objeto do Visio**
  
|**Objeto ou coleção**|**Membros substituídos**|
|:-----|:-----|
|**Objeto Window**  <br/> |Propriedade **PageTabWidth**  <br/> |
   
## <a name="see-also"></a>Confira também
<a name="vis15_WhatsNew_Additional"> </a>

- [Visio para desenvolvedores](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [Novidades para desenvolvedores do Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md)
    
- [Serviços do Visio no SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)
    
- [Novidades do Visio (Office.com)](https://office.com/redir/HA102749364.aspx)
    
- [Centro do desenvolvedor do Visio](https://msdn.microsoft.com/office/aa905478.aspx)
    

