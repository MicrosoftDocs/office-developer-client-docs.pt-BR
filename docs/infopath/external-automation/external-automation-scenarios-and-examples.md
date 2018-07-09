---
title: Exemplos e cenários de automação externa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- automatizando o infopath 2007, formulários [InfoPath 2007], adicionando dados programaticamente, automação [InfoPath 2007], cenários externos
localization_priority: Normal
ms.assetid: dfa880e6-de23-41c4-b80b-6935e0c8563d
description: Os membros fornecido pelo Microsoft Office InfoPath principal assembly de interoperabilidade (Microsoft.Office.Interop.InfoPath.dll) e o assembly de interoperabilidade do InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) suportam escrever código gerenciado para automatizar InfoPath.
ms.openlocfilehash: 1c76e5cb659c9d3f39eec4a7e517ab57c98c858a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765499"
---
# <a name="external-automation-scenarios-and-examples"></a><span data-ttu-id="fc296-104">Exemplos e cenários de automação externa</span><span class="sxs-lookup"><span data-stu-id="fc296-104">External automation scenarios and examples</span></span>

<span data-ttu-id="fc296-105">Os membros fornecido pelo Microsoft Office InfoPath principal assembly de interoperabilidade (Microsoft.Office.Interop.InfoPath.dll) e o assembly de interoperabilidade do InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) suportam escrever código gerenciado para automatizar InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fc296-105">The members provided by the Microsoft Office InfoPath primary interop assembly (Microsoft.Office.Interop.InfoPath.dll) and the InfoPath XML interop assembly (Microsoft.Office.Interop.InfoPath.Xml.dll) support writing managed code for automating InfoPath.</span></span> 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a><span data-ttu-id="fc296-106">Estabelecimento de referências a assemblies de interoperabilidade primários do Microsoft Office InfoPath e interoperabilidade de XML do InfoPath</span><span class="sxs-lookup"><span data-stu-id="fc296-106">Establishing references to the Microsoft Office InfoPath Primary Interop and InfoPath XML Interop assemblies</span></span>

<span data-ttu-id="fc296-107">Para escrever código gerenciado para automatizar o InfoPath, você precisa estabelecer referências de interoperabilidade primários do Microsoft InfoPath e os assemblies de interoperabilidade do InfoPath XML.</span><span class="sxs-lookup"><span data-stu-id="fc296-107">To write managed code for automating InfoPath, you must establish references to the Microsoft InfoPath primary interop and the InfoPath XML interop assemblies.</span></span> <span data-ttu-id="fc296-108">O assembly de interoperabilidade primário do Microsoft InfoPath fornece suporte para a interoperabilidade com o modelo de objeto COM expostos pelo IPEDITOR. DLL usando os membros do namespace [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fc296-108">The Microsoft InfoPath primary interop assembly provides support for interoperability with the COM object model exposed by IPEDITOR.DLL by using the members of the [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) namespace.</span></span> <span data-ttu-id="fc296-109">O assembly de interoperabilidade do InfoPath XML fornece suporte para a interoperabilidade com o modelo de objeto COM expostos pelo Microsoft XML Core Services (MSXML) usando os membros do namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/pt-br/library/microsoft.office.interop.infopath.xml) .</span><span class="sxs-lookup"><span data-stu-id="fc296-109">The InfoPath XML interop assembly provides support for interoperability with the COM object model exposed by Microsoft XML Core Services (MSXML) by using the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/pt-br/library/microsoft.office.interop.infopath.xml) namespace.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="fc296-110">Os usuários de aplicativos de código gerenciado que automatizam o InfoPath devem ter o InfoPath, o assembly de interoperabilidade primário do Microsoft Office InfoPath e o assembly de interoperabilidade do InfoPath XML instalada em seus computadores.</span><span class="sxs-lookup"><span data-stu-id="fc296-110">Users of managed-code applications that automate InfoPath must have InfoPath, the Microsoft Office InfoPath primary interop assembly, and the InfoPath XML interop assembly installed on their computers.</span></span> <span data-ttu-id="fc296-111">A opção de **Suporte à programação do .NET** no programa de instalação do InfoPath é definida como **Executar de Meu computador** para uma instalação típica do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fc296-111">The **.NET Programmability Support** option in the InfoPath setup program is set to **Run from My Computer** for a typical installation of InfoPath.</span></span>
>  
> <span data-ttu-id="fc296-112">Como resultado, conforme longos como o .NET Framework 1.1 Software Development Kit (SDK) ou redistribuível do .NET Framework 1.1 ou posterior é instalado, esses assemblies de interoperabilidade também serão instalados por padrão.</span><span class="sxs-lookup"><span data-stu-id="fc296-112">As a result, as long as the .NET Framework 1.1 Redistributable or .NET Framework 1.1 Software Development Kit (SDK) or later is installed, these interop assemblies will also be installed by default.</span></span> <span data-ttu-id="fc296-113">Se esses assemblies de interoperabilidade não estão disponíveis em um computador do usuário, você deve confirmar que o .NET Framework 1.1 ou posterior é instalado e, em seguida, executar **programas e recursos** no **Painel de controle** para alterar a instalação e definir o **programação do .NET Suporte** opção do InfoPath para **Executar de Meu computador**.</span><span class="sxs-lookup"><span data-stu-id="fc296-113">If these interop assemblies are not available on a user's computer, you must confirm that the .NET Framework 1.1 or later is installed, and then run **Programs and Features** from the **Control Panel** to change setup and set the **.NET Programmability Support** option of InfoPath to **Run from My Computer**.</span></span> 
  
<span data-ttu-id="fc296-114">Os procedimentos a seguir descrevem como definir os assemblies de interoperabilidade de referências de interoperabilidade primários do Microsoft Office InfoPath e InfoPath XML em um projeto do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fc296-114">The following procedures describe how to set references to the Microsoft Office InfoPath primary interop and the InfoPath XML interop assemblies in a Visual Studio project.</span></span>
  
<span data-ttu-id="fc296-115">Para definir uma referência para o assembly de interoperabilidade primário do Microsoft.Office.Interop.InfoPath, defina uma referência à **Biblioteca de tipos do Microsoft InfoPath 3.0** na guia **COM** da caixa de diálogo **Adicionar referência** .</span><span class="sxs-lookup"><span data-stu-id="fc296-115">To set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly, set a reference to **Microsoft InfoPath 3.0 Type Library** on the **COM** tab of the **Add Reference** dialog box.</span></span> <span data-ttu-id="fc296-116">Mesmo que você definir uma referência a partir da guia **COM** , uma referência é estabelecida para o assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath.dll instalado no Cache de Assembly Global (GAC), o programa de instalação do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fc296-116">Even though you set a reference from the **COM** tab, a reference is established to the Microsoft.Office.Interop.InfoPath.dll primary interop assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span> 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a><span data-ttu-id="fc296-117">Definir uma referência para o assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath</span><span class="sxs-lookup"><span data-stu-id="fc296-117">Set a reference to the Microsoft.Office.Interop.InfoPath primary interop assembly</span></span>

1. <span data-ttu-id="fc296-118">Abra um projeto de código gerenciado do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fc296-118">Open a Visual Studio managed code project.</span></span>
    
2. <span data-ttu-id="fc296-119">No **Solution Explorer**, clique com o botão **referências**e, em seguida, clique em **Adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="fc296-119">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="fc296-120">Na guia **COM** , clique duas vezes em **Biblioteca de tipos do Microsoft InfoPath 3.0**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="fc296-120">On the **COM** tab, double-click **Microsoft InfoPath 3.0 Type Library**, and then click **OK**.</span></span>
    
<span data-ttu-id="fc296-121">Para definir uma referência para o assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.Xml, navegue até o arquivo de Microsoft.Office.Interop.InfoPath.Xml.dll que é instalado por padrão no < _unidade_>: \Program Files\Microsoft Office\OFFICE14 pasta .</span><span class="sxs-lookup"><span data-stu-id="fc296-121">To set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly, browse to the Microsoft.Office.Interop.InfoPath.Xml.dll file that is installed by default in the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder.</span></span> <span data-ttu-id="fc296-122">Mesmo que você especifique a cópia do assembly no sistema de arquivos local, esse procedimento estabelece uma referência para o assembly Microsoft.Office.Interop.InfoPath.Xml.dll instalado no Cache de Assembly Global (GAC), o programa de instalação do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="fc296-122">Even though you specify the copy of the assembly in the local file system, this procedure establishes a reference to the Microsoft.Office.Interop.InfoPath.Xml.dll assembly that is installed in the Global Assembly Cache (GAC) by the InfoPath setup program.</span></span>
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a><span data-ttu-id="fc296-123">Definir uma referência para o assembly de interoperabilidade de Microsoft.Office.Interop.InfoPath.Xml</span><span class="sxs-lookup"><span data-stu-id="fc296-123">Set a reference to the Microsoft.Office.Interop.InfoPath.Xml interop assembly</span></span>

1. <span data-ttu-id="fc296-124">Abra ou crie um projeto de código gerenciado do Visual Studio, como um **Aplicativo de Console** ou de um **Aplicativo do Windows**.</span><span class="sxs-lookup"><span data-stu-id="fc296-124">Open or create a Visual Studio managed code project, such as a **Console Application** or **Windows Application**.</span></span>
    
2. <span data-ttu-id="fc296-125">No **Solution Explorer**, clique com o botão **referências**e, em seguida, clique em **Adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="fc296-125">In **Solution Explorer**, right-click **References**, and then click **Add Reference**.</span></span>
    
3. <span data-ttu-id="fc296-126">Na guia **.NET** , clique em **Procurar**, navegue até a < _unidade_>: \Program Files\Microsoft Office\OFFICE14 pasta e clique em Microsoft.Office.Interop.InfoPath.Xml.dll.</span><span class="sxs-lookup"><span data-stu-id="fc296-126">On the **.NET** tab, click **Browse**, navigate to the < _drive_>:\Program Files\Microsoft Office\OFFICE14 folder, and then click Microsoft.Office.Interop.InfoPath.Xml.dll.</span></span>
    
4. <span data-ttu-id="fc296-127">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc296-127">Click **OK**.</span></span>
    
## <a name="automate-changing-the-value-of-a-field"></a><span data-ttu-id="fc296-128">Automatizar a alteração do valor de um campo</span><span class="sxs-lookup"><span data-stu-id="fc296-128">Automate changing the value of a field</span></span>

<span data-ttu-id="fc296-129">Vamos supor que um dos clientes do usuário de um modelo de formulário do InfoPath relatório Vendas alterados recentemente seu nome de "Empresa A" para "Empresa B."</span><span class="sxs-lookup"><span data-stu-id="fc296-129">Suppose one of the customers of the user of an InfoPath sales report form template recently changed its name from "Company A" to "Company B."</span></span> <span data-ttu-id="fc296-130">Um desenvolvedor é solicitado a escrever o código que será atualizada automaticamente os formulários de relatório de vendas salvos deste modelo de formulário para refletir a alteração do nome.</span><span class="sxs-lookup"><span data-stu-id="fc296-130">A developer is asked to write code that will automatically update the sales report forms saved from this form template to reflect the name change.</span></span> <span data-ttu-id="fc296-131">O cenário a seguir supõe que um formulário que contenha uma caixa de texto que está acoplada a um campo denominado NomeDoCliente.</span><span class="sxs-lookup"><span data-stu-id="fc296-131">The following scenario assumes a form that contains a text box that is bound to a field named customerName.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="fc296-132">Criar o modelo de formulário de amostra e formulário</span><span class="sxs-lookup"><span data-stu-id="fc296-132">Create the sample form template and form</span></span>

1. <span data-ttu-id="fc296-133">Abra o InfoPath e crie um modelo de formulário em branco.</span><span class="sxs-lookup"><span data-stu-id="fc296-133">Open InfoPath and create a blank form template.</span></span>
    
2. <span data-ttu-id="fc296-134">Adicionar um controle de **Caixa de texto** ao formulário e nomeie o campo acoplado NomeDoCliente o controle.</span><span class="sxs-lookup"><span data-stu-id="fc296-134">Add a **Text Box** control to the form, and name the field bound to the control customerName.</span></span>
    
3. <span data-ttu-id="fc296-135">No painel de tarefas **campos** , clique com botão direito na pasta **myFields** e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="fc296-135">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="fc296-136">Na guia **detalhes** , selecione e copie o seguinte valor **Namespace:** e, em seguida, cole-o no bloco de notas ou em algum outro local onde você possa recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="fc296-136">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="fc296-137">Você precisará esse valor de posteriormente para definir o valor da propriedade **SelectionNamespaces** em seu código.</span><span class="sxs-lookup"><span data-stu-id="fc296-137">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="fc296-138">Publique o modelo de formulário para uma pasta denominada C:\Test e aceite o nome padrão, modelo1.</span><span class="sxs-lookup"><span data-stu-id="fc296-138">Publish the form template to a folder named C:\Test and accept the default name, Template1.</span></span> 
    
6. <span data-ttu-id="fc296-139">Abra o modelo de formulário, adicione o nome "Empresa uma" à caixa de texto vinculada ao campo NomeDoCliente e salve o formulário como "Formulário1".</span><span class="sxs-lookup"><span data-stu-id="fc296-139">Open the form template, add the name "Company A" to text box bound to the customerName field, and then save the form as "Form1".</span></span> 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a><span data-ttu-id="fc296-140">Criar um aplicativo de console do código gerenciado para alterar o nome de 'Uma empresa' 'Empresa b'</span><span class="sxs-lookup"><span data-stu-id="fc296-140">Create a managed code console application to change the name from 'Company A' to 'Company B'</span></span>

1. <span data-ttu-id="fc296-141">Abra o Visual Studio e crie um novo Visual c# ou aplicativo de Console do Visual Basic chamado UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="fc296-141">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named UpdateCustomer.</span></span>
    
2. <span data-ttu-id="fc296-142">Estabelece referências à interoperabilidade primários do Microsoft Office InfoPath e assemblies de interoperabilidade do InfoPath XML, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="fc296-142">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="fc296-143">Adicione o código a seguir ao arquivo Module. vb ou Module1, certificando-se atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando você criou o formulário de exemplo.</span><span class="sxs-lookup"><span data-stu-id="fc296-143">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="fc296-144">No menu **Debug** para compilar e executar o aplicativo de console, clique em **Iniciar depuração** .</span><span class="sxs-lookup"><span data-stu-id="fc296-144">Click **Start Debugging** on the **Debug** menu to compile and run the console application.</span></span> 
    
   <span data-ttu-id="fc296-145">O aplicativo abre o formulário salvo como Form1.xml e faz um loop em todos os elementos de NomeDoCliente que contêm o valor empresa A e altera o valor para a empresa B. Quando a operação for concluída, uma nova cópia do formulário é salvo como Form2.xml na pasta C:\Test.</span><span class="sxs-lookup"><span data-stu-id="fc296-145">The application opens the form saved as Form1.xml and loops through all customerName elements that contain the value Company A and changes that value to Company B. When the operation is complete, a new copy of the form is saved as Form2.xml in the C:\Test folder.</span></span> 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a><span data-ttu-id="fc296-146">Automatizar a abertura de um formulário e ao preencher os valores de campo</span><span class="sxs-lookup"><span data-stu-id="fc296-146">Automate opening a form and populating field values</span></span>

<span data-ttu-id="fc296-147">O exemplo a seguir automatiza abrir um formulário em branco e preencher o primeiro nome, sobrenome e campos de endereço no formulário.</span><span class="sxs-lookup"><span data-stu-id="fc296-147">The following example automates opening a blank form and populating the first name, last name, and address fields in the form.</span></span> <span data-ttu-id="fc296-148">Este cenário pressupõe um formulário que contém três caixas de texto que são vinculadas a campos denominados FirstName, LastName e endereço.</span><span class="sxs-lookup"><span data-stu-id="fc296-148">This scenario assumes a form that contains three text boxes that are bound to fields named FirstName, LastName, and Address.</span></span>
  
### <a name="create-the-sample-form-template-and-form"></a><span data-ttu-id="fc296-149">Criar o modelo de formulário de amostra e formulário</span><span class="sxs-lookup"><span data-stu-id="fc296-149">Create the sample form template and form</span></span>

1. <span data-ttu-id="fc296-150">Abra o InfoPath e crie um formulário em branco.</span><span class="sxs-lookup"><span data-stu-id="fc296-150">Open InfoPath and create a blank form.</span></span>
    
2. <span data-ttu-id="fc296-151">Adicione três controles de caixa de texto ao formulário e nomeie campos acoplados a controles: FirstName, LastName e endereço.</span><span class="sxs-lookup"><span data-stu-id="fc296-151">Add three text box controls to the form, and name the fields bound to the controls: FirstName, LastName, and Address.</span></span> <span data-ttu-id="fc296-152">Adicione outros campos que você deseja.</span><span class="sxs-lookup"><span data-stu-id="fc296-152">Add any other fields you want.</span></span>
    
3. <span data-ttu-id="fc296-153">No painel de tarefas **campos** , clique com botão direito na pasta **myFields** e, em seguida, clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="fc296-153">In the **Fields** task pane, right-click the **myFields** folder, and then click **Properties**.</span></span>
    
4. <span data-ttu-id="fc296-154">Na guia **detalhes** , selecione e copie o seguinte valor **Namespace:** e, em seguida, cole-o no bloco de notas ou em algum outro local onde você possa recuperá-lo.</span><span class="sxs-lookup"><span data-stu-id="fc296-154">On the **Details** tab, select and copy the value following **Namespace:**, and then paste this into Notepad or some other location where you can retrieve it.</span></span> <span data-ttu-id="fc296-155">Você precisará esse valor de posteriormente para definir o valor da propriedade **SelectionNamespaces** em seu código.</span><span class="sxs-lookup"><span data-stu-id="fc296-155">You will need this value later for setting the value of the **SelectionNamespaces** property in your code.</span></span> 
    
5. <span data-ttu-id="fc296-156">Publique o modelo de formulário para uma pasta denominada c:\Temp. e aceite o nome padrão, modelo1.</span><span class="sxs-lookup"><span data-stu-id="fc296-156">Publish the form template to a folder named C:\Temp and accept the default name, Template1.</span></span>
    
6. <span data-ttu-id="fc296-157">Abra o modelo de formulário e salvar um formulário em branco como "Formulário1" como c:\Temp..</span><span class="sxs-lookup"><span data-stu-id="fc296-157">Open the form template and save a blank form as "Form1" to C:\Temp.</span></span>
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a><span data-ttu-id="fc296-158">Criar um aplicativo de console do código gerenciado para abrir o formulário e preencha os campos</span><span class="sxs-lookup"><span data-stu-id="fc296-158">Create a managed code console application to open the form and populate the fields</span></span>

1. <span data-ttu-id="fc296-159">Abra o Visual Studio e crie um novo Visual c# ou aplicativo de Console do Visual Basic chamado OpenForm.</span><span class="sxs-lookup"><span data-stu-id="fc296-159">Open Visual Studio and create a new Visual C# or Visual Basic Console Application named OpenForm.</span></span>
    
2. <span data-ttu-id="fc296-160">Estabelece referências à interoperabilidade primários do Microsoft Office InfoPath e assemblies de interoperabilidade do InfoPath XML, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="fc296-160">Establish references to the Microsoft Office InfoPath primary interop and InfoPath XML interop assemblies as described above.</span></span>
    
3. <span data-ttu-id="fc296-161">Adicione o código a seguir ao arquivo Module. vb ou Module1, certificando-se atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando você criou o formulário de exemplo.</span><span class="sxs-lookup"><span data-stu-id="fc296-161">Add the following code to the Program.cs or Module1.vb file, making sure to update the value of the namespace in the setting for the **SelectionNamespaces** property with the value you copied when you created the sample form.</span></span> 
    
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

4. <span data-ttu-id="fc296-162">No menu **Depurar** , clique em **Iniciar depuração** para compilar e executar o aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="fc296-162">On the **Debug** menu, click **Start Debugging** to compile and run the console application.</span></span> 
    
   <span data-ttu-id="fc296-163">O aplicativo abre o formulário salvo como Form1.xml e preencha os campos FirstName, LastName e endereço com os valores especificados no código e, então, salve o formulário, deixando o InfoPath aberta.</span><span class="sxs-lookup"><span data-stu-id="fc296-163">The application will open the form saved as Form1.xml and fill in the FirstName, LastName, and Address fields with the values specified in the code, and then save the form, leaving InfoPath open.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fc296-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc296-164">See also</span></span>

- [<span data-ttu-id="fc296-165">Sobre o Assembly de interoperabilidade primário do InfoPath do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="fc296-165">About the Microsoft Office InfoPath Primary Interop Assembly</span></span>](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [<span data-ttu-id="fc296-166">Sobre o Assembly de interoperabilidade de XML do InfoPath</span><span class="sxs-lookup"><span data-stu-id="fc296-166">About the InfoPath XML Interop Assembly</span></span>](about-the-infopath-xml-interop-assembly.md)

