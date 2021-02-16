---
title: Cenários e exemplos de automação externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automação do infopath 2007,formulários [InfoPath 2007],adição de dados via programação,automação [InfoPath 2007], cenários externos
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Os membros fornecidos pelo assembly de interoperabilidade primário do Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) e pelo assembly de interoperabilidade XML do InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permitem escrever código gerenciado para automatizar o InfoPath.
ms.openlocfilehash: 79fbc56033ffce639b5007874dabf56e8e286edb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537812"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="3b859-104">Cenários e exemplos de automação externa</span><span class="sxs-lookup"><span data-stu-id="3b859-104">External automation scenarios and examples</span></span>

<span data-ttu-id="3b859-105">Os membros fornecidos pelo assembly de interoperabilidade primário do Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) e pelo assembly de interoperabilidade XML do InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permitem escrever código gerenciado para automatizar o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3b859-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="3b859-106">Estabelecer referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath</span><span class="sxs-lookup"><span data-stu-id="3b859-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="3b859-107">Para escrever um código gerenciado que automatize o InfoPath, você deve estabelecer referências ao assembly de interoperabilidade primário do Microsoft InfoPath e ao assembly de interoperabilidade XML do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3b859-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="3b859-108">O assembly de interoperabilidade primário do Microsoft InfoPath fornece suporte para interoperabilidade com o modelo de objeto COM exposto por IPEDITOR.DLL, usando os membros do namespace [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b859-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="3b859-109">O assembly de interoperabilidade XML do InfoPath fornece suporte para interoperabilidade com o modelo de objeto COM exposto pelo Microsoft XML Core Services (MSXML) usando os membros do namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml).</span><span class="sxs-lookup"><span data-stu-id="3b859-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3b859-110">Os usuários de aplicativos de código gerenciado que automatizam o InfoPath devem ter o InfoPath, o assembly de interoperabilidade primário do Microsoft Office InfoPath e o assembly de interoperabilidade XML do InfoPath instalados em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="3b859-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="3b859-111">A opção **Suporte à Programação .NET** no programa de instalação do InfoPath está definida como **Executar do Meu Computador** para uma instalação típica do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3b859-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="3b859-112">Como resultado, desde que o Redistribuível do .NET Framework 1.1 ou o .NET Framework 1.1 Software Development Kit (SDK) ou posterior esteja instalado, esses módulos de interoperabilidade também serão instalados por padrão.</span><span class="sxs-lookup"><span data-stu-id="3b859-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="3b859-113">Se esses módulos de interoperabilidade não estiverem disponíveis no computador de um usuário, você deve confirmar se o .NET Framework 1.1 ou posterior está instalado e executar **Programas e Recursos** no **Painel de Controle** para alterar a configuração e definir a opção **Suporte à Programação .NET** do InfoPath para **Executar do Meu Computador**.</span><span class="sxs-lookup"><span data-stu-id="3b859-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="3b859-114">Os procedimentos a seguir descrevem como definir referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath em um projeto do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3b859-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="3b859-115">Para definir uma referência ao assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath, defina uma referência à **Biblioteca de Tipos do Microsoft InfoPath 3.0** na guia **COM** da caixa de diálogo **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="3b859-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="3b859-116">Mesmo que você defina uma referência na guia **COM**, é estabelecida uma referência com o assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath.dll instalado no GAC (Cache de Assembly Global) pelo programa de instalação do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3b859-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="3b859-117">Definir uma referência ao assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="3b859-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="3b859-118">Abra um projeto de código gerenciado do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3b859-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="3b859-119">No **Gerenciador de Soluções**, clique com o botão direito do mouse em **Referências** e clique em **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="3b859-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="3b859-120">Na guia **COM**, clique duas vezes em **Biblioteca de Tipos do Microsoft InfoPath 3.0** e depois clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b859-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="3b859-121">Para definir uma referência ao assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.Xml, navegue até o arquivo Microsoft.Office.Interop.InfoPath.Xml.dll instalado por padrão na pasta <_unidade_>:\Arquivos de Programa\Microsoft Office\OFFICE14.</span><span class="sxs-lookup"><span data-stu-id="3b859-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="3b859-122">Mesmo que você especifique a cópia do assembly no sistema de arquivos local, esse procedimento estabelece uma referência ao assembly Microsoft.Office.Interop.InfoPath.Xml.dll instalado no GAC (Cache de Assembly Global) pelo programa de instalação do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3b859-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="3b859-123">Definir uma referência ao assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.Xml</span><span class="sxs-lookup"><span data-stu-id="3b859-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="3b859-124">Abra ou crie um projeto de código gerenciado do Visual Studio, como um **Aplicativo de Console** ou um **Aplicativo do Windows**.</span><span class="sxs-lookup"><span data-stu-id="3b859-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="3b859-125">No **Gerenciador de Soluções**, clique com o botão direito do mouse em **Referências** e clique em **Adicionar Referência**.</span><span class="sxs-lookup"><span data-stu-id="3b859-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="3b859-126">Na guia **.NET**, clique em **Procurar**, navegue até a pasta <_unidade_>:\Arquivos de Programa\Microsoft Office\OFFICE14 e clique em Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="3b859-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="3b859-127">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b859-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="3b859-128">Automatizar a alteração do valor de um campo</span><span class="sxs-lookup"><span data-stu-id="3b859-128">Automate changing the value of a field</span></span>

<span data-ttu-id="3b859-129">Suponha que um dos clientes do usuário de um modelo de formulário de relatório de vendas do InfoPath tenha alterado recentemente seu nome de "Empresa A" para "Empresa B".</span><span class="sxs-lookup"><span data-stu-id="3b859-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="3b859-130">Um desenvolvedor é solicitado a escrever um código que atualize automaticamente os formulários de relatórios de vendas salvos desse modelo de formulário para refletir a alteração no nome.</span><span class="sxs-lookup"><span data-stu-id="3b859-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="3b859-131">O cenário a seguir pressupõe um formulário que contém uma caixa de texto associada a um campo denominado customerName.</span><span class="sxs-lookup"><span data-stu-id="3b859-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="3b859-132">Criar um exemplo de modelo de formulário e de formulário</span><span class="sxs-lookup"><span data-stu-id="3b859-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="3b859-133">Abra o InfoPath e crie um modelo de formulário em branco.</span><span class="sxs-lookup"><span data-stu-id="3b859-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="3b859-134">Adicione um controle **Caixa de Texto** ao formulário e nomeie o campo associado a esse controle como customerName.</span><span class="sxs-lookup"><span data-stu-id="3b859-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="3b859-135">No painel de tarefas **Campos**, clique com o botão direito do mouse na pasta **meusCampos** e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="3b859-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="3b859-136">Na guia **Detalhes**, selecione e copie o valor após **Namespace:** e cole-o no Bloco de Notas ou em outro local em que você possa recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="3b859-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="3b859-137">Você precisará desse valor mais tarde para definir o valor da propriedade **SelectionNamespaces** no seu código.</span><span class="sxs-lookup"><span data-stu-id="3b859-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="3b859-138">Publique o modelo de formulário em uma pasta nomeada C:\Test e aceite o nome padrão, Template1.</span><span class="sxs-lookup"><span data-stu-id="3b859-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="3b859-139">Abra o modelo de formulário, adicione o nome "Empresa A" à caixa de texto associada ao campo customerName e depois salve o formulário como "Form1".</span><span class="sxs-lookup"><span data-stu-id="3b859-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="3b859-140">Criar um aplicativo de console de código gerenciado para alterar o nome de "Empresa A" para "Empresa B"</span><span class="sxs-lookup"><span data-stu-id="3b859-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="3b859-141">Abra o Visual Studio e crie um novo Aplicativo de Console do Visual C # ou Visual Basic com o nome UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="3b859-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="3b859-142">Estabeleça referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="3b859-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="3b859-143">Adicione o seguinte código ao arquivo Program.cs ou Module1.vb, certificando-se de atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando criou o formulário de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3b859-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace UpdateCustomer
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp = 
                new Microsoft.Office.Interop.InfoPath.Application();
            // Get a reference the XDocuments collection 
            // and open the sample form.
            XDocumentsCollection myXDocs = myApp.XDocuments;
            XDocument myXDoc = myXDocs.Open("C:\\Test\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Access the XML DOM for the underlying XML document using
            // the DOM property. Note that you must cast to the 
            // IXMLDOMDocument2 type from the
            // Microsoft.Office.Interop.InfoPath.Xml namespace
            // to access the XML DOM.
            IXMLDOMDocument2 myXMLDoc = myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace 
            // value below with that of your sample form.
            myXMLDoc.setProperty("SelectionNamespaces",
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Select all instances of customerName that contain 
            //'Company A'.
            IXMLDOMNodeList myNames = 
                myXMLDoc.selectNodes(
                "//my:customerName[. = 'Company A']");
            // Check to determine if any nodes were returned.
            if (myNames.length < 1)
            Console.WriteLine(
                "No elements containing 'Company A' were found.");
            // Loop through the list updating to 'Company B'.
            IXMLDOMNode myName = myNames.nextNode();
            while (myName != null)
            {
                myName.text = "Company B";
                myName = myNames.nextNode();
            }
            // Save the updated form as Form2.xml and close out.
            myXDoc.SaveAs("C:\\Test\\Form2.xml");
            myXDocs.Close(0);
            myApp.Quit(false);
            Console.WriteLine("Finished!");
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application()
          ' Get a reference the XDocuments collection 
          ' and open the sample form.
          Dim myXDocs As XDocumentsCollection = myApp.XDocuments
          Dim myXDoc As XDocument = myXDocs.Open( _
            "C:\\Test\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Access the XML DOM for the underlying XML document using
          ' the DOM property. Note that you must cast to the 
          ' IXMLDOMDocument2 type from the
          ' Microsoft.Office.Interop.InfoPath.Xml namespace
          ' to access the XML DOM.
          Dim myXMLDoc As IXMLDOMDocument2 = _
            DirectCast(myXDoc.DOM, IXMLDOMDocument2)
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace 
          ' value below with that of your sample form.
          myXMLDoc.setProperty("SelectionNamespaces", _
    "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Select all instances of customerName that contain 
          ''Company A'.
          Dim myNames As IXMLDOMNodeList = _
      myXMLDoc.selectNodes("//my:customerName[. = 'Company A']")
          ' Check to determine if any nodes were returned.
          If (myNames.length < 1) Then
            Console.WriteLine( _
                "No elements containing 'Company A' were found.")
          Else
            ' Loop through the list updating to 'Company B'.
            Dim myName As IXMLDOMNode = myNames.nextNode()
            While (myName IsNot Nothing)
                myName.text = "Company B"
                myName = myNames.nextNode()
            End While
          End If
          ' Save the updated form as Form2.xml and close out.
          myXDoc.SaveAs("C:\\Test\\Form2.xml")
          myXDocs.Close(0)
          myApp.Quit(False)
          Console.WriteLine("Finished!")
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="3b859-144">Clique em **Iniciar Depuração** no menu **Depurar** para compilar e executar o aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="3b859-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="3b859-145">O aplicativo abre o formulário salvo como Form1.xml e circula por todos os elementos customerName que contêm o valor Empresa A, alterando esse valor para Empresa B. Quando a operação é concluída, uma nova cópia do formulário é salva como Form2.xml na pasta C:\Test.</span><span class="sxs-lookup"><span data-stu-id="3b859-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="3b859-146">Automatizar a abertura de um formulário e o preenchimento de valores de campos</span><span class="sxs-lookup"><span data-stu-id="3b859-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="3b859-147">O exemplo a seguir automatiza a abertura de um formulário em branco e o preenchimento dos campos de nome, sobrenome e endereço no formulário.</span><span class="sxs-lookup"><span data-stu-id="3b859-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="3b859-148">Esse cenário pressupõe um formulário que contém três caixas de texto associadas aos campos FirstName, LastName e Address.</span><span class="sxs-lookup"><span data-stu-id="3b859-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="3b859-149">Criar um exemplo de modelo de formulário e de formulário</span><span class="sxs-lookup"><span data-stu-id="3b859-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="3b859-150">Abra o InfoPath e crie um formulário em branco.</span><span class="sxs-lookup"><span data-stu-id="3b859-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="3b859-151">Adicione três controles de caixa de texto ao formulário e forneça os seguintes nomes aos campos associados a esses controles: FirstName, LastName e Address.</span><span class="sxs-lookup"><span data-stu-id="3b859-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="3b859-152">Adicione outros campos, se desejar.</span><span class="sxs-lookup"><span data-stu-id="3b859-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="3b859-153">No painel de tarefas **Campos**, clique com o botão direito do mouse na pasta **meusCampos** e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="3b859-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="3b859-154">Na guia **Detalhes**, selecione e copie o valor após **Namespace:** e cole-o no Bloco de Notas ou em outro local em que você possa recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="3b859-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="3b859-155">Você precisará desse valor mais tarde para definir o valor da propriedade **SelectionNamespaces** no seu código.</span><span class="sxs-lookup"><span data-stu-id="3b859-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="3b859-156">Publique o modelo de formulário em uma pasta chamada C:\Temp e aceite o nome padrão, Template1.</span><span class="sxs-lookup"><span data-stu-id="3b859-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="3b859-157">Abra o modelo de formulário e salve um formulário em branco como "Form1" em C:\Temp.</span><span class="sxs-lookup"><span data-stu-id="3b859-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="3b859-158">Criar um aplicativo de console de código gerenciado para abrir o formulário e preencher os campos</span><span class="sxs-lookup"><span data-stu-id="3b859-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="3b859-159">Abra o Visual Studio e crie um novo Aplicativo de Console do Visual C # ou Visual Basic com o nome OpenForm.</span><span class="sxs-lookup"><span data-stu-id="3b859-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="3b859-160">Estabeleça referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="3b859-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="3b859-161">Adicione o seguinte código ao arquivo Program.cs ou Module1.vb, certificando-se de atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando criou o formulário de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3b859-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Text;
    using Microsoft.Office.Interop.InfoPath;
    using Microsoft.Office.Interop.InfoPath.Xml;
    namespace OpenForm
    {
      class Program
      {
          static void Main(string[] args)
          {
            // Create an InfoPath Application object.
            Application myApp=
                new Microsoft.Office.Interop.InfoPath.Application();
            // Create an InfoPath XDocument variable and open 
            // the blank form.
            XDocument myXDoc = myApp.XDocuments.Open(
                "c:\\temp\\Form1.xml",
                (int) XdDocumentVersionMode.xdFailOnVersionOlder);
            
            // Create an IXMLDOMDocument2 variable and access 
            // the XML DOM from the underlying XML document
            // using the DOM property of the XDocument object. 
            // Note that you must cast to IXMLDOMDocument2 to do so.
            IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
            // Set the MSXML SelectionNamespaces property to the my
            // namespace of the form. IMPORTANT:Replace the namespace
            // value below with that of your sample form.
            doc.setProperty("SelectionNamespaces","xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'");
            // Pre-populate the fields with specified values.
            doc.selectSingleNode("//my:FirstName").text="My Name";
            doc.selectSingleNode("//my:LastName").text="My LastName";
            doc.selectSingleNode("//my:Address").text="My Address";
            // Save the form, leaving InfoPath open.
            myXDoc.Save();
            
          }
      }
    }
   ```

   ```vb
    Imports Microsoft.Office.Interop.InfoPath
    Imports Microsoft.Office.Interop.InfoPath.Xml
    Module Module1
      Sub Main()
          ' Create an InfoPath Application object.
          Dim myApp As Application = _
            New Microsoft.Office.Interop.InfoPath.Application
          ' Create an InfoPath XDocument variable and open 
          ' the blank form.
          Dim myXDoc As XDocument = myApp.XDocuments.Open( _
            "c:\\temp\\Form1.xml", _
            XdDocumentVersionMode.xdFailOnVersionOlder)
          ' Create an IXMLDOMDocument2 variable and access 
          ' the XML DOM from the underlying XML document
          ' using the DOM property of the XDocument object.
          Dim doc As IXMLDOMDocument2 = myXDoc.DOM
          ' Set the MSXML SelectionNamespaces property to the my
          ' namespace of the form. IMPORTANT:Replace the namespace
          ' value below with that of your sample form.
          doc.setProperty("SelectionNamespaces", "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2006-09-06T23:17:34'")
          ' Pre-populate the fields with specified values.
          doc.selectSingleNode("//my:FirstName").text = "My Name"
          doc.selectSingleNode("//my:LastName").text = "My LastName"
          doc.selectSingleNode("//my:Address").text = "My Address"
          ' Save the form, leaving InfoPath open.
          myXDoc.Save()
      End Sub
    End Module
    
   ```

4. <span data-ttu-id="3b859-162">No menu **Depurar**, clique em **Iniciar Depuração** para compilar e executar o aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="3b859-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="3b859-163">O aplicativo abrirá o formulário salvo como Form1.xml e preencherá os campos FirstName, LastName e Address com os valores especificados no código. Em seguida, ele salvará o formulário, deixando o InfoPath aberto.</span><span class="sxs-lookup"><span data-stu-id="3b859-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3b859-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b859-164">See also</span></span>

- [<span data-ttu-id="3b859-165">Sobre o assembly de interoperabilidade primário do Microsoft Office InfoPath</span><span class="sxs-lookup"><span data-stu-id="3b859-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="3b859-166">Sobre o assembly de interoperabilidade XML do InfoPath</span><span class="sxs-lookup"><span data-stu-id="3b859-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

