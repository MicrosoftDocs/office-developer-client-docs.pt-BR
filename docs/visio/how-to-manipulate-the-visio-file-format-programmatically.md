---
title: Manipular o formato de arquivo do Visio via programação
manager: soliver
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Crie uma solução no Visual Studio 2012 para ler o novo pacote de formato de arquivo no Visio 2013, selecione partes no pacote, altere os dados em uma peça e adicione novas partes ao pacote.
localization_priority: Priority
ms.openlocfilehash: 2b031a74fa8d2df9b9baa15e97652b8d8afdaf23
ms.sourcegitcommit: 6f3f42b656afb45a0189a0ad4c81c095e285b3d9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33655608"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="238a7-103">Manipular o formato de arquivo do Visio via programação</span><span class="sxs-lookup"><span data-stu-id="238a7-103">Manipulate the Visio file format programmatically</span></span>

![Tópico de tutorial](media/mod_icon_howto.png)
  
<span data-ttu-id="238a7-105">Aprenda a criar uma solução no Visual Studio 2012 para ler o novo pacote de formato de arquivo no Visio 2013, selecione partes no pacote, altere os dados em uma peça e adicione novas partes ao pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-105">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="238a7-106">Recursos básicos de manipulação de formato de arquivo do Visio</span><span class="sxs-lookup"><span data-stu-id="238a7-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="238a7-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-107"><a name="vis15_ManipulateFF_Essentials"> </a></span></span>

<span data-ttu-id="238a7-108">Versões anteriores do Visio salvavam arquivos em um formato de arquivo binário proprietário (.vsd) ou em um formato de arquivo de documento XML do Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="238a7-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="238a7-109">O Visio 2013 apresenta um novo formato de arquivo (.vsdx), que é baseado nas tecnologias de arquivo XML e ZIP.</span><span class="sxs-lookup"><span data-stu-id="238a7-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="238a7-110">Assim como nas versões anteriores do Visio, os arquivos são salvos em um único contêiner.</span><span class="sxs-lookup"><span data-stu-id="238a7-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="238a7-111">Ao contrário dos arquivos legados, no entanto, o novo formato de arquivo pode ser aberto, lido, atualizado, modificado e construído sem automatizar o aplicativo Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="238a7-112">Os desenvolvedores familiarizados com a manipulação de XML ou com o namespace [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) podem começar a trabalhar rapidamente com o novo formato de arquivo por meio de programação.</span><span class="sxs-lookup"><span data-stu-id="238a7-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="238a7-113">Os desenvolvedores que trabalharam com o formato de desenho do Visio XML de versões anteriores podem encontrar muitos estruturas desse formato mantidos no novo formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="238a7-114">Neste artigo, examinamos como trabalhar com o formato de arquivo do Visio 2013 programaticamente, usando o Microsoft .NET Framework 4.5, C # ou Visual Basic e o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="238a7-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="238a7-115">Você pode ver como abrir o arquivo do Visio 2013, selecionar partes do documento dentro do arquivo, alterar dados em partes e criar uma nova parte do documento.</span><span class="sxs-lookup"><span data-stu-id="238a7-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="238a7-116">As amostras de código neste artigo pressupõem que você tenha uma compreensão rudimentar de classes nas namespaces [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) e [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx).</span><span class="sxs-lookup"><span data-stu-id="238a7-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) and [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespaces.</span></span> <span data-ttu-id="238a7-117">> Este artigo supõe também que você compreende conceitos e terminologia das Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="238a7-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="238a7-118">Você deve ter alguma familiaridade com os conceitos de pacotes, partes do documento ou partes do pacote e relacionamentos.</span><span class="sxs-lookup"><span data-stu-id="238a7-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="238a7-119">Para saber mais, confira [OPC: um novo padrão para os dados de embalagem](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="238a7-119">For more information, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="238a7-120">> O código demonstra como criar consultas LINQ (integrada à linguagem de consulta) para selecionar o XML.</span><span class="sxs-lookup"><span data-stu-id="238a7-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="238a7-121">A maioria dos exemplos de código usa a sintaxe de consulta para criar consultas LINQ.</span><span class="sxs-lookup"><span data-stu-id="238a7-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="238a7-122">Você pode reescrever qualquer uma das consultas LINQ fornecidas no código usando a sintaxe do método LINQ, se necessário.</span><span class="sxs-lookup"><span data-stu-id="238a7-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="238a7-123">Confira mais informações sobre sintaxe de consulta LINQ e método sintaxe em [Sintaxe de consulta LINQ versus sintaxe de método (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Tabela 1 mostra tópicos essenciais que você devem estar familiarizado antes de trabalhar com este artigo.</span><span class="sxs-lookup"><span data-stu-id="238a7-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="238a7-124">**Tabela 1. Conceitos fundamentais para a manipulação do formato de arquivo do Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="238a7-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="238a7-125">**Título do artigo**</span><span class="sxs-lookup"><span data-stu-id="238a7-125">**Article title**</span></span>|<span data-ttu-id="238a7-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="238a7-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="238a7-127">Introdução ao formato de arquivo do Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="238a7-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="238a7-128">Esta visão geral descreve alguns dos principais recursos do formato de arquivo do Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="238a7-129">Ele discute as Open Packaging Conventions (OPC) e como elas foram aplicadas ao formato de arquivo do Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="238a7-130">Também lista algumas diferenças entre o formato de arquivo do Visio 2013 e o formato de arquivo anterior do desenho do Visio XML (. vdx).</span><span class="sxs-lookup"><span data-stu-id="238a7-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="238a7-131">OPC: Um novo padrão para sua embalagem de dados</span><span class="sxs-lookup"><span data-stu-id="238a7-131">OPC: A New Standard for Packaging Your Data</span></span>](https://msdn.microsoft.com/magazine/cc163372.aspx) <br/> |<span data-ttu-id="238a7-132">Este artigo da MSDN revista descreve as Open Packaging Conventions como um conceito.</span><span class="sxs-lookup"><span data-stu-id="238a7-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|[<span data-ttu-id="238a7-133">Conceitos básicos das Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="238a7-133">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx) <br/> [<span data-ttu-id="238a7-134">Apresentando os formatos de arquivo Open XML (2007) do Office</span><span class="sxs-lookup"><span data-stu-id="238a7-134">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx) <br/> |<span data-ttu-id="238a7-135">Esses dois artigos discutem como as Open Packaging Conventions foram aplicadas aos arquivos do Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="238a7-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="238a7-136">Eles contêm descrições de como os relacionamentos funcionam em um pacote e também incluem alguns exemplos de código.</span><span class="sxs-lookup"><span data-stu-id="238a7-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="238a7-137">Criar um arquivo. vsdx e uma nova solução do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="238a7-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="238a7-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span></span>

<span data-ttu-id="238a7-139">Antes de começar a seguir os procedimentos deste artigo, você precisa criar um arquivo do Visio 2013 para abrir e manipular.</span><span class="sxs-lookup"><span data-stu-id="238a7-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="238a7-140">O desenho usado nos exemplos de código deste artigo contém uma única página com duas formas conectadas, uma das formas sendo uma forma "Início / fim" do modelo "Fluxograma básico".</span><span class="sxs-lookup"><span data-stu-id="238a7-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="238a7-141">Use o procedimento a seguir para criar um novo arquivo do Visio 2013 para usar nos demais procedimentos deste artigo.</span><span class="sxs-lookup"><span data-stu-id="238a7-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="238a7-142">Para criar um novo arquivo do Visio 2013</span><span class="sxs-lookup"><span data-stu-id="238a7-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="238a7-143">Abra o Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="238a7-144">Criar um novo documento baseado no modelo fluxograma básico escolhendo **CATEGORIAS**, **Fluxograma**, **Fluxograma Básico**, **Criar**.</span><span class="sxs-lookup"><span data-stu-id="238a7-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="238a7-145">Na janela **Formas**, arraste um formato **inicial/final** para a tela.</span><span class="sxs-lookup"><span data-stu-id="238a7-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="238a7-146">Selecione a nova forma Start / End na tela de desenho e digite 'Iniciar Processo'.</span><span class="sxs-lookup"><span data-stu-id="238a7-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="238a7-147">Na janela **Formas**, arraste um formato **Processo** para a tela.</span><span class="sxs-lookup"><span data-stu-id="238a7-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="238a7-148">Selecione a nova forma de processo na tela de desenho e digite "Executar algumas tarefas".</span><span class="sxs-lookup"><span data-stu-id="238a7-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="238a7-149">No menu de atalho para a forma inicial/final, selecione **Um Conector para a Página**e, em seguida, desenhe um conector entre as formas Início/Fim e Processo na tela, conforme mostrado na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="238a7-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="238a7-150">**Figura 1. Simples desenho do Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="238a7-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![Uma forma Início/Fim conectada a uma forma de processo](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="238a7-152">Salve o arquivo na Area de trabalho como um arquivo. vsdx escolhendo **Arquivo**, **Salvar como**, **Computador**, **Área de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="238a7-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="238a7-153">Na caixa de diálogo **Salvar como**, digite o pacote do Visio na caixa **Nome do arquivo**, selecione **desenho do Visio (\*. vsdx)** na lista**Salvar como tipo** e, em seguida, escolha o botão **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="238a7-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="238a7-154">Fechar o arquivo e, em seguida, feche o Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="238a7-155">Às vezes, o Visio abre o arquivo com êxito, mesmo se houver problemas com o arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="238a7-156">Para garantir que o Visio notifique você sobre qualquer problema de arquivo, ative os avisos de abertura de arquivo ao testar as soluções que manipulam os arquivos do Visio no nível do pacote de arquivos.</span><span class="sxs-lookup"><span data-stu-id="238a7-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="238a7-157">> Para ativar os avisos de abertura de arquivos, no Visio 2013, escolha,**Arquivo**, **Opções**, **Avançado**.</span><span class="sxs-lookup"><span data-stu-id="238a7-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="238a7-158">Em **Salvar/abrir**, selecione **Mostrar avisos de abertura de arquivo**.</span><span class="sxs-lookup"><span data-stu-id="238a7-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="238a7-159">Esses procedimentos usam um aplicativo de console do Windows para manipular arquivos "Visio Package.vsdx".</span><span class="sxs-lookup"><span data-stu-id="238a7-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="238a7-160">Use o procedimento a seguir para criar e configurar um novo aplicativo de console do Windows no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="238a7-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="238a7-161">Para criar uma nova solução no Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="238a7-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="238a7-162">No menu **Arquivo**, clique em **Novo**, **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="238a7-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="238a7-163">Na caixa de diálogo**novo projeto**, expanda uma \*\*Visual C# \*\* ou **Visual Basic** e escolha **Windows**, **Console aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="238a7-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="238a7-164">Na caixa**nome**, digite "VisioFileAccessor", selecione um local para o projeto e, em seguida, escolha o botão **OK**.</span><span class="sxs-lookup"><span data-stu-id="238a7-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="238a7-165">No menu **Projeto**, escolha **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="238a7-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="238a7-166">Na caixa de diálogo **Gerenciador de Referência** em **Assemblies**, escolha **Estrutura**e adicionar uma referência para os componentes **System. XML** e **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="238a7-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="238a7-167">No arquivo Module. vb ou Module1 do projeto, adicione as seguintes diretivas**usando** (instruções**Imports** no Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="238a7-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
    ```cs
    using System.Xml;
    using System.Xml.Linq;
    using System.IO;
    using System.IO.Packaging;
    using System.Text;
    
    ```

    ```vb
    Imports System.Xml
    Imports System.Xml.Linq
    Imports System.IO
    Imports System.IO.Packaging
    Imports System.Text
    
    ```

5. <span data-ttu-id="238a7-168">Também no arquivo Module. vb ou Module1, antes do final do método **Principal** da classe **Programa** (**Module1** no Visual Basic), adicione o seguinte código que interrompe a execução do aplicativo de console até que o usuário pressione uma tecla.</span><span class="sxs-lookup"><span data-stu-id="238a7-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
    ```cs
    // This code stops the execution of the console application
    // so you can read the output.
    Console.WriteLine("Press any key to continue ...");
    Console.ReadKey();
    
    ```

    ```vb
    ' This code stops the execution of the console application
    ' so you can read the output.
    Console.WriteLine("Press any key to continue ...")
    Console.ReadKey()
    ```

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="238a7-169">Abrir um arquivo do Visio 2013 como um pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="238a7-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span></span>

<span data-ttu-id="238a7-171">Antes de manipular os dados no arquivo, você precisa primeiro abri-lo em um objeto [pacote](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx), que está incluído na namespace[System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx).</span><span class="sxs-lookup"><span data-stu-id="238a7-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) object, which is contained within the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace.</span></span> <span data-ttu-id="238a7-172">O objeto **pacote** representa o arquivo do Visio como um todo.</span><span class="sxs-lookup"><span data-stu-id="238a7-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="238a7-173">Ele expõe membros que permitem selecionar partes individuais do documento dentro do pacote de arquivos.</span><span class="sxs-lookup"><span data-stu-id="238a7-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="238a7-174">Em particular, a classe **Package** expõe o método estático [Open (String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) que você usa para abrir um arquivo como um pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) method that you use to open a file as a package.</span></span> <span data-ttu-id="238a7-175">Isso também expõe o método [Close ()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) para fechar o pacote assim que você terminar.</span><span class="sxs-lookup"><span data-stu-id="238a7-175">It also exposes a [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="238a7-176">Como prática recomendada, **use** o bloco de uso para abrir o arquivo do Visio no objeto **Package** para que você não precise fechar explicitamente o pacote de arquivos quando terminar.</span><span class="sxs-lookup"><span data-stu-id="238a7-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="238a7-177">Você também pode chamar explicitamente o método **Package.Close** no bloco **finally** de uma construção **try /catch/finally**.</span><span class="sxs-lookup"><span data-stu-id="238a7-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="238a7-178">Use o código a seguir para obter o caminho completo para o arquivo "Visio Package.vsdx" usando o objeto [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx), passe o caminho como um argumento para o método **Package.Open** e, em seguida, retorne ao objeto **Package** para o código de chamada.</span><span class="sxs-lookup"><span data-stu-id="238a7-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="238a7-179">Para abrir um arquivo. vsdx como um pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="238a7-180">Após o método **Main** na classe **Program** (ou **Module1** no Visual Basic), adicione o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static Package OpenPackage(string fileName, 
        Environment.SpecialFolder folder)
    {
        Package visioPackage = null;
        // Get a reference to the location 
        // where the Visio file is stored.
        string directoryPath = System.Environment.GetFolderPath(
            folder);
        DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
        // Get the Visio file from the location.
        FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
        if (fileInfos.Count() > 0)
        {
            FileInfo fileInfo = fileInfos[0];
            string filePathName = fileInfo.FullName;
            // Open the Visio file as a package with
            // read/write file access.
            visioPackage = Package.Open(
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite);
            }
            // Return the Visio file as a package.
            return visioPackage;
    }
    ```

    ```vb
    Private Function OpenPackage(fileName As String, _
        folder As Environment.SpecialFolder) As Package
        Dim visioPackage As Package = Nothing
        ' Get a reference to the location
        ' where the Visio file is stored.
        Dim directoryPath As String = System.Environment.GetFolderPath( _
            folder)
        Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
        ' Get the Visio file from the location.
        Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
        If (fileInfos.Count() > 0) Then
            Dim fileInfo As FileInfo = fileInfos(0)
            Dim filePathName As String = fileInfo.FullName
            ' Open the Visio file as a package 
            ' with read/write access.
            visioPackage = Package.Open( _
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite)
            End If
        ' Return the Visio file as a package.
        Return visioPackage
    End Function
    
    ```

2. <span data-ttu-id="238a7-181">No método **Main** da classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    // Open the Visio file in a Package object.
    using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
        Environment.SpecialFolder.Desktop))
    {
    }
    
    ```

    ```vb
    ' Open the Visio file in a Package object.
    Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
        Environment.SpecialFolder.Desktop)
    End Using
    
    ```

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="238a7-182">Selecione e leia as partes do pacote de um pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-182">Select and read package parts from a package</span></span>
<span data-ttu-id="238a7-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span></span>

<span data-ttu-id="238a7-184">Depois de abrir o arquivo do Visio 2013 como um pacote, você pode acessar as partes do documento usando a classe [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) incluída na namespace **System.IO.Packaging**.</span><span class="sxs-lookup"><span data-stu-id="238a7-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="238a7-185">Objetos **PackagePart** podem ser instanciados individualmente ou como uma coleção.</span><span class="sxs-lookup"><span data-stu-id="238a7-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="238a7-186">A classe **pacote** expõe um método [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) e um método [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) para obter objetos **PackagePart** fora do \*\* Pacote\*\*.</span><span class="sxs-lookup"><span data-stu-id="238a7-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="238a7-187">O método **GetParts** retornará uma instância da classe [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) classe. Você pode interagir com como qualquer outro conjunto que implementa a interface [IEnumerator \<T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2).</span><span class="sxs-lookup"><span data-stu-id="238a7-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) interface.</span></span> 
  
<span data-ttu-id="238a7-188">Use o código no procedimento a seguir para obter um objeto **PackagePartCollection** do **Pacote** como uma coleção, iterar pelos objetos **PackagePart** na coleção e gravar o URI e o tipo de conteúdo de cada **PackagePart** no console.</span><span class="sxs-lookup"><span data-stu-id="238a7-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="238a7-189">Para percorrer as partes do pacote em um pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="238a7-190">Após o método`OpenPackage` na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static void IteratePackageParts(Package filePackage)
    {
        
        // Get all of the package parts contained in the package
        // and then write the URI and content type of each one to the console.
        PackagePartCollection packageParts = filePackage.GetParts();
        foreach (PackagePart part in packageParts)
        {
            Console.WriteLine("Package part URI: {0}", part.Uri);
            Console.WriteLine("Content type: {0}", part.ContentType.ToString());
        }
    }
    
    ```

    ```vb
    Private Sub IteratePackageParts(filePackage As Package)
        ' Get all of the package parts contained in the package
        ' and then write the URI and content type of each one to the console.
        Dim packageParts As PackagePartCollection = filePackage.GetParts()
        For Each part In packageParts
            Console.WriteLine("Package part: {0}", part.Uri)
            Console.WriteLine("Content type: {0}", part.ContentType.ToString())
        Next
    End Sub 
    
    ```

2. <span data-ttu-id="238a7-191">Adicione o seguinte código dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="238a7-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. <span data-ttu-id="238a7-192">Escolha a tecla F5 para a solução de depuração.</span><span class="sxs-lookup"><span data-stu-id="238a7-192">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="238a7-193">Quando o programa estiver concluído, escolha qualquer tecla para sair.</span><span class="sxs-lookup"><span data-stu-id="238a7-193">When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="238a7-194">O aplicativo de console produz saída semelhante à seguinte (parte da saída foi omitida por brevidade):</span><span class="sxs-lookup"><span data-stu-id="238a7-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
<span data-ttu-id="238a7-195">Mais frequentemente, você precisará selecionar um **PackagePart** sem precisar iterar todos eles.</span><span class="sxs-lookup"><span data-stu-id="238a7-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="238a7-196">Você pode obter um objeto **PackagePart** de um **Pacote** usando sua relação com o **Pacote** ou outro **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="238a7-197">Um relacionamento no formato de arquivo do Visio 2013 é uma entidade discreta que descreve como uma parte do documento se relaciona com o pacote de arquivos ou como duas partes do documento se relacionam entre si.</span><span class="sxs-lookup"><span data-stu-id="238a7-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="238a7-198">Por exemplo, o pacote de arquivos do Visio 2013 em si tem um relacionamento com a parte do documento do Visio e a parte do documento do Visio tem um relacionamento com a parte do Windows.</span><span class="sxs-lookup"><span data-stu-id="238a7-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="238a7-199">Essas relações são representadas como instâncias das classes[PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) ou [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx).</span><span class="sxs-lookup"><span data-stu-id="238a7-199">These relationships are represented as instances of the [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) or [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) classes.</span></span> 
  
<span data-ttu-id="238a7-200">A classe **Pacote** expõe vários métodos para obter os relacionamentos que ela contém como objetos **PackageRelationship** ou **PackageRelationshipCollection**.</span><span class="sxs-lookup"><span data-stu-id="238a7-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="238a7-201">Você pode usar o método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) para criar uma instância de um objeto**PackageRelationshipCollection** que contém objetos **PackageRelationship** de um único tipo específico.</span><span class="sxs-lookup"><span data-stu-id="238a7-201">You can use the [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="238a7-202">Claro, usar o método **Package.GetRelationshipsByType** requer que você já saiba o tipo de relação necessárias.</span><span class="sxs-lookup"><span data-stu-id="238a7-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="238a7-203">Os tipos de relacionamento são sequências no formato de namespace XML.</span><span class="sxs-lookup"><span data-stu-id="238a7-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="238a7-204">Por exemplo, o tipo de relação de parte do documento Visio é http://schemas.microsoft.com/visio/2010/relationships/document.</span><span class="sxs-lookup"><span data-stu-id="238a7-204">For example, the relationship type of the Visio Document part is http://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="238a7-205">Depois que você sabe a relação de um **PackagePart** com o **Pacote** ou outra **PackagePart** (ou seja, você tem um objeto **PackageRelationship**que faz referência ao **PackagePart** desejado), você pode usar essa relação obter o URI desse **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-205">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**.</span></span> <span data-ttu-id="238a7-206">Passar URI para o método **GetPart** para retornar a **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-206">You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="238a7-207">Você também pode obter uma referência a uma determinada **PackagePart** usando apenas o método **GetPart** e o URI das **PackagePart**, ignorando a etapa em que você obtém os relacionamentos da parte do pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="238a7-208">No entanto, algumas partes do pacote no pacote de arquivos do Visio podem ser salvas em locais diferentes de seus locais padrão em um pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="238a7-209">Você não pode presumir que uma parte do pacote esteja sempre localizada no mesmo URI para todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="238a7-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="238a7-210">> Em vez disso, a prática recomendada é usar relações para acessar objetos individuais **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="238a7-211">Use o procedimento a seguir para obter uma **PackagePart** (a parte do documento Visio) usando o **PackageRelationship** do **pacote** que faz referência a parte.</span><span class="sxs-lookup"><span data-stu-id="238a7-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="238a7-212">Para selecionar uma parte específica do pacote no pacote por relação</span><span class="sxs-lookup"><span data-stu-id="238a7-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="238a7-213">Após o método`IteratePackageParts` na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        string relationship)
    {
        
        // Use the namespace that describes the relationship 
        // to get the relationship.
        PackageRelationship packageRel = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart part = null;
        // If the Visio file package contains this type of relationship with 
        // one of its parts, return that part.
        if (packageRel != null)
        {
            // Clean up the URI using a helper class and then get the part.
            Uri docUri = PackUriHelper.ResolvePartUri(
                new Uri("/", UriKind.Relative), packageRel.TargetUri);
            part = filePackage.GetPart(docUri);
        }
        return part;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, relationship As String) _
        As PackagePart
        ' Use the namespace that describes the relationship 
        ' to get the relationship.
        Dim packageRel As PackageRelationship = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
        Dim part As PackagePart = Nothing
        ' If the Visio file package contains this type of relationship with 
        ' one of its parts, return that part.
        If Not IsNothing(packageRel) Then
            ' Clean up the URI using a helper class and then get the part.
            Dim docUri = PackUriHelper.ResolvePartUri( _
                New Uri("/", UriKind.Relative), packageRel.TargetUri)
            part = filePackage.GetPart(docUri)
        End If
        Return part
    End Function
    
    ```

2. <span data-ttu-id="238a7-214">Substitua o seguinte código dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic) com o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "http://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "http://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

<span data-ttu-id="238a7-215">Conforme mencionado anteriormente, você também pode obter objetos **PackagePart** usando a relação com outros objetos**PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="238a7-216">Isso é importante porque, para um documento do Visio de qualquer complexidade, a maioria dos objetos **PackagePart** não tem um relacionamento com o **Package**.</span><span class="sxs-lookup"><span data-stu-id="238a7-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="238a7-217">Por exemplo, uma parte individual do Conteúdo da Página no pacote de arquivos (ou seja, /visio/pages/page1.xml) tem um relacionamento com a parte do Índice da Página (ou seja, /visio/pages/pages.xml), mas não com o pacote de arquivos em si.</span><span class="sxs-lookup"><span data-stu-id="238a7-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="238a7-218">Se você não tiver o URI exato da página individual no pacote, você pode usar sua relação com a parte do Índice de Página para obter uma referência a ela.</span><span class="sxs-lookup"><span data-stu-id="238a7-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="238a7-219">A classe **PackagePart** expõe um método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) que você pode usar para voltar um objeto **PackageRelationshipCollection** que contém apenas um tipo de objeto **PackageRelationship**.</span><span class="sxs-lookup"><span data-stu-id="238a7-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="238a7-220">Quando você tiver a **PackageRelationshipCollection**, você pode selecionar a **PackageRelationship** do conjunto de e, em seguida, fazer referência ao objeto**PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="238a7-221">Use o seguinte código para obter uma **PackagePart** do **Package** usando sua relação com (obter um objeto **PackageRelationship** a partir de) outro \*\* PackagePart\*\*.</span><span class="sxs-lookup"><span data-stu-id="238a7-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="238a7-222">Para selecionar uma parte específica do pacote através de sua relação com outra parte do pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="238a7-223">Após o método `GetPackagePart` na classe **Program** (ou **Module1** no Visual Basic), adicione o seguinte método de sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="238a7-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        PackagePart sourcePart, string relationship)
    {
        // This gets only the first PackagePart that shares the relationship
        // with the PackagePart passed in as an argument. You can modify the code
        // here to return a different PackageRelationship from the collection.
        PackageRelationship packageRel = 
            sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart relatedPart = null;
        if (packageRel != null)
        {
            // Use the PackUriHelper class to determine the URI of PackagePart
            // that has the specified relationship to the PackagePart passed in
            // as an argument.
            Uri partUri = PackUriHelper.ResolvePartUri(
                sourcePart.Uri, packageRel.TargetUri);
            relatedPart = filePackage.GetPart(partUri);
        }
        return relatedPart;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, 
        sourcePart As PackagePart, relationship As String) As PackagePart
        ' This gets only the first PackagePart that shares the relationship
        ' with the PackagePart passed in as an argument. You can modify the
        ' code to return a different PackageRelationship from the collection.
        Dim packageRel As PackageRelationship = sourcePart. _
            GetRelationshipsByType(relationship).FirstOrDefault()
        Dim relatedPart As PackagePart = Nothing
        If Not IsNothing(packageRel) Then
            ' Use the PackUriHelper class to determine the URI of the 
            ' PackagePart that has the specified relationship to the 
            ' PackagePart passed in as an argument.
            Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
                sourcePart.Uri, packageRel.TargetUri)
            relatedPart = filePackage.GetPart(partUri)
        End If
        Return relatedPart
    End Function
    ```

2. <span data-ttu-id="238a7-224">Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="238a7-224">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> <span data-ttu-id="238a7-225">(Não exclua o código que você adicionou no procedimento anterior).</span><span class="sxs-lookup"><span data-stu-id="238a7-225">(Do not delete the code that you added in the previous procedure.)</span></span> 
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "http://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "http://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "http://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "http://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

<span data-ttu-id="238a7-226">Antes de poder fazer alterações no XML incluído em uma parte do documento, primeiro é necessário carregar o documento XML em um objeto que permita a leitura do XML, usando a classe [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) ou a classe [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx).</span><span class="sxs-lookup"><span data-stu-id="238a7-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="238a7-227">Ambas as classes expõem métodos para tarefas como selecionar elementos XML contidos nos documentos XML; criar, ler e escrever atributos; e inserir novos elementos XML em um documento.</span><span class="sxs-lookup"><span data-stu-id="238a7-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="238a7-228">Dos dois, a classe **XDocument** permite consultar o XML usando LINQ.</span><span class="sxs-lookup"><span data-stu-id="238a7-228">Of the two, the **XDocument** class allows you to query the XML using LINQ.</span></span> <span data-ttu-id="238a7-229">Com o LINQ, você pode selecionar facilmente elementos individuais de um documento XML criando consultas, em vez de iterar sobre todos os elementos de uma coleção e testando os elementos de que precisa.</span><span class="sxs-lookup"><span data-stu-id="238a7-229">With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need.</span></span> <span data-ttu-id="238a7-230">Por esse motivo, os procedimentos a seguir neste artigo usam a classe **XDocument** e outras classes da namespace **System.Xml.Linq** para trabalhar com o XML.</span><span class="sxs-lookup"><span data-stu-id="238a7-230">For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="238a7-231">Use o procedimento a seguir para abrir um **PackagePart** como um documento XML em um objeto**XDocument**.</span><span class="sxs-lookup"><span data-stu-id="238a7-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="238a7-232">Para ler o XML de uma parte do pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="238a7-233">Após a última sobrecarga para o `GetPackagePart` método na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static XDocument GetXMLFromPart(PackagePart packagePart)
    {
        XDocument partXml = null;
        // Open the packagePart as a stream and then 
        // open the stream in an XDocument object.
        Stream partStream = packagePart.GetStream();
        partXml = XDocument.Load(partStream);
        return partXml;
    }
    ```

    ```vb
    Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
        Dim partXml As XDocument = Nothing
        ' Open the packagePart as a stream and then
        ' open the stream in an an XDocument object.
        Dim partStream As Stream = packagePart.GetStream()
        partXml = XDocument.Load(partStream)
        Return partXml
    End Function
    ```

2. <span data-ttu-id="238a7-234">Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="238a7-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="238a7-235">Selecionar e alterar dados XML em uma parte do pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="238a7-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span></span>

<span data-ttu-id="238a7-237">Depois de carregar uma parte do documento em um objeto**XDocument**, você pode usar o LINQ para selecionar elementos XML e fazer alterações no documento XML.</span><span class="sxs-lookup"><span data-stu-id="238a7-237">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document.</span></span> <span data-ttu-id="238a7-238">Você pode usar o LINQ para solicitar elementos XML e fazer alterações no documento XML.</span><span class="sxs-lookup"><span data-stu-id="238a7-238">You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="238a7-239">A tarefa mais comum para manipular o formato de arquivo do Visio é selecionar elementos XML específicos ou coleções de elementos no documento.</span><span class="sxs-lookup"><span data-stu-id="238a7-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="238a7-240">A namespace **System.Xml.Linq** inclui a classe[XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx), que representa um elemento XML.</span><span class="sxs-lookup"><span data-stu-id="238a7-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="238a7-241">A classe **XElement**oferece acesso aos dados contidos no arquivo do Visio em um nível granular, de elementos individuais **Shape** a elementos **ValidationRule** (como exemplos).</span><span class="sxs-lookup"><span data-stu-id="238a7-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="238a7-242">Use o código a seguir para selecionar os elementos **Shape** de um **XDocument** (contendo uma parte do Conteúdo da Página) e, em seguida, selecione um elemento **Shape** específico.</span><span class="sxs-lookup"><span data-stu-id="238a7-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="238a7-243">Para selecionar um elemento específico em uma parte do pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="238a7-244">Após o método`GetXMLFromPart` na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
        
    ```cs
    private static IEnumerable<XElement> GetXElementsByName(
        XDocument packagePart, string elementType)
    {
        // Construct a LINQ query that selects elements by their element type.
        IEnumerable<XElement> elements = 
            from element in packagePart.Descendants() 
            where element.Name.LocalName == elementType 
            select element;
        // Return the selected elements to the calling code.
        return elements.DefaultIfEmpty(null);
    }
    
    ```

    ```vb
    Private Function GetXElementsByName(partXML As XDocument, _
        elementType As String) As IEnumerable(Of XElement)
        ' Construct a LINQ query that selects elements by their element type.
        Dim elements As IEnumerable(Of XElement) =
            From element In partXML.Descendants()
            Where element.Name.LocalName = elementType
            Select element
        ' If there aren't any elements of the specified type
        ' in the document, return Nothing to the calling code.
        Return elements.DefaultIfEmpty(Nothing)
    End Function
    ```

2. <span data-ttu-id="238a7-245">Após o método`GetXElementsByName` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
        string attributeName, string attributeValue) 
    {
        // Construct a LINQ query that selects elements from a group
        // of elements by the value of a specific attribute.
        IEnumerable<XElement> selectedElements = 
            from el in elements
            where el.Attribute(attributeName).Value == attributeValue
            select el;
        // If there aren't any elements of the specified type
        // with the specified attribute value in the document,
        // return null to the calling code.
        return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
    }
    ```

    ```vb
    Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
        attributeName As String, attributeValue As String) As XElement
        ' Construct a LINQ query that selects elements from a group
        ' of elements by the value of a specific attribute.
        Dim selectedElements As IEnumerable(Of XElement) =
            From el In elements
            Where el.Attribute(attributeName).Value = attributeValue
            Select el
        ' If there aren't any elements of the specified type 
        ' with the specified attribute value in the document,
        ' return Nothing to the calling code.
        Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
    End Function
    
    ```

3. <span data-ttu-id="238a7-246">Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="238a7-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Get all of the shapes from the page by getting
    // all of the Shape elements from the pageXML document.
    IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
    // Select a Shape element from the shapes on the page by 
    // its name. You can modify this code to select elements
    // by other attributes and their values.
    XElement startEndShapeXML = 
        GetXElementByAttribute(shapesXML, "NameU", "Start/End");
    
    ```

    ```vb
    ' Get all of the shapes from the page by getting
    ' all of the Shape elements from the pageXML document.
    Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
        pageXML, "Shape")
    ' Select a Shape element from the shapes on the page by
    ' its name. You can modify this code to select elements
    ' by other attributes and their values.
    Dim startEndShapeXML As XElement = GetXElementByAttribute( _
        shapesXML, "NameU", "Start/End")
    ```

<span data-ttu-id="238a7-247">Depois de obter uma referência a um objeto **XElement** contido em um objeto **XDocument**, você poderá manipulá-lo como qualquer outro dado XML e, assim, alterar os dados contidos no arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="238a7-248">Por exemplo, se uma forma tiver texto quando ele é aberto no Visio, o elemento **Forma** correspondente inclui pelo menos um elemento **Texto**.</span><span class="sxs-lookup"><span data-stu-id="238a7-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="238a7-249">Se você alterar o valor desse elemento **Texto**, o texto da forma será alterado quando o arquivo for exibido no Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="238a7-250">Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), 
para alterar o texto na forma Início/Fim de "Começar processo" para "Iniciar processo".</span><span class="sxs-lookup"><span data-stu-id="238a7-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> <span data-ttu-id="238a7-251">No exemplo de código anterior, o texto da forma existente e a cadeia de caracteres usada para substituí-lo têm o mesmo número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="238a7-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="238a7-252">Observe também que a consulta LINQ altera o valor do último nó filho do elemento retornado (que, nesse caso, é um nó de texto).</span><span class="sxs-lookup"><span data-stu-id="238a7-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="238a7-253">Isso é feito para evitar alterar as configurações do elemento **cp** que é filho do elemento **texto**.</span><span class="sxs-lookup"><span data-stu-id="238a7-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="238a7-254">> É possível causar instabilidade no arquivo se você alterar o texto da forma programaticamente sobrescrevendo todos os filhos do elemento **Texto**.</span><span class="sxs-lookup"><span data-stu-id="238a7-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="238a7-255">Como no exemplo acima, a formatação do texto é representada por elementos **cp** no elemento**Texto** no arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="238a7-256">A definição da formatação é armazenada no elemento pai**Section**.</span><span class="sxs-lookup"><span data-stu-id="238a7-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="238a7-257">Se essas duas informações se tornarem inconsistentes, o arquivo poderá não se comportar como esperado.</span><span class="sxs-lookup"><span data-stu-id="238a7-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="238a7-258">O Visio cura muitas inconsistências, mas é melhor garantir que as alterações programáticas sejam consistentes para que você controle o comportamento final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="238a7-259">Quando você faz alterações no XML de uma parte do documento, essas alterações existem apenas na memória.</span><span class="sxs-lookup"><span data-stu-id="238a7-259">When you make changes to the XML of a document part, those changes exist in memory only.</span></span> <span data-ttu-id="238a7-260">Para persistir as alterações no arquivo, você deve salvar o XML de volta na parte do documento.</span><span class="sxs-lookup"><span data-stu-id="238a7-260">To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="238a7-261">O código a seguir usa a classe [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) e a classe [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) para gravar o XML de volta para a parte do pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="238a7-262">Embora você possa usar o método [Save ()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) para salvar o XML de volta à peça, as classes **XmlWriter** e **XmlWriterSettings** permitem um melhor controle sobre a saída, incluindo a especificação do tipo de codificação.</span><span class="sxs-lookup"><span data-stu-id="238a7-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="238a7-263">A classe **XDocument** expõe um método [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) que usa um objeto **XmlWriter** 
e grava XML de volta para um fluxo.</span><span class="sxs-lookup"><span data-stu-id="238a7-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="238a7-264">Use o procedimento a seguir para salvar o XML da página do Visio de volta à parte do Conteúdo da Página.</span><span class="sxs-lookup"><span data-stu-id="238a7-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="238a7-265">Para salvar o XML alterado de volta ao pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="238a7-266">Após o método`GetXElementByAttribute` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void SaveXDocumentToPart(PackagePart packagePart, 
        XDocument partXML)
    {
        
        // Create a new XmlWriterSettings object to 
        // define the characteristics for the XmlWriter
        XmlWriterSettings partWriterSettings = new XmlWriterSettings();
        partWriterSettings.Encoding = Encoding.UTF8;
        // Create a new XmlWriter and then write the XML
        // back to the document part.
        XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
            partWriterSettings);
        partXML.WriteTo(partWriter);
        // Flush and close the XmlWriter.
        partWriter.Flush();
        partWriter.Close();
    }
    ```

    ```vb
    Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
        partXML As XDocument)
        ' Create a new XmlWriterSettings object to 
        ' define the characteristics for the XmlWriter.
        Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
        partWriterSettings.Encoding = Encoding.UTF8
        ' Create a new XmlWriter and then write the XML
        ' back to the document part.
        Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
        partXML.WriteTo(partWriter)
        ' Flush and close the XmlWriter.
        partWriter.Flush()
        partWriter.Close()
    End Sub
    ```

2. <span data-ttu-id="238a7-267">Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="238a7-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. <span data-ttu-id="238a7-268">Escolha a tecla F5 para a solução de depuração.</span><span class="sxs-lookup"><span data-stu-id="238a7-268">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="238a7-269">Quando o programa estiver concluído, escolha qualquer tecla para sair.</span><span class="sxs-lookup"><span data-stu-id="238a7-269">When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="238a7-270">Abra o arquivo do Visio Package.vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="238a7-271">A forma Início/Fim agora deve conter o texto "Iniciar processo".</span><span class="sxs-lookup"><span data-stu-id="238a7-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="238a7-272">Recalcular os dados no arquivo</span><span class="sxs-lookup"><span data-stu-id="238a7-272">Recalculate data in the file</span></span>
<span data-ttu-id="238a7-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span></span>

<span data-ttu-id="238a7-274">Algumas alterações nos dados em um arquivo podem exigir que o Visio recalcule o documento quando ele abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="238a7-275">O Visio fornece muita lógica para um diagrama, principalmente para relacionamentos de forma (ou seja, quando uma forma depende de outra) e para a conexão de formas.</span><span class="sxs-lookup"><span data-stu-id="238a7-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="238a7-276">Se qualquer um dos dados que a lógica personalizada depende for alterado, o Visio precisa propagar as alterações para todos os dados calculados afetados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="238a7-277">O formato de arquivo do Visio 2013 inclui algumas técnicas que podem ser usados para calcular novamente os dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="238a7-278">Existem três tipos de cenários que você deve considerar ao decidir se precisa recalcular o arquivo do Visio e como fazê-lo:</span><span class="sxs-lookup"><span data-stu-id="238a7-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="238a7-279">As alterações para os dados não afetam os valores no formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="238a7-280">Não é necessário adicionar as instruções adicionais ao Visio para calcular novamente o documento.</span><span class="sxs-lookup"><span data-stu-id="238a7-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="238a7-281">Como demonstrado anteriormente, muitas vezes você pode alterar o texto da forma sem precisar recalcular o documento.</span><span class="sxs-lookup"><span data-stu-id="238a7-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="238a7-282">As alterações nos dados limitam-se a alterar os valores das células ShapeSheet no XML, e há outros valores ShapeSheet que dependem desses dados.</span><span class="sxs-lookup"><span data-stu-id="238a7-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="238a7-283">Nesse caso, você deve adicionar uma instrução de processamento de XML (usando a classe [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)) para o elemento**célula** que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="238a7-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="238a7-284">Por exemplo, a célula **ThemeIndex** de uma forma afeta os valores de várias outras células ShapeSheet contidas na forma.</span><span class="sxs-lookup"><span data-stu-id="238a7-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="238a7-285">Se você alterar a célula **ThemeIndex** dentro do próprio arquivo (por exemplo, o elemento **célula** com um valor**N** de "ThemeIndex"), será necessário adicionar um instruções de processamento para o elemento **célula** para que sejam atualizados valores dependentes.</span><span class="sxs-lookup"><span data-stu-id="238a7-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="238a7-286">As alterações nos dados afetam a localização de um conector ou pontos de conexão.</span><span class="sxs-lookup"><span data-stu-id="238a7-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="238a7-287">Outra situação é quando há muitas alterações nos dados da ShapeSheet e você deseja recalcular o documento inteiro com uma instrução (em vez de adicionar instruções de processamento individuais para cada alteração).</span><span class="sxs-lookup"><span data-stu-id="238a7-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="238a7-288">Nesse caso, você pode instruir o Visio a recalcular todo o documento quando ele é aberto.</span><span class="sxs-lookup"><span data-stu-id="238a7-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="238a7-289">Para fazer isso, adicione uma propriedade **RecalcDocument** para a parte de propriedades do arquivo personalizado (/ docProps) do pacote do Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="238a7-290">Ajustar a posição ou o tamanho das formas em um diagrama conectado é um exemplo desse tipo de cenário.</span><span class="sxs-lookup"><span data-stu-id="238a7-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="238a7-291">Tenha em mente que esta é a opção mais custosa do ponto de vista do desempenho.</span><span class="sxs-lookup"><span data-stu-id="238a7-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="238a7-292">Use o procedimento a seguir para inserir um elemento **Célula** em um elemento **Forma**, onde outros elementos **Célula** na mesma **Forma** precisam ser recalculados devido ao novo valor.</span><span class="sxs-lookup"><span data-stu-id="238a7-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="238a7-293">O novo elemento**Célula** inclui uma instrução de processamento como um elemento filho, para informar ao Visio que ele precisa executar algum recálculo local.</span><span class="sxs-lookup"><span data-stu-id="238a7-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="238a7-294">Para recalcular os valores para uma única forma</span><span class="sxs-lookup"><span data-stu-id="238a7-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="238a7-295">Substitua o código dos dois exemplos anteriores (alterando o texto da forma e a chamada para `SaveXDocumentToPart`) no bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Módulo1** no Visual Basic) com o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Insert a new Cell element in the Start/End shape that adds an arbitrary
    // local ThemeIndex value. This code assumes that the shape does not 
    // already have a local ThemeIndex cell.
    startEndShapeXML.Add(new XElement("Cell",
        new XAttribute("N", "ThemeIndex"),
        new XAttribute("V", "25"),
        new XProcessingInstruction("NewValue", "V")));
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Insert a new Cell element in the shape that adds an arbitrary local
    ' ThemeIndex value. This code assumes that the shape does not
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. <span data-ttu-id="238a7-296">Escolha a tecla F5 para a solução de depuração.</span><span class="sxs-lookup"><span data-stu-id="238a7-296">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="238a7-297">Quando o programa estiver concluído, escolha qualquer tecla para sair.</span><span class="sxs-lookup"><span data-stu-id="238a7-297">When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="238a7-298">Abra o arquivo do Visio Package.vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="238a7-299">A forma Início/Fim agora deve ter uma cor de preenchimento diferente.</span><span class="sxs-lookup"><span data-stu-id="238a7-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="238a7-300">A cor da forma depende do valor da célula **ThemeIndex** ela determina de qual dos temas ativos a forma é herdada.</span><span class="sxs-lookup"><span data-stu-id="238a7-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="238a7-301">No exemplo anterior, a forma é definida para herdar de um tema diferente (a célula **ThemeIndex** é definida para um valor de "25").</span><span class="sxs-lookup"><span data-stu-id="238a7-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="238a7-302">Se você não usar uma instrução de processamento, a cor do texto da forma - que também é afetada pela célula **ThemeIndex** - não é recalculada.</span><span class="sxs-lookup"><span data-stu-id="238a7-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="238a7-303">A cor de preenchimento da forma mudaria para branco, mas seu texto permaneceria branco - deixando o texto ilegível.</span><span class="sxs-lookup"><span data-stu-id="238a7-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="238a7-304">Além disso, sem a instrução de processamento, é possível que o Visio possa atualizar a forma em uma data posterior, deixando o arquivo em um estado instável onde os valores de formatação da forma podem ser atualizados imprevisivelmente.</span><span class="sxs-lookup"><span data-stu-id="238a7-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="238a7-305">Se você alterar dados no arquivo que exige o Visio para recalcular o documento (por exemplo, alterando a posição de uma forma conectada e, portanto, forçando os conectores a redirecionar), você deve adicionar uma instrução de recálculo ao arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="238a7-306">A instrução é criada adicionando um elemento de**propriedade** com um valor de atributo de **nome**  "RecalcDocument" ao XML da parte Custom File Properties do pacote de arquivos do Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="238a7-307">Como prática recomendada, você deve verificar a parte Propriedades de Arquivos Personalizados para ter certeza de que uma instrução "RecalcDocument" não foi registrada no arquivo.</span><span class="sxs-lookup"><span data-stu-id="238a7-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="238a7-308">Use o seguinte código para alterar o valor da célula**PinY** da forma Início/Fim dos exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="238a7-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="238a7-309">O código seleciona o elemento **célula** que contém a célula de dados **PinY**como um objeto **XElement** usando o valor de seu atributo **N**.</span><span class="sxs-lookup"><span data-stu-id="238a7-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="238a7-310">O código, em seguida, adiciona uma instrução de recálculo à parte Propriedades do arquivo personalizado do arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="238a7-311">O código aproveita os métodos `GetPackagePart` e `SaveXDocumentToPart` criados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="238a7-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="238a7-312">Para recalcular todo o documento quando ele é aberto</span><span class="sxs-lookup"><span data-stu-id="238a7-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="238a7-313">Após o método`SaveXDocumentToPart` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
            "custom-properties");
        XDocument customPartXML = GetXMLFromPart(customPart);
        // Check to see whether document recalculation has already been 
        // set for this document. If it hasn't, use the integer
        // value returned by CheckForRecalc as the property ID.
        int pidValue = CheckForRecalc(customPartXML);
        if (pidValue > -1)
        {
            XElement customPartRoot = customPartXML.Elements().ElementAt(0);
            // Two XML namespaces are needed to add XML data to this 
            // document. Here, we're using the GetNamespaceOfPrefix and 
            // GetDefaultNamespace methods to get the namespaces that 
            // we need. You can specify the exact strings for the 
            // namespaces, but that is not recommended.
            XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
            XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
            // Construct the XML for the new property in the XDocument.Add method.
            // This ensures that the XNamespace objects will resolve properly, 
            // apply the correct prefix, and will not default to an empty namespace.
            customPartRoot.Add(
                new XElement(customPropsSchemaNS + "property",
                    new XAttribute("pid", pidValue.ToString()),
                    new XAttribute("name", "RecalcDocument"),
                    new XAttribute("fmtid", 
                        "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                    new XElement(customVTypesNS + "bool", "true")
                ));
        }
        // Save the Custom Properties package part back to the package.
        SaveXDocumentToPart(customPart, customPartXML);
    }
    ```

    ```vb
    Private Sub RecalcDocument(filePackage As Package)
            ' Get the Custom File Properties part from the package and
            ' then extract the XML from it.
            Dim customPart As PackagePart = GetPackagePart(filePackage, _
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
                "relationships/custom-properties")
            Dim customPartXML As XDocument = GetXMLFromPart(customPart)
            ' Check to see whether document recalculation has already been
            ' set for this document. If it hasn't, use the integer
            ' value returned by CheckForRecalc as the property ID.
            Dim pidValue As Integer = CheckForRecalc(customPartXML)
            If (pidValue > 1) Then
                Dim customPartRoot As XElement = _
                    customPartXML.Elements().ElementAt(0)
                ' Two XML namespaces are needed to add XML data to this 
                ' document. Here, we're using the GetNamespaceOfPrefix and
                ' GetDefaultNamespace methods to get the namespaces that
                ' we need. You can specify the exact strings for the 
                ' namespaces, but that is not recommended.
                Dim customVTypesNS As XNamespace = _
                    customPartRoot.GetNamespaceOfPrefix("vt")
                Dim customPropsSchemaNS As XNamespace = _
                    customPartRoot.GetDefaultNamespace()
                ' Contruct the XML for the new property in the XDocument.Add
                ' method. This ensures that the XML namespaces resolve 
                ' properly, apply the correct prefix, and do not default to 
                ' an empty namespace.
                customPartRoot.Add( _
                    New XElement(customPropsSchemaNS + "property", _
                        New XAttribute("pid", pidValue.ToString()), _
                        New XAttribute("name", "RecalcDocument"), _
                        New XAttribute("fmtid", _
                            "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                        New XElement(customVTypesNS + "bool", "true") _
                ))
            ' Save the Custom Properties package part back to the package.
            SaveXDocumentToPart(customPart, customPartXML)
            End If
        End Sub
    ```

2. <span data-ttu-id="238a7-314">Após o método`RecalcDocument` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static int CheckForRecalc(XDocument customPropsXDoc) 
    {
        
        // Set the inital pidValue to -1, which is not an allowed value.
        // The calling code tests to see whether the pidValue is 
        // greater than -1.
        int pidValue = -1;
        // Get all of the property elements from the document. 
        IEnumerable<XElement> props = GetXElementsByName(
            customPropsXDoc, "property");
        // Get the RecalcDocument property from the document if it exists already.
        XElement recalcProp = GetXElementByAttribute(props, 
            "name", "RecalcDocument");
        // If there is already a RecalcDocument instruction in the 
        // Custom File Properties part, then we don't need to add another one. 
        // Otherwise, we need to create a unique pid value.
        if (recalcProp != null)
        {
            return pidValue;
        }
        else
        {
            // Get all of the pid values of the property elements and then
            // convert the IEnumerable object into an array.
            IEnumerable<string> propIDs = 
                from prop in props
                where prop.Name.LocalName == "property"
                select prop.Attribute("pid").Value;
            string[] propIDArray = propIDs.ToArray();
            // Increment this id value until a unique value is found.
            // This starts at 2, because 0 and 1 are not valid pid values.
            int id = 2;
            while (pidValue == -1)
            {
                if (propIDArray.Contains(id.ToString()))
                {
                    id++;
                }
                else
                {
                    pidValue = id;
                }
            }
        }
        return pidValue;
    }
    
    ```

    ```vb
    Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
        ' Set the initial pidValue to -1, which is not an allowed value. 
        ' The calling code test to see whether the pidValue is
        ' greater than -1.
        Dim pidValue As Integer = -1
        ' Get all of the property elements from the document.
        Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
            customPropsXDoc, "property")
        ' Get the RecalcDocument property from the document if 
        ' it exists already.
        Dim recalcProp As XElement = GetXElementByAttribute(props, _
            "name", "RecalcDocument")
        ' If there is already a RecalcDocument instruction in the 
        ' Custom File Properties part, then we don't need another one.
        ' Otherwise, we need to create a unique pid value.
        If Not IsNothing(recalcProp) Then
            Return pidValue
        Else
            ' Get all of the pid values of the proeprty elements and then
            ' convert the IEnumerable object into an array.
            Dim propIDs As IEnumerable(Of String) = _
            From prop In props
            Where prop.Name.LocalName = "property"
            Select prop.Attribute("pid").Value
            Dim propIDArray As String() = propIDs.ToArray()
            ' Increment this id value until a unique value is found.
            ' This starts at 2, because 0 and 1 are not valid pid values.
            Dim id As Integer = 2
            While (pidValue = -1)
                If (propIDArray.Contains(id.ToString())) Then
                    id = id + 1
                Else
                    pidValue = id
                End If
            End While
        End If
        Return pidValue
    End Function
    ```

3. <span data-ttu-id="238a7-315">Substitua o código do exemplo anterior dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic) com o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Change the shape's horizontal position on the page 
    // by getting a reference to the Cell element for the PinY 
    // ShapeSheet cell and changing the value of its V attribute.
    XElement pinYCellXML = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY");
    pinYCellXML.SetAttributeValue("V", "2");
    // Add instructions to Visio to recalculate the entire document
    // when it is next opened.
    RecalcDocument(visioPackage);
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Change the shape's horizontal position on the page
    ' by getting a reference to the Cell element for the PinY
    ' ShapeSheet cell and changing the value of its V attribute.
    Dim pinYCellXML As XElement = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY")
    pinYCellXML.SetAttributeValue("V", "2")
    ' Add instructions to Visio to recalculate the entire document
    ' when it is next opened.
    RecalcDocument(visioPackage)
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

4. <span data-ttu-id="238a7-316">Escolha a tecla F5 para a solução de depuração.</span><span class="sxs-lookup"><span data-stu-id="238a7-316">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="238a7-317">Quando o programa estiver concluído, escolha qualquer tecla para sair.</span><span class="sxs-lookup"><span data-stu-id="238a7-317">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="238a7-318">Abra o arquivo do Visio Package.vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="238a7-319">Agora a forma Início/Fim deve ser de 2 polegadas da borda inferior do desenho.</span><span class="sxs-lookup"><span data-stu-id="238a7-319">The Start/End shape should now be 2 inches from the bottom edge of the drawing.</span></span> <span data-ttu-id="238a7-320">O conector entre a forma Início/Fim e a forma Processo deve ter sido reencaminhado para acomodar a alteração no layout.</span><span class="sxs-lookup"><span data-stu-id="238a7-320">The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout.</span></span> <span data-ttu-id="238a7-321">Se a propriedade **RecalcDocument** não tivesse sido adicionada ao arquivo, a posição da forma teria sido alterada, mas o conector não teria sido reencaminhado para o novo local da forma.</span><span class="sxs-lookup"><span data-stu-id="238a7-321">If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="238a7-322">Adicionar uma nova parte do pacote para um pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-322">Add a new package part to a package</span></span>
<span data-ttu-id="238a7-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span></span>

<span data-ttu-id="238a7-324">Um dos cenários mais comuns para modificar um pacote de arquivos é adicionar uma nova parte do documento ao pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="238a7-325">Por exemplo, se você quiser adicionar uma página ao desenho do Visio adicionando conteúdo ao pacote, precisará adicionar uma parte do Conteúdo da Página ao pacote.</span><span class="sxs-lookup"><span data-stu-id="238a7-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="238a7-326">O processo para adicionar uma nova parte para o pacote é simples:</span><span class="sxs-lookup"><span data-stu-id="238a7-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="238a7-327">Criar o documento XML com os dados para o **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-327">You create the XML document with the data for the **PackagePart**.</span></span> <span data-ttu-id="238a7-328">Você precisa prestar atenção especial aos namespaces XML que controlam o esquema para o tipo específico de documento XML que você cria.</span><span class="sxs-lookup"><span data-stu-id="238a7-328">You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="238a7-329">Crie um novo arquivo para conter o XML e salvar o arquivo em um local no **Package**.</span><span class="sxs-lookup"><span data-stu-id="238a7-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="238a7-330">Crie as relações necessárias entre o novo objeto **PackagePart** e o objeto**Package** ou outros objetos **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="238a7-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="238a7-331">Atualize todas as peças existentes que precisam referenciar a nova peça.</span><span class="sxs-lookup"><span data-stu-id="238a7-331">You update any existing parts that need to reference the new part.</span></span> <span data-ttu-id="238a7-332">Por exemplo, se você adicionar uma nova parte do Conteúdo da Página (uma nova página) ao arquivo, também precisará atualizar a parte do Índice de Página (arquivo /visio/pages/pages.xml) para incluir as informações corretas sobre a nova página.</span><span class="sxs-lookup"><span data-stu-id="238a7-332">For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="238a7-333">Use o procedimento a seguir para criar uma nova parte de extensibilidade de faixa de opções no arquivo do Visio.</span><span class="sxs-lookup"><span data-stu-id="238a7-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="238a7-334">A nova Extensibilidade da Faixa de Opções adiciona à faixa de opções uma nova guia com um único grupo que contém um único botão.</span><span class="sxs-lookup"><span data-stu-id="238a7-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="238a7-335">Para criar uma nova parte do pacote</span><span class="sxs-lookup"><span data-stu-id="238a7-335">To create a new package part</span></span>

1. <span data-ttu-id="238a7-336">Após o método `CheckForRecalc` na classe **Programa** classe (ou **Module1** no Visual Basic) do procedimento anterior, adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "http://schemas.microsoft.com/office/2006/01/customui";
        XDocument customUIXDoc = new XDocument(
            new XDeclaration("1.0", "utf-8", "true"),
            new XElement(customUINS + "customUI",
                new XElement(customUINS + "ribbon",
                    new XElement(customUINS + "tabs",
                        new XElement(customUINS + "tab",
                            new XAttribute("id", "customTab"),
                            new XAttribute("label", "CUSTOM"),
                            new XElement(customUINS + "group",
                                new XAttribute("id", "customGroup"),
                                new XAttribute("label", "Custom Group"),
                                new XElement(customUINS + "button",
                                    new XAttribute("id", "customButton"),
                                    new XAttribute("label", "Custom Button"),
                                    new XAttribute("size", "large"),
                                    new XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        );
        return customUIXDoc;
    }
    ```

    ```vb
    Private Function CreateCustomUI() As XDocument
        ' Add a new Custom User Interface document part to the package.
        ' This code adds a new CUSTOM tab to the ribbon for this
        ' document. The tab has one group that contains one button.
        Dim customUINS As XNamespace = _
            "http://schemas.microsoft.com/office/2006/01/customui"
        Dim customUIXML = New XDocument( _
            New XDeclaration("1.0", "utf-8", "true"), _
            New XElement(customUINS + "customUI", _
                New XElement(customUINS + "ribbon",
                    New XElement(customUINS + "tabs",
                        New XElement(customUINS + "tab",
                            New XAttribute("id", "customTab"),
                            New XAttribute("label", "CUSTOM"),
                            New XElement(customUINS + "group",
                                New XAttribute("id", "customGroup"),
                                New XAttribute("label", "Custom Group"),
                                New XElement(customUINS + "button",
                                    New XAttribute("id", "customButton"),
                                    New XAttribute("label", "Custom Button"),
                                    New XAttribute("size", "large"),
                                    New XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        )
        Return customUIXML
    End Function
    ```

2. <span data-ttu-id="238a7-337">Após o método`CreateCustomUI` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método.</span><span class="sxs-lookup"><span data-stu-id="238a7-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void CreateNewPackagePart(Package filePackage, 
        XDocument partXML, Uri packageLocation, string contentType, 
        string relationship)
    {
        // Need to check first to see whether the part exists already.
        if (!filePackage.PartExists(packageLocation))
        {
            // Create a new blank package part at the specified URI 
            // of the specified content type.
            PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
                contentType);
            // Create a stream from the package part and save the 
            // XML document to the package part.
            using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
                FileAccess.ReadWrite))
            {
                partXML.Save(partStream);
            }
        }
        // Add a relationship from the file package to this
        // package part. You can also create relationships
        // between an existing package part and a new part.
        filePackage.CreateRelationship(packageLocation,
            TargetMode.Internal,
            relationship);
    }
    ```

    ```vb
    Private Sub CreateNewPackagePart(filePackage As Package, _
        partXML As XDocument, packageLocation As Uri, contentType As String, _
        relationship As String)
        ' Need to check first to see whether the part exists already.
        If Not (filePackage.PartExists(packageLocation)) Then
            ' Create a new blank package part at the specified URI
            ' of the specified content type.
            Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
                contentType)
            ' Create a stream from the package part and save the
            ' XML document to the package part.
            Using partStream As Stream = newPart.GetStream(FileMode.Create, _
                FileAccess.ReadWrite)
                partXML.Save(partStream)
            End Using
            ' Add a relationship from the file package to this
            ' package part. You can also create relationships
            ' between an existing package part and a new part.
            filePackage.CreateRelationship(packageLocation, _
                TargetMode.Internal, relationship)
        End If
    End Sub
    ```

3. <span data-ttu-id="238a7-338">Substitua todos os códigos dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic) com o seguinte código.</span><span class="sxs-lookup"><span data-stu-id="238a7-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. <span data-ttu-id="238a7-339">Escolha a tecla F5 para a solução de depuração.</span><span class="sxs-lookup"><span data-stu-id="238a7-339">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="238a7-340">Quando o programa estiver concluído, escolha qualquer tecla para sair.</span><span class="sxs-lookup"><span data-stu-id="238a7-340">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="238a7-341">Abra o arquivo do Visio Package.vsdx no Visio 2013 e, em seguida, escolha a guia **CUSTOM**.</span><span class="sxs-lookup"><span data-stu-id="238a7-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="238a7-342">A faixa de opções personalizada se parece com a Figura 2 quando o arquivo é aberto no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="238a7-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="238a7-343">**Figura 2. Guia personalizada na faixa de opções do Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="238a7-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![A custom tab in the ribbon](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="238a7-345">O XML criado pelo método `CreateCustomUI` é semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="238a7-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a><span data-ttu-id="238a7-346">Reconhecimento</span><span class="sxs-lookup"><span data-stu-id="238a7-346">Acknowledgements</span></span>
<span data-ttu-id="238a7-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-347"><a name="vis15_ManipulateFF_Ackn"> </a></span></span>

<span data-ttu-id="238a7-348">Gostaríamos de reconhecer a contribuição e o auxílio do Visio MVP **Al Edlund** na criação dos exemplos de código contidos neste artigo técnico.</span><span class="sxs-lookup"><span data-stu-id="238a7-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="238a7-349">Al é um especialista reconhecido na manipulação do formato de arquivo do Visio, incluindo o formato de desenho de XML do Visio (.vdx) eo novo formato de arquivo do Visio (.vsdx).</span><span class="sxs-lookup"><span data-stu-id="238a7-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="238a7-350">Al criou projetos que exploram os formatos de arquivo do Visio programaticamente e expõem as estruturas internas.</span><span class="sxs-lookup"><span data-stu-id="238a7-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="238a7-351">Para obter mais informações sobre o trabalho do Al com o formato de arquivo do Visio, consulte os links na seção Recursos Adicionais a seguir.</span><span class="sxs-lookup"><span data-stu-id="238a7-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="238a7-352">Confira também</span><span class="sxs-lookup"><span data-stu-id="238a7-352">See also</span></span>
<span data-ttu-id="238a7-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="238a7-353"><a name="vis15_ManipulateFF_Additional"> </a></span></span>

- <span data-ttu-id="238a7-354">Por Al Edlund:</span><span class="sxs-lookup"><span data-stu-id="238a7-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="238a7-355">[pkgVisio - manipulação do projeto Visio 2013 XML](https://pkgvisio.codeplex.com/documentation) no CodePlex.</span><span class="sxs-lookup"><span data-stu-id="238a7-355">[pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="238a7-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) vídeo no YouTube.</span><span class="sxs-lookup"><span data-stu-id="238a7-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="238a7-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) vídeo no YouTube.</span><span class="sxs-lookup"><span data-stu-id="238a7-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="238a7-358">Centro do desenvolvedor do Visio</span><span class="sxs-lookup"><span data-stu-id="238a7-358">Visio Developer Center</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [<span data-ttu-id="238a7-359">Manipular documentos de formatos Open XML do Office</span><span class="sxs-lookup"><span data-stu-id="238a7-359">Manipulate Office Open XML Formats Documents</span></span>](https://msdn.microsoft.com/library/aa982683%28v=office.12%29.aspx)
    
- [<span data-ttu-id="238a7-360">Criar um documento com Namespaces (C#) (LINQ XML)</span><span class="sxs-lookup"><span data-stu-id="238a7-360">Create a Document with Namespaces (C#) (LINQ to XML)</span></span>](https://msdn.microsoft.com/library/bb387075.aspx)
    
- [<span data-ttu-id="238a7-361">Adicionar partes XML personalizadas em documentos sem iniciar o Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="238a7-361">Add Custom XML Parts to Documents Without Starting Microsoft Office</span></span>](https://msdn.microsoft.com/library/bb608597%28VS.90%29.aspx)
    

