---
title: Introdução ao formato de arquivo do Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Leia sobre o novo formato de arquivo no Visio 2013, explore alguns conceitos de alto nível para trabalhar programaticamente com o novo formato de arquivo do Visio 2013 e crie um aplicativo de console simples que examinará um arquivo do Visio 2013.
localization_priority: Priority
ms.openlocfilehash: 74c0f05a1db280386f3dc9dfd23da73a9b2daaf5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357271"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Introdução ao formato de arquivo do Visio (.vsdx)

Leia sobre o novo formato de arquivo no Visio 2013, explore alguns conceitos de alto nível para trabalhar programaticamente com o novo formato de arquivo do Visio 2013 e crie um aplicativo de console simples que examinará um arquivo do Visio 2013.
  
|||
|:-----|:-----|
|**Neste artigo**[Introdução](#vis15_IntroVSDX_Intro)[Qual é o formato de arquivo subjacente do Visio 2013?](#vis15_IntroVSDX_What)          [Cenários de desenvolvedor para trabalhar com o formato de arquivo do Visio 2013](#vis15_IntroVSDX_Scenarios)[Explorar o formato de arquivo do Visio 2013 de forma programática](#vis15_IntroVSDX_Explore)[recursos adicionais                    ](#vis15_IntroVSDX_Resources)||
   
## <a name="introduction"></a>Introdução
<a name="vis15_IntroVSDX_Intro"> </a>

O Visio 2013 apresenta um novo formato de arquivo (.vsdx) para o Visio que substitui o formato de arquivo binário do Visio (.vsd) e o formato de arquivo de desenho XML do Visio (.vdx). Como o formato de arquivo do Visio 2013 é baseado em Open Packaging Conventions e XML, os desenvolvedores que estão familiarizados com essas tecnologias podem aprender rapidamente como trabalhar com arquivos do Visio 2013 programaticamente. Desenvolvedores que estão familiarizados com o formato de arquivo do desenho XML do Visio (. vdx) de versões anteriores do Visio podem encontrar muitas das mesmas estruturas de XML em partes de formato de arquivo. vsdx. A interoperabilidade com arquivos do Visio aumenta porque o software de terceiros pode manipular os arquivos do Visio em um nível de formato de arquivo. O formato de arquivo do Visio 2013 é suportado no Serviços do Visio no Microsoft SharePoint Server 2013, sem a necessidade de um formato de arquivo "intermediário" para publicação no SharePoint Server.
  
Há vários tipos de arquivo, por extensão, que compõem o formato de arquivo do Visio 2013. Essas extensões incluem:
  
- . vsdx (desenho do Visio)
    
- . vsdm (desenho habilitados para macro do Visio)
    
- vssx (estêncil do Visio)
    
- . vssm (estêncil habilitados para macro do Visio)
    
- . vstx (modelo do Visio)
    
- . vstm (modelo habilitado para macro do Visio)
    
> [!NOTE]
> Somente os arquivos ativados por macro (.vsdm, .vssm, .vstm) podem armazenar macros VBA. Não é possível armazenar macros com extensões .vsdx, .vssx ou .vstx. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Qual é o formato de arquivo subjacente do Visio 2013?
<a name="vis15_IntroVSDX_What"> </a>

O formato de arquivo do Visio 2013 usa o Open Packing Conventions (OPC), que define um meio estruturado para armazenar dados do aplicativo junto com recursos relacionados usando um contêiner de algum tipo - por exemplo, um arquivo ZIP. Em um nível básico, um arquivo do Visio 2013 é realmente um contêiner ZIP que contém outros tipos de arquivos. Na verdade, você pode salvar um desenho no Visio 2013 como um arquivo .vsdx, renomear a extensão do arquivo para "\*.zip" no Windows Explorer e, em seguida, abrir o arquivo como uma pasta para ver o conteúdo interno.
  
> [!NOTE]
>  Este artigo contém apenas uma breve visão geral da Open Packaging Conventions. Você pode encontrar uma cobertura mais detalhada das convenções em outros artigos: > [OPC: um novo padrão para empacotar dados](https://msdn.microsoft.com/magazine/cc163372.aspx). Para obter mais informações sobre Open Packaging Conventions e seu uso em arquivos do Microsoft Office, consulte [Fundamentos de Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) e [Introduzindo os formatos de arquivo XML abertos do Microsoft Office (2007)](https://msdn.microsoft.com/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Pacotes e partes de pacotes

Conforme iniciado anteriormente, os arquivos do Visio 2013 são contêineres ZIP ou "pacotes" que contêm outros arquivos (chamados "partes do pacote") dentro deles. Uma parte do pacote pode ser um arquivo XML, uma imagem, até mesmo uma solução do VBA. Partes dentro do pacote podem ser divididas em duas categorias amplas, "partes do documento" e "partes da relação." As partes do documento contêm o conteúdo e os metadados reais do arquivo do Visio, como o nome do arquivo, a primeira página e todas as formas que ele contém e até mesmo as conexões de dados para as formas. Imagens e arquivos de texto dentro do pacote são considerados partes do documento. Partes da relação estão descritas com mais detalhes neste artigo.
  
> [!NOTE]
> Se você abrir um arquivo do Visio 2013 usando um utilitário ZIP, provavelmente poderá ver várias pastas contidas dentro do pacote ZIP. Você pode até mesmo manipular esses sub-endereços como pastas usando um utilitário ZIP. No entanto, essas "pastas" representam sub-endereços dentro do pacote ZIP, não pastas reais. Você não pode usar os equivalentes programáticos de pastas para trabalhar com esses subendereços na sua solução. 
  
As partes de pacotes (partes de documentos e de relações) também possuem tipos de conteúdo associados. Esses tipos de conteúdo são cadeias de caracteres, que definem um tipo de mídia MIME. Esses tipos de conteúdo especificam e analisam os tipos MIME, que podem estar incluídos no arquivo.
  
### <a name="relationships"></a>Relações

As partes da relação (que terminam com a extensão "\*. rels" e são armazenadas em uma pasta rels") descrevem como as partes dentro do pacote se relacionam entre si e proporcionam uma estrutura do arquivo. Um documento XML autônomo usa relacionamento pai/filho de elementos para determinar a relação de uma entidade com a outra.  Outros arquivos podem usar outras hierarquias ou estrutura de pastas de arquivos para descrever a interação do conteúdo no arquivo. Para o formato de arquivo do Visio 2013, o pacote é um arquivo do Visio válido se contiver o conjunto correto de partes e o pacote contiver os relacionamentos entre as partes. 
  
As partes de relacionamentos são documentos XML que descrevem as relacionamentos entre as diferentes partes do documento no pacote. Elas definem uma associação entre dois itens: uma fonte especificada (definida pelo nome e local do arquivo de relacionamento) e uma parte do documento de destino especificado. Por exemplo, as partes do relacionamento são utilizadas para descrever quais as formas padrão estão associadas ao arquivo, como as páginas se referem ao arquivo e entre si e como as imagens e objetos se referem a uma página específica. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Semelhanças e diferenças no esquema VDX do Visio

Como mencionado, as versões anteriores do Visio também incluíam um formato de arquivo baseado em XML, o Visio XML Drawing Format ou .vdx. (Nas versões anteriores do Visio, o esquema usado para o Visio XML Drawing Format é chamado DatadiagramML.) Algumas partes do esquema XML do Visio permaneceram as mesmas entre os dois formatos de arquivo. Por exemplo, o elemento do **Windows** e seus filhos permanecem inalterados - com a exceção de que o elemento do**Windows** agora é um elemento raiz de um documento XML (window.xml). 
  
A maior diferença entre o formato do arquivo do Visio 2013 e o formato de desenho do XML é a embalagem. Um arquivo XML Drawing Format pode ser manipulado como um XML autônomo normal; o formato de arquivo do Visio 2013 deve ser manipulado como um pacote. No Visio 2013, o XML foi dividido em partes para facilitar o consumo. Outra alteração perceptível é que o formato de arquivo do Visio 2013 armazena todas as propriedades do documento em partes do documento descritas pelo padrão OPC (app.xml, core.xml, custom.xml).
  
No entanto, há uma alteração significativa que todos os desenvolvedores do Visio devem considerar: a introdução dos elementos **Célula**, **Linha**, e **Seção**. No esquema XML Drawing File Format, linhas e células individuais na ShapeSheet são representadas por elementos nomeados. Por exemplo, imagine que você tem um documento com uma única página que contém uma forma com um valor **PinX** de "2" (o que significa que o pino de rotação da forma é de 2 polegadas a partir da borda esquerda do desenho). A marcação relevante para essa configuração no XML Drawing File Format é mostrada no código a seguir. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Aqui, o elemento**PinX** é filho do elemento**XForm**, que, por sua vez, é um filho do elemento **Shape**. Isso modela a Visio ShapeSheet UI, onde a célula **PinX** é incluída na seção **Shape Transform** de uma forma. 
  
No formato de arquivo do Visio 2013, todas as células na ShapeSheet─ **PinX**, **LinePattern**, uma célula **X** em uma linha**MoveTo** em uma seção **Geometria**, etc.─são representadas por um tipo de elemento XML, o elemento **Cell**. Diferentes elementos **Cell** são individualizados entre si pelo valor de seu atributo **N**. Desse modo, no exemplo acima, os dados contidos na célula **PinX** na ShapeSheet é armazenada em um arquivo VSDX conforme mostrado no código a seguir. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

O elemento **Cell** para **PinX** (assim como outras células nomeadas individuais chamadas "células singleton", como **LinePattern** ou **LockSelect**) é um filho direto do elemento **Shape**. Não é necessário nenhum elemento exclusivo para representar a linha que contém a célula**PinX** já que cada forma só pode ter uma **PinX**.
  
E as seções que incluem como os dados tabulares, como as seções **Geometria**? Das células essas seções, o esquema de formato de arquivo do Visio 2013 usa **seção** e **linha** elements─also distintos pela sua **N** atributo ou **T ** atributo conforme mostrado below─to contêm os dados. Por exemplo, a mesma forma do exemplo anterior pode conter dados na seção **Geometria 1** parecidos com o seguinte código no esquema de desenho XML. 
  
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

No entanto, ele tem a aparência do seguinte código no arquivo do Visio 2013.
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Cenários de desenvolvedor para trabalhar com o formato de arquivo do Visio 2013
<a name="vis15_IntroVSDX_Scenarios"> </a>

Conforme explicado acima, o formato de arquivo do Visio 2013 aproveita várias tecnologias bem compreendidas, como arquivos ZIP e XML, para armazenar dados. Para manipular um desenho do Visio 2013 no nível do arquivo, uma solução só precisa usar as namespaces e classes do .NET Framework associadas ao trabalho com arquivos ZIP ou XML, como [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) ou [System. XML](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).
  
A principal vantagem para desenvolvedores do formato de arquivo do Visio 2013 é ler e gravar arquivos do Visio 2013 sem automatizar o aplicativo de cliente do Visio. Alguns cenários que você pode considerar como um desenvolvedor para trabalhar com o formato de arquivo do Visio 2013 incluem:
  
- Verificar arquivos individuais do Visio 2013 para dados específicos. É possível ler um item de forma seletiva fora do contêiner ZIP sem ter que extrair o arquivo inteiro.
    
- Atualizar a bibliotecas de arquivos do Visio 2013 com o conteúdo específico. É possível alterar o logotipo de forma programática em todas as páginas de fundo para refletir as novas diretrizes da marca.
    
- Criar aplicativos que consomem arquivos do Visio 2013. Por exemplo, é possível criar uma ferramenta para ler um diagrama do fluxo de trabalho no Visio e, em seguida, executar sua própria lógica de negócios com base nesse fluxo de trabalho.
    
Saiba que, por essas soluções utilizarem conjuntos padrão do .NET Framework, a maioria das soluções que podem ser executadas em um computador cliente também podem ser executadas em um servidor!
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Explorar o formato de arquivo do Visio 2013 de forma programática
<a name="vis15_IntroVSDX_Explore"> </a>

A tarefa mais básica e fundamental para qualquer desenvolvedor que trabalhe com o formato de arquivo do Visio 2013 é abrir o arquivo como um pacote e, em seguida, acessar partes individuais dentro do pacote. O **System.IO.Packaging.Package** no WindowsBase.dll contém muitas classes que permitem abrir e manipular pacotes e partes. 
  
No seguinte modelo de código, você pode verificar como abrir um arquivo .vsdx, ler a lista de partes no pacote e obter informações sobre cada uma delas.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Abrir um arquivo. vsdx e exibir as partes do documento

1. Abra o Visio 2013 e crie um novo documento.
    
2. Crie um novo documento e salve-o na área de trabalho.
    
3. Abra o Visual Studio 2012.
    
4. No menu **arquivo**, escolha **novo** e, em seguida, selecione ** Projeto**.
    
5. Em **Visual C# ** ou **Visual Basic**, expanda o **Windows**e selecione **Aplicativo de console**.
    
6. Na caixa **Nome**, digite "VisioFileExplorer". O projeto Aplicativo de Console é aberto. 
    
7. No **Gerenciador de Soluções**, clique com o botão direito do mouse em **VisioFileExplorer** e clique em **Adicionar Referência**. 
    
8. Na caixa de diálogo **referenciar** em **Assemblies**, expanda **estrutura**e escolha **WindowsBase**.
    
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

Para obter mais informações sobre o formato de arquivo do Visio 2013, a Open Packaging Convention, ou como trabalhar com o Visio 2013, ou com arquivos OpenXML do Office de forma programática, consulte os seguintes recursos:
  
- [Visio para desenvolvedores](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: Um novo padrão para sua embalagem de dados](https://msdn.microsoft.com/magazine/cc163372.aspx).
    
- [Conceitos básicos das Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Apresentando os formatos de arquivo Open XML (2007) do Office](https://msdn.microsoft.com/library/aa338205.aspx)
    

