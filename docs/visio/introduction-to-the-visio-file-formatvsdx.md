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
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="18000-103">Introdução ao formato de arquivo do Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="18000-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="18000-104">Leia sobre o novo formato de arquivo no Visio 2013, explore alguns conceitos de alto nível para trabalhar programaticamente com o novo formato de arquivo do Visio 2013 e crie um aplicativo de console simples que examinará um arquivo do Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="18000-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18000-105">**Neste artigo**[Introdução](#vis15_IntroVSDX_Intro)[Qual é o formato de arquivo subjacente do Visio 2013?](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="18000-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="18000-106">[Cenários de desenvolvedor para trabalhar com o formato de arquivo do Visio 2013](#vis15_IntroVSDX_Scenarios)[Explorar o formato de arquivo do Visio 2013 de forma programática](#vis15_IntroVSDX_Explore)[recursos adicionais                    ](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="18000-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="18000-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="18000-107">Introduction</span></span>
<span data-ttu-id="18000-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="18000-108"></span></span>

<span data-ttu-id="18000-109">O Visio 2013 apresenta um novo formato de arquivo (.vsdx) para o Visio que substitui o formato de arquivo binário do Visio (.vsd) e o formato de arquivo de desenho XML do Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="18000-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="18000-110">Como o formato de arquivo do Visio 2013 é baseado em Open Packaging Conventions e XML, os desenvolvedores que estão familiarizados com essas tecnologias podem aprender rapidamente como trabalhar com arquivos do Visio 2013 programaticamente.</span><span class="sxs-lookup"><span data-stu-id="18000-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="18000-111">Desenvolvedores que estão familiarizados com o formato de arquivo do desenho XML do Visio (. vdx) de versões anteriores do Visio podem encontrar muitas das mesmas estruturas de XML em partes de formato de arquivo. vsdx.</span><span class="sxs-lookup"><span data-stu-id="18000-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="18000-112">A interoperabilidade com arquivos do Visio aumenta porque o software de terceiros pode manipular os arquivos do Visio em um nível de formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="18000-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="18000-113">O formato de arquivo do Visio 2013 é suportado no Serviços do Visio no Microsoft SharePoint Server 2013, sem a necessidade de um formato de arquivo "intermediário" para publicação no SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="18000-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="18000-114">Há vários tipos de arquivo, por extensão, que compõem o formato de arquivo do Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="18000-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="18000-115">Essas extensões incluem:</span><span class="sxs-lookup"><span data-stu-id="18000-115">These extensions include:</span></span>
  
- <span data-ttu-id="18000-116">. vsdx (desenho do Visio)</span><span class="sxs-lookup"><span data-stu-id="18000-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="18000-117">. vsdm (desenho habilitados para macro do Visio)</span><span class="sxs-lookup"><span data-stu-id="18000-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="18000-118">vssx (estêncil do Visio)</span><span class="sxs-lookup"><span data-stu-id="18000-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="18000-119">. vssm (estêncil habilitados para macro do Visio)</span><span class="sxs-lookup"><span data-stu-id="18000-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="18000-120">. vstx (modelo do Visio)</span><span class="sxs-lookup"><span data-stu-id="18000-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="18000-121">. vstm (modelo habilitado para macro do Visio)</span><span class="sxs-lookup"><span data-stu-id="18000-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="18000-p104">Somente os arquivos ativados por macro (.vsdm, .vssm, .vstm) podem armazenar macros VBA. Não é possível armazenar macros com extensões .vsdx, .vssx ou .vstx.</span><span class="sxs-lookup"><span data-stu-id="18000-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="18000-124">Qual é o formato de arquivo subjacente do Visio 2013?</span><span class="sxs-lookup"><span data-stu-id="18000-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="18000-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="18000-125"></span></span>

<span data-ttu-id="18000-126">O formato de arquivo do Visio 2013 usa o Open Packing Conventions (OPC), que define um meio estruturado para armazenar dados do aplicativo junto com recursos relacionados usando um contêiner de algum tipo - por exemplo, um arquivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="18000-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="18000-127">Em um nível básico, um arquivo do Visio 2013 é realmente um contêiner ZIP que contém outros tipos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="18000-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="18000-128">Na verdade, você pode salvar um desenho no Visio 2013 como um arquivo .vsdx, renomear a extensão do arquivo para "\*.zip" no Windows Explorer e, em seguida, abrir o arquivo como uma pasta para ver o conteúdo interno.</span><span class="sxs-lookup"><span data-stu-id="18000-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="18000-129">Este artigo contém apenas uma breve visão geral da Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="18000-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="18000-130">Você pode encontrar uma cobertura mais detalhada das convenções em outros artigos: > [OPC: um novo padrão para empacotar dados](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="18000-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="18000-131">Para obter mais informações sobre Open Packaging Conventions e seu uso em arquivos do Microsoft Office, consulte [Fundamentos de Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) e [Introduzindo os formatos de arquivo XML abertos do Microsoft Office (2007)](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="18000-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="18000-132">Pacotes e partes de pacotes</span><span class="sxs-lookup"><span data-stu-id="18000-132">Packages and Package Parts</span></span>

<span data-ttu-id="18000-133">Conforme iniciado anteriormente, os arquivos do Visio 2013 são contêineres ZIP ou "pacotes" que contêm outros arquivos (chamados "partes do pacote") dentro deles.</span><span class="sxs-lookup"><span data-stu-id="18000-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="18000-134">Uma parte do pacote pode ser um arquivo XML, uma imagem, até mesmo uma solução do VBA.</span><span class="sxs-lookup"><span data-stu-id="18000-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="18000-135">Partes dentro do pacote podem ser divididas em duas categorias amplas, "partes do documento" e "partes da relação."</span><span class="sxs-lookup"><span data-stu-id="18000-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="18000-136">As partes do documento contêm o conteúdo e os metadados reais do arquivo do Visio, como o nome do arquivo, a primeira página e todas as formas que ele contém e até mesmo as conexões de dados para as formas.</span><span class="sxs-lookup"><span data-stu-id="18000-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="18000-137">Imagens e arquivos de texto dentro do pacote são considerados partes do documento.</span><span class="sxs-lookup"><span data-stu-id="18000-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="18000-138">Partes da relação estão descritas com mais detalhes neste artigo.</span><span class="sxs-lookup"><span data-stu-id="18000-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="18000-139">Se você abrir um arquivo do Visio 2013 usando um utilitário ZIP, provavelmente poderá ver várias pastas contidas dentro do pacote ZIP.</span><span class="sxs-lookup"><span data-stu-id="18000-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="18000-140">Você pode até mesmo manipular esses sub-endereços como pastas usando um utilitário ZIP.</span><span class="sxs-lookup"><span data-stu-id="18000-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="18000-141">No entanto, essas "pastas" representam sub-endereços dentro do pacote ZIP, não pastas reais.</span><span class="sxs-lookup"><span data-stu-id="18000-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="18000-142">Você não pode usar os equivalentes programáticos de pastas para trabalhar com esses subendereços na sua solução.</span><span class="sxs-lookup"><span data-stu-id="18000-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="18000-p109">As partes de pacotes (partes de documentos e de relações) também possuem tipos de conteúdo associados. Esses tipos de conteúdo são cadeias de caracteres, que definem um tipo de mídia MIME. Esses tipos de conteúdo especificam e analisam os tipos MIME, que podem estar incluídos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="18000-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="18000-146">Relações</span><span class="sxs-lookup"><span data-stu-id="18000-146">Relationships</span></span>

<span data-ttu-id="18000-147">As partes da relação (que terminam com a extensão "\*. rels" e são armazenadas em uma pasta rels") descrevem como as partes dentro do pacote se relacionam entre si e proporcionam uma estrutura do arquivo.</span><span class="sxs-lookup"><span data-stu-id="18000-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="18000-148">Um documento XML autônomo usa relacionamento pai/filho de elementos para determinar a relação de uma entidade com a outra. </span><span class="sxs-lookup"><span data-stu-id="18000-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="18000-149">Outros arquivos podem usar outras hierarquias ou estrutura de pastas de arquivos para descrever a interação do conteúdo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="18000-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="18000-150">Para o formato de arquivo do Visio 2013, o pacote é um arquivo do Visio válido se contiver o conjunto correto de partes e o pacote contiver os relacionamentos entre as partes.</span><span class="sxs-lookup"><span data-stu-id="18000-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="18000-p111">As partes de relacionamentos são documentos XML que descrevem as relacionamentos entre as diferentes partes do documento no pacote. Elas definem uma associação entre dois itens: uma fonte especificada (definida pelo nome e local do arquivo de relacionamento) e uma parte do documento de destino especificado. Por exemplo, as partes do relacionamento são utilizadas para descrever quais as formas padrão estão associadas ao arquivo, como as páginas se referem ao arquivo e entre si e como as imagens e objetos se referem a uma página específica.</span><span class="sxs-lookup"><span data-stu-id="18000-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="18000-154">Semelhanças e diferenças no esquema VDX do Visio</span><span class="sxs-lookup"><span data-stu-id="18000-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="18000-155">Como mencionado, as versões anteriores do Visio também incluíam um formato de arquivo baseado em XML, o Visio XML Drawing Format ou .vdx.</span><span class="sxs-lookup"><span data-stu-id="18000-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="18000-156">(Nas versões anteriores do Visio, o esquema usado para o Visio XML Drawing Format é chamado DatadiagramML.) Algumas partes do esquema XML do Visio permaneceram as mesmas entre os dois formatos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="18000-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="18000-157">Por exemplo, o elemento do **Windows** e seus filhos permanecem inalterados - com a exceção de que o elemento do**Windows** agora é um elemento raiz de um documento XML (window.xml).</span><span class="sxs-lookup"><span data-stu-id="18000-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="18000-158">A maior diferença entre o formato do arquivo do Visio 2013 e o formato de desenho do XML é a embalagem.</span><span class="sxs-lookup"><span data-stu-id="18000-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="18000-159">Um arquivo XML Drawing Format pode ser manipulado como um XML autônomo normal; o formato de arquivo do Visio 2013 deve ser manipulado como um pacote.</span><span class="sxs-lookup"><span data-stu-id="18000-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="18000-160">No Visio 2013, o XML foi dividido em partes para facilitar o consumo.</span><span class="sxs-lookup"><span data-stu-id="18000-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="18000-161">Outra alteração perceptível é que o formato de arquivo do Visio 2013 armazena todas as propriedades do documento em partes do documento descritas pelo padrão OPC (app.xml, core.xml, custom.xml).</span><span class="sxs-lookup"><span data-stu-id="18000-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="18000-162">No entanto, há uma alteração significativa que todos os desenvolvedores do Visio devem considerar: a introdução dos elementos **Célula**, **Linha**, e **Seção**.</span><span class="sxs-lookup"><span data-stu-id="18000-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="18000-163">No esquema XML Drawing File Format, linhas e células individuais na ShapeSheet são representadas por elementos nomeados.</span><span class="sxs-lookup"><span data-stu-id="18000-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="18000-164">Por exemplo, imagine que você tem um documento com uma única página que contém uma forma com um valor **PinX** de "2" (o que significa que o pino de rotação da forma é de 2 polegadas a partir da borda esquerda do desenho).</span><span class="sxs-lookup"><span data-stu-id="18000-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="18000-165">A marcação relevante para essa configuração no XML Drawing File Format é mostrada no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="18000-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="18000-166">Aqui, o elemento**PinX** é filho do elemento**XForm**, que, por sua vez, é um filho do elemento **Shape**.</span><span class="sxs-lookup"><span data-stu-id="18000-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="18000-167">Isso modela a Visio ShapeSheet UI, onde a célula **PinX** é incluída na seção **Shape Transform** de uma forma.</span><span class="sxs-lookup"><span data-stu-id="18000-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="18000-168">No formato de arquivo do Visio 2013, todas as células na ShapeSheet─ **PinX**, **LinePattern**, uma célula **X** em uma linha**MoveTo** em uma seção **Geometria**, etc.─são representadas por um tipo de elemento XML, o elemento **Cell**.</span><span class="sxs-lookup"><span data-stu-id="18000-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="18000-169">Diferentes elementos **Cell** são individualizados entre si pelo valor de seu atributo **N**.</span><span class="sxs-lookup"><span data-stu-id="18000-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="18000-170">Desse modo, no exemplo acima, os dados contidos na célula **PinX** na ShapeSheet é armazenada em um arquivo VSDX conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="18000-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="18000-171">O elemento **Cell** para **PinX** (assim como outras células nomeadas individuais chamadas "células singleton", como **LinePattern** ou **LockSelect**) é um filho direto do elemento **Shape**.</span><span class="sxs-lookup"><span data-stu-id="18000-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="18000-172">Não é necessário nenhum elemento exclusivo para representar a linha que contém a célula**PinX** já que cada forma só pode ter uma **PinX**.</span><span class="sxs-lookup"><span data-stu-id="18000-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="18000-173">E as seções que incluem como os dados tabulares, como as seções **Geometria**?</span><span class="sxs-lookup"><span data-stu-id="18000-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="18000-174">Das células essas seções, o esquema de formato de arquivo do Visio 2013 usa **seção** e **linha** elements─also distintos pela sua **N** atributo ou \*\*T \*\* atributo conforme mostrado below─to contêm os dados.</span><span class="sxs-lookup"><span data-stu-id="18000-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="18000-175">Por exemplo, a mesma forma do exemplo anterior pode conter dados na seção **Geometria 1** parecidos com o seguinte código no esquema de desenho XML.</span><span class="sxs-lookup"><span data-stu-id="18000-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="18000-176">No entanto, ele tem a aparência do seguinte código no arquivo do Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="18000-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="18000-177">Cenários de desenvolvedor para trabalhar com o formato de arquivo do Visio 2013</span><span class="sxs-lookup"><span data-stu-id="18000-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="18000-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="18000-178"></span></span>

<span data-ttu-id="18000-179">Conforme explicado acima, o formato de arquivo do Visio 2013 aproveita várias tecnologias bem compreendidas, como arquivos ZIP e XML, para armazenar dados.</span><span class="sxs-lookup"><span data-stu-id="18000-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="18000-180">Para manipular um desenho do Visio 2013 no nível do arquivo, uma solução só precisa usar as namespaces e classes do .NET Framework associadas ao trabalho com arquivos ZIP ou XML, como [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) ou [System. XML](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="18000-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="18000-181">A principal vantagem para desenvolvedores do formato de arquivo do Visio 2013 é ler e gravar arquivos do Visio 2013 sem automatizar o aplicativo de cliente do Visio.</span><span class="sxs-lookup"><span data-stu-id="18000-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="18000-182">Alguns cenários que você pode considerar como um desenvolvedor para trabalhar com o formato de arquivo do Visio 2013 incluem:</span><span class="sxs-lookup"><span data-stu-id="18000-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="18000-183">Verificar arquivos individuais do Visio 2013 para dados específicos.</span><span class="sxs-lookup"><span data-stu-id="18000-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="18000-184">É possível ler um item de forma seletiva fora do contêiner ZIP sem ter que extrair o arquivo inteiro.</span><span class="sxs-lookup"><span data-stu-id="18000-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="18000-185">Atualizar a bibliotecas de arquivos do Visio 2013 com o conteúdo específico.</span><span class="sxs-lookup"><span data-stu-id="18000-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="18000-186">É possível alterar o logotipo de forma programática em todas as páginas de fundo para refletir as novas diretrizes da marca.</span><span class="sxs-lookup"><span data-stu-id="18000-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="18000-187">Criar aplicativos que consomem arquivos do Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="18000-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="18000-188">Por exemplo, é possível criar uma ferramenta para ler um diagrama do fluxo de trabalho no Visio e, em seguida, executar sua própria lógica de negócios com base nesse fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="18000-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="18000-189">Saiba que, por essas soluções utilizarem conjuntos padrão do .NET Framework, a maioria das soluções que podem ser executadas em um computador cliente também podem ser executadas em um servidor!</span><span class="sxs-lookup"><span data-stu-id="18000-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="18000-190">Explorar o formato de arquivo do Visio 2013 de forma programática</span><span class="sxs-lookup"><span data-stu-id="18000-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="18000-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="18000-191"></span></span>

<span data-ttu-id="18000-192">A tarefa mais básica e fundamental para qualquer desenvolvedor que trabalhe com o formato de arquivo do Visio 2013 é abrir o arquivo como um pacote e, em seguida, acessar partes individuais dentro do pacote.</span><span class="sxs-lookup"><span data-stu-id="18000-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="18000-193">O **System.IO.Packaging.Package** no WindowsBase.dll contém muitas classes que permitem abrir e manipular pacotes e partes.</span><span class="sxs-lookup"><span data-stu-id="18000-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="18000-194">No seguinte modelo de código, você pode verificar como abrir um arquivo .vsdx, ler a lista de partes no pacote e obter informações sobre cada uma delas.</span><span class="sxs-lookup"><span data-stu-id="18000-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="18000-195">Abrir um arquivo. vsdx e exibir as partes do documento</span><span class="sxs-lookup"><span data-stu-id="18000-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="18000-196">Abra o Visio 2013 e crie um novo documento.</span><span class="sxs-lookup"><span data-stu-id="18000-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="18000-197">Crie um novo documento e salve-o na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="18000-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="18000-198">Abra o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="18000-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="18000-199">No menu **arquivo**, escolha **novo** e, em seguida, selecione \*\* Projeto\*\*.</span><span class="sxs-lookup"><span data-stu-id="18000-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="18000-200">Em \*\*Visual C# \*\* ou **Visual Basic**, expanda o **Windows**e selecione **Aplicativo de console**.</span><span class="sxs-lookup"><span data-stu-id="18000-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="18000-201">Na caixa **Nome**, digite "VisioFileExplorer".</span><span class="sxs-lookup"><span data-stu-id="18000-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="18000-202">O projeto Aplicativo de Console é aberto.</span><span class="sxs-lookup"><span data-stu-id="18000-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="18000-203">No **Gerenciador de Soluções**, clique com o botão direito do mouse em **VisioFileExplorer** e clique em **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="18000-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="18000-204">Na caixa de diálogo **referenciar** em **Assemblies**, expanda **estrutura**e escolha **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="18000-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="18000-205">Cole o seguinte código na solução.</span><span class="sxs-lookup"><span data-stu-id="18000-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="18000-p126">Pressione F5 para depurar a solução. Quando o programa concluir a execução, pressione qualquer tecla para sair.</span><span class="sxs-lookup"><span data-stu-id="18000-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18000-208">Confira também</span><span class="sxs-lookup"><span data-stu-id="18000-208">See also</span></span>
<span data-ttu-id="18000-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="18000-209"></span></span>

<span data-ttu-id="18000-210">Para obter mais informações sobre o formato de arquivo do Visio 2013, a Open Packaging Convention, ou como trabalhar com o Visio 2013, ou com arquivos OpenXML do Office de forma programática, consulte os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="18000-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="18000-211">Visio para desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="18000-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="18000-212">[OPC: Um novo padrão para sua embalagem de dados](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="18000-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="18000-213">Conceitos básicos das Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="18000-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="18000-214">Apresentando os formatos de arquivo Open XML (2007) do Office</span><span class="sxs-lookup"><span data-stu-id="18000-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

