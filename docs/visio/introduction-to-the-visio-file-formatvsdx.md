---
title: Introdução ao formato de arquivo do Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Saiba mais sobre o novo formato de arquivo no Visio 2013, explorar alguns conceitos de alto nível para trabalhar com o formato de arquivo do Visio 2013 programaticamente e criar um aplicativo de console simples que examina um arquivo do Visio 2013.
ms.openlocfilehash: aa3497af7c467c8f51ab80ab82071776568b4978
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772086"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Introdução ao formato de arquivo do Visio (.vsdx)

Saiba mais sobre o novo formato de arquivo no Visio 2013, explorar alguns conceitos de alto nível para trabalhar com o formato de arquivo do Visio 2013 programaticamente e criar um aplicativo de console simples que examina um arquivo do Visio 2013.
  
|||
|:-----|:-----|
|**Neste artigo** [Introdução](#vis15_IntroVSDX_Intro) [Qual é o formato de arquivo do Visio 2013 "reais"?](#vis15_IntroVSDX_What)                             [Cenários do desenvolvedor para trabalhar com o formato de arquivo do Visio 2013](#vis15_IntroVSDX_Scenarios) [Explorando o formato de arquivo do Visio 2013 programaticamente](#vis15_IntroVSDX_Explore) [Recursos adicionais](#vis15_IntroVSDX_Resources)                    ||
   
## <a name="introduction"></a>Introdução
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 introduz um novo formato de arquivo (. vsdx) para o Visio que substitui o formato de arquivo binário do Visio (. vsd) e o formato de arquivo de desenho XML do Visio (. vdx). Porque o formato de arquivo do Visio 2013 baseia-se se convenções de empacotamento abertos e XML, os desenvolvedores que estão familiarizados com essas tecnologias podem rapidamente Saiba como trabalhar com arquivos do Visio 2013 programaticamente. Os desenvolvedores que estão familiarizados com o formato de arquivo de desenho XML do Visio (. vdx) das versões anteriores do Visio podem encontrar muitas das mesmas estruturas de XML dentro das partes de formato de arquivo. vsdx. Interoperabilidade com o Visio arquivos aumenta consideravelmente desde que o software de terceiros pode manipular os arquivos em um nível de formato de arquivo do Visio. O formato de arquivo do Visio 2013 tem suporte nos serviços do Visio no Microsoft SharePoint Server 2013, sem a necessidade de um formato de arquivo "intermediário" para publicar no SharePoint Server.
  
Há vários tipos de arquivo, por extensão, que compõem o formato de arquivo do Visio 2013. Essas extensões incluem:
  
- .vsdx (Desenho do Visio)
    
- .vsdm (Desenho habilitado para macro do Visio)
    
- .vssx (Estêncil do Visio)
    
- .vssm (Estêncil habilitado para macro do Visio)
    
- .vstx (Modelo do Visio)
    
- .vstm (Modelo habilitado para macro do Visio)
    
> [!NOTE]
> Somente os arquivos ativados por macro (.vsdm, .vssm, .vstm) podem armazenar macros VBA. Não é possível armazenar macros com extensões .vsdx, .vssx ou .vstx. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>O que é o formato de arquivo do Visio 2013 "reais"?
<a name="vis15_IntroVSDX_What"> </a>

O formato de arquivo do Visio 2013 usa o Open remessa convenções (OPC), que definem um meio estruturado para armazenar dados de aplicativo com os recursos relacionados usando um contêiner de alguns sort─for por exemplo, um arquivo ZIP. Em um nível básico, um arquivo do Visio 2013 é realmente um contêiner ZIP que contém os outros tipos de arquivos. Na verdade, você pode salvar um desenho no Visio 2013, como um arquivo. vsdx, renomear a extensão de arquivo para "\*. zip" no Windows Explorer e então abrir o arquivo like para ver o conteúdo dentro de uma pasta.
  
> [!NOTE]
>  Este artigo contém apenas uma breve visão geral das convenções de empacotamento Open. Você pode encontrar mais detalhadas cobertura das convenções em outros artigos: > para obter mais informações sobre as convenções de empacotamento Open sozinhos, consulte [OPC: uma nova padrão para seus dados do empacotamento](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > Para obter mais informações sobre as convenções de empacotamento aberto e seus usos em arquivos do Microsoft Office, consulte [conceitos básicos sobre as convenções de empacotamento abertos](http://msdn.microsoft.com/en-us/library/ee361919.aspx) e [apresentando formatos XML abertos do Office (2007)](http://msdn.microsoft.com/en-us/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Pacotes e partes de pacotes

Como iniciado anteriormente, o Visio 2013 arquivos são contêineres ZIP ou "pacotes" que armazenam os outros arquivos (chamados "empacotar partes") dentro deles. Uma parte do pacote pode ser um arquivo XML, uma imagem, até mesmo uma solução do VBA. As partes dentro do pacote podem ser divididas em duas amplas categorias, "partes do documento" e "partes de relação". As partes do documento contêm o conteúdo real e os metadados do arquivo do Visio, como o nome do arquivo, a primeira página e todas as formas que ele contém, e até mesmo as conexões de dados para as formas. Imagens e arquivos de texto dentro do pacote são considerados partes do documento. Partes de relação são descritos em mais detalhes posteriormente neste artigo.
  
> [!NOTE]
> Se você abrir um arquivo do Visio 2013 usando um utilitário ZIP, você provavelmente pode ver várias pastas contidas no pacote ZIP. Você ainda pode manipular esses endereços sub-recurso como pastas usando um utilitário ZIP. No entanto, esses "pastas" representam endereços subsites dentro do pacote ZIP, pastas não reais. Você não pode usar os equivalentes de programação de pastas para trabalhar com esses endereços sub-recurso em sua solução. 
  
As partes de pacotes (partes de documentos e de relações) também possuem tipos de conteúdo associados. Esses tipos de conteúdo são cadeias de caracteres, que definem um tipo de mídia MIME. Esses tipos de conteúdo especificam e analisam os tipos MIME, que podem estar incluídos no arquivo.
  
### <a name="relationships"></a>Relacionamento

As partes de relação (que terminam com a extensão "\*. rels" e são armazenados em uma pasta rels") descrevem como as partes dentro do pacote se relacionam entre si e fornecer a estrutura do arquivo. Um documento XML autônomo usa a relação pai/filho dos elementos para determinar a relação de entidades uns aos outros. Outros arquivos podem usar outras hierarquias ou uma estrutura de pasta de arquivo para descrever a interação do conteúdo do arquivo. Para o formato de arquivo do Visio 2013, o pacote é um arquivo válido do Visio se ele contém o conjunto correto de partes e o pacote contém as relações entre as partes. 
  
As partes de relacionamentos são documentos XML que descrevem as relacionamentos entre as diferentes partes do documento no pacote. Elas definem uma associação entre dois itens: uma fonte especificada (definida pelo nome e local do arquivo de relacionamento) e uma parte do documento de destino especificado. Por exemplo, as partes do relacionamento são utilizadas para descrever quais as formas padrão estão associadas ao arquivo, como as páginas se referem ao arquivo e entre si e como as imagens e objetos se referem a uma página específica. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Semelhanças e diferenças com o esquema do Visio VDX

Conforme mencionado, as versões anteriores do Visio também incluíam um arquivo baseado em XML formato, o formato de desenho XML do Visio ou. vdx. (Nas versões anteriores do Visio, o esquema usado para o formato de desenho XML do Visio é chamado DatadiagramML). Algumas partes do esquema XML do Visio permaneceram inalterados entre os formatos de dois arquivo. Por exemplo, o elemento do **Windows** e seus filhos permanecem unchanged─with a exceção de que o elemento do **Windows** agora é um elemento raiz de um documento XML (window.xml). 
  
A maior diferença entre o formato de desenho XML e o formato de arquivo do Visio 2013 é o empacotamento. Um arquivo em formato de desenho XML poderia ser manipulado como um XML autônomo normal; o formato de arquivo do Visio 2013 deve ser manipulado como um pacote. No Visio 2013, o XML tiver sido dividido em partes para consumo mais fácil. Outra alteração perceptível é que o formato de arquivo do Visio 2013 armazena todas as propriedades de documento em partes do documento descritas pelo OPC standard (App. XML, Core, Custom).
  
No entanto, há uma alteração significativa que todos os desenvolvedores do Visio devem estar cientes: a introdução dos elementos de **célula**, **linha**e **seção** . No esquema de formato de arquivo de desenho XML, linhas individuais e células na ShapeSheet são representadas por elementos nomeados. Por exemplo, imagine que você tenha um documento com uma única página que contém uma forma com um valor de **PinX** de "2" (o que significa que o pin de rotação da forma é 2 polegadas, da borda esquerda do desenho). A marcação relevante para que a configuração no formato de arquivo de desenho XML é mostrada no código a seguir. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Aqui, o elemento **PinX** é um filho do elemento **XForm** , que por sua vez é um filho do elemento de **forma** . Estes modelos da UI do ShapeSheet do Visio, onde a célula **PinX** está incluída na seção **Shape Transform** de uma forma. 
  
No formato de arquivo do Visio 2013, todas as células a ShapeSheet─ **PinX**, **LinePattern**, uma célula **X** em uma linha **MoveTo** em uma seção **Geometry** , etc.─are representado por um tipo de elemento XML, o elemento de **célula** . Diferentes elementos de **célula** são individuated uns dos outros pelo valor do atributo seus **N** . Assim, o exemplo acima, os dados contidos na célula **PinX** na ShapeSheet são armazenados em um arquivo VSDX, conforme mostrado no código a seguir. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

O elemento de **célula** para **PinX** (assim como outras células individuais, denominadas chamadas "células único" como **LinePattern** ou **LockSelect**) é um filho direto do elemento de **forma** . Nenhum elemento exclusivo necessário para representar a linha que contém a célula **PinX** , conforme a cada forma só pode ter um **PinX**.
  
E quanto seções que incluem dados tabulares, como seções **Geometry** ? Para as células nessas seções, o esquema de formato de arquivo do Visio 2013 usa **seção** e **linha** elements─also diferenciado por seus **N** atributo ou o atributo **T** como mostrado below─to contêm os dados. Por exemplo, a forma mesma do exemplo anterior pode conter dados na seção **Geometry 1** parecido com o seguinte código no esquema de desenho XML. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Geom IX="0">
        <!--- Other cells and rows in the Geometry 1 section -->
        <LineTo IX="1">
            <X F="Width*0">0</X>
            <Y F="Height*0">0</Y>
        </LineTo>
    </Geom>
</Shape>

```

No entanto, ele se parece com o código a seguir no arquivo do Visio 2013.
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Section N="Geometry" IX="0"> 
        <!--- Other cells and rows in the Geometry 1 section -->
        <Row IX="1" T="LineTo">
            <Cell V="0" N="X" V="Width*0" />
            <Cell V="0" N="Y" V="Height*0" />
        </Row>
    </Section>
</Shape>

```

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Cenários de desenvolvedores para trabalhar com formatos de arquivo do Visio 2013.
<a name="vis15_IntroVSDX_Scenarios"> </a>

Conforme explicado acima, o formato de arquivo do Visio 2013 aproveita várias tecnologias bem compreendidas como arquivos ZIP e XML para armazenar dados. Para manipular no nível do arquivo de desenho do Visio 2013, uma solução só precisa usar os namespaces do .NET Framework e classes associadas como trabalhar com arquivos ZIP ou XML, como [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) ou [System. XML](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx).
  
Os principais benefícios aos desenvolvedores de formato de arquivo do Visio 2013 é que você pode ler e gravar em arquivos do Visio 2013 sem automatizando o aplicativo cliente do Visio. Alguns cenários que podem ser considerados como um desenvolvedor para trabalhar com o formato de arquivo do Visio 2013 incluem:
  
- Verificando arquivos do Visio 2013 individuais para dados específicos. Seletivamente, você pode ler um item sem o contêiner ZIP sem precisar extrair o arquivo todo.
    
- Atualizando bibliotecas de arquivos do Visio 2013 com conteúdo específico. Programaticamente, você pode alterar o logotipo em todas as páginas do plano de fundo para refletir a novas diretrizes de marcas.
    
- Criando aplicativos que consomem arquivos do Visio 2013. Por exemplo, você pode criar uma ferramenta que lê um diagrama de fluxo de trabalho do Visio e, em seguida, executa sua própria lógica de negócios com base àquele fluxo de trabalho.
    
Saiba que, por essas soluções utilizarem conjuntos padrão do .NET Framework, a maioria das soluções que podem ser executadas em um computador cliente também podem ser executadas em um servidor!
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Explorar o formato de arquivo do Visio 2013 de forma programática
<a name="vis15_IntroVSDX_Explore"> </a>

A tarefa mais básica e fundamental para qualquer desenvolvedor trabalhando com o formato de arquivo do Visio 2013 é abrir o arquivo como um pacote e, em seguida, acessando partes individuais dentro do pacote. O **System.IO.Packaging.Package** no WindowsBase. dll contém várias classes que permitem que você abra e manipular pacotes e partes. 
  
No seguinte modelo de código, você pode verificar como abrir um arquivo .vsdx, ler a lista de partes no pacote e obter informações sobre cada uma delas.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Para abrir um arquivo .vsdx e exibir as partes do documento

1. Abra o Visio 2013 e crie um novo documento.
    
2. Crie um novo documento e salve-o na área de trabalho.
    
3. Abra o Visual Studio 2012.
    
4. No menu **arquivo** , escolha **novo**e escolha * * Project * *.
    
5. Em **Visual C#** ou **Visual Basic**, expanda o **Windows** e selecione **Aplicativo de Console**.
    
6. Na caixa **nome** , digite 'VisioFileExplorer'. O projeto de aplicativo de Console é aberto. 
    
7. No ** 	Gerenciador de Soluções**, clique com o botão direito do mouse em **VisioFileExplorer** e em **Adicionar Referência**. 
    
8. Na caixa de diálogo **Adicionar Referência**, em **Conjuntos**, expanda **Framework** e escolha **WindowsBase**.
    
9. Cole o seguinte código na solução.
    
  ```cs
  using System;
  using System.Collections.Generic;
  using System.Linq;
  using System.Text;
  using System.IO;
  using System.IO.Packaging;
  using System.Diagnostics;
  namespace VisioFileExplorer
  {
      class Program
      {
          static void Main(string[] args)
          {    
              try
              {
                  Console.WriteLine("Opening the VSDX file ...");
                  // Need to get the folder path for the Desktop
                  // where the file is saved.
                  string dirPath = System.Environment.GetFolderPath(
                      System.Environment.SpecialFolder.Desktop);
                  DirectoryInfo myDir = new DirectoryInfo(dirPath);
                  // It is a best practice to get the file name string
                  // using a FileInfo object, but it isn't necessary.
                  FileInfo[] fInfos = myDir.GetFiles("*.vsdx");
                  FileInfo fi = fInfos[0];
                  string fName = fi.FullName;
                  // We're not going to do any more than open
                  // and read the list of parts in the package, although
                  // we can create a package or read/write what's inside.
                  using (Package fPackage = Package.Open(
                      fName, FileMode.Open, FileAccess.Read))
                  {
                      
                      // The way to get a reference to a package part is
                      // by using its URI. Thus, we're reading the URI
                      // for each part in the package.
                      PackagePartCollection fParts = fPackage.GetParts();
                      foreach (PackagePart fPart in fParts)
                      {
                          Console.WriteLine("Package part: {0}", fPart.Uri);
                      }
                  }   
              }
              catch (Exception err)
              {
                  Console.WriteLine("Error: {0}", err.Message);
              }
              finally
              {
                  Console.Write("\nPress any key to continue ...");
                  Console.ReadKey();
              }   
          }
      }
  }
  ```

  ```vb
  Imports System
  Imports System.Collections.Generic
  Imports System.Linq
  Imports System.Text
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Diagnostics
  Module Module1
      Sub Main()
          Try
              Console.WriteLine("Opening the VSDX file ...")
              ' Need to get the folder path for the Desktop
              ' or where the file is saved.
              Dim dirPath As String = System.Environment.GetFolderPath( _
                  System.Environment.SpecialFolder.Desktop)
              Dim myDir As New DirectoryInfo(dirPath)
              ' It is a best practice to get the file name string
              ' using a FileInfo object, but it isn't necessary.
              Dim fInfos As FileInfo() = myDir.GetFiles("*.vsdx")
              Dim fi As FileInfo = fInfos(0)
              Dim fName As String = fi.FullName
              ' We don't need to do any more than open
              ' and read the list of parts in the package, although
              ' we can create a package or read/write what's inside.
              Using fPackage As Package = Package.Open( _
                  fName, FileMode.Open, FileAccess.Read)
                  ' The way to get a reference to a document part is
                  ' by using its URI. Thus, we're reading the URI
                  ' for each document part in the package.
                  Dim fParts As PackagePartCollection = fPackage.GetParts()
                  For Each fPart As PackagePart In fParts
                      Console.WriteLine("Package part: {0}", fPart.Uri)
                  Next
              End Using
          Catch err As Exception
              Console.WriteLine("Error: {0}", err.Message)
          Finally
              Console.Write(vbLf &amp; "Press any key to continue ...")
              Console.ReadKey()
          End Try
      End Sub
  End Module
  
  ```

10. Pressione F5 para depurar a solução. Quando o programa concluir a execução, pressione qualquer tecla para sair.
    
## <a name="see-also"></a>Confira também
<a name="vis15_IntroVSDX_Resources"> </a>

Para obter mais informações sobre como trabalhar com arquivos de OpenXML Office Visio 2013or programaticamente, Open Packaging Convention ou o formato de arquivo do Visio 2013, consulte os seguintes recursos:
  
- [Visio para desenvolvedores](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [OPC: um novo padrão para empacotar dados](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).
    
- [Conceitos básicos sobre as convenções de empacotamento Open](http://msdn.microsoft.com/en-us/library/ee361919.aspx)
    
- [Apresentando os formatos de arquivo do Office (2007) Open XML](http://msdn.microsoft.com/en-us/library/aa338205.aspx)
    

