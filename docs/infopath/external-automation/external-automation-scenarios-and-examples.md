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
# <a name="external-automation-scenarios-and-examples"></a>Exemplos e cenários de automação externa

Os membros fornecido pelo Microsoft Office InfoPath principal assembly de interoperabilidade (Microsoft.Office.Interop.InfoPath.dll) e o assembly de interoperabilidade do InfoPath XML (Microsoft.Office.Interop.InfoPath.Xml.dll) suportam escrever código gerenciado para automatizar InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Estabelecimento de referências a assemblies de interoperabilidade primários do Microsoft Office InfoPath e interoperabilidade de XML do InfoPath

Para escrever código gerenciado para automatizar o InfoPath, você precisa estabelecer referências de interoperabilidade primários do Microsoft InfoPath e os assemblies de interoperabilidade do InfoPath XML. O assembly de interoperabilidade primário do Microsoft InfoPath fornece suporte para a interoperabilidade com o modelo de objeto COM expostos pelo IPEDITOR. DLL usando os membros do namespace [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) . O assembly de interoperabilidade do InfoPath XML fornece suporte para a interoperabilidade com o modelo de objeto COM expostos pelo Microsoft XML Core Services (MSXML) usando os membros do namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) . 
  
> [!IMPORTANT]
> Os usuários de aplicativos de código gerenciado que automatizam o InfoPath devem ter o InfoPath, o assembly de interoperabilidade primário do Microsoft Office InfoPath e o assembly de interoperabilidade do InfoPath XML instalada em seus computadores. A opção de **Suporte à programação do .NET** no programa de instalação do InfoPath é definida como **Executar de Meu computador** para uma instalação típica do InfoPath.
>  
> Como resultado, conforme longos como o .NET Framework 1.1 Software Development Kit (SDK) ou redistribuível do .NET Framework 1.1 ou posterior é instalado, esses assemblies de interoperabilidade também serão instalados por padrão. Se esses assemblies de interoperabilidade não estão disponíveis em um computador do usuário, você deve confirmar que o .NET Framework 1.1 ou posterior é instalado e, em seguida, executar **programas e recursos** no **Painel de controle** para alterar a instalação e definir o **programação do .NET Suporte** opção do InfoPath para **Executar de Meu computador**. 
  
Os procedimentos a seguir descrevem como definir os assemblies de interoperabilidade de referências de interoperabilidade primários do Microsoft Office InfoPath e InfoPath XML em um projeto do Visual Studio.
  
Para definir uma referência para o assembly de interoperabilidade primário do Microsoft.Office.Interop.InfoPath, defina uma referência à **Biblioteca de tipos do Microsoft InfoPath 3.0** na guia **COM** da caixa de diálogo **Adicionar referência** . Mesmo que você definir uma referência a partir da guia **COM** , uma referência é estabelecida para o assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath.dll instalado no Cache de Assembly Global (GAC), o programa de instalação do InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Definir uma referência para o assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath

1. Abra um projeto de código gerenciado do Visual Studio.
    
2. No **Solution Explorer**, clique com o botão **referências**e, em seguida, clique em **Adicionar referência**.
    
3. Na guia **COM** , clique duas vezes em **Biblioteca de tipos do Microsoft InfoPath 3.0**e, em seguida, clique em **Okey**.
    
Para definir uma referência para o assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.Xml, navegue até o arquivo de Microsoft.Office.Interop.InfoPath.Xml.dll que é instalado por padrão no < _unidade_>: \Program Files\Microsoft Office\OFFICE14 pasta . Mesmo que você especifique a cópia do assembly no sistema de arquivos local, esse procedimento estabelece uma referência para o assembly Microsoft.Office.Interop.InfoPath.Xml.dll instalado no Cache de Assembly Global (GAC), o programa de instalação do InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Definir uma referência para o assembly de interoperabilidade de Microsoft.Office.Interop.InfoPath.Xml

1. Abra ou crie um projeto de código gerenciado do Visual Studio, como um **Aplicativo de Console** ou de um **Aplicativo do Windows**.
    
2. No **Solution Explorer**, clique com o botão **referências**e, em seguida, clique em **Adicionar referência**.
    
3. Na guia **.NET** , clique em **Procurar**, navegue até a < _unidade_>: \Program Files\Microsoft Office\OFFICE14 pasta e clique em Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Clique em **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatizar a alteração do valor de um campo

Vamos supor que um dos clientes do usuário de um modelo de formulário do InfoPath relatório Vendas alterados recentemente seu nome de "Empresa A" para "Empresa B." Um desenvolvedor é solicitado a escrever o código que será atualizada automaticamente os formulários de relatório de vendas salvos deste modelo de formulário para refletir a alteração do nome. O cenário a seguir supõe que um formulário que contenha uma caixa de texto que está acoplada a um campo denominado NomeDoCliente.
  
### <a name="create-the-sample-form-template-and-form"></a>Criar o modelo de formulário de amostra e formulário

1. Abra o InfoPath e crie um modelo de formulário em branco.
    
2. Adicionar um controle de **Caixa de texto** ao formulário e nomeie o campo acoplado NomeDoCliente o controle.
    
3. No painel de tarefas **campos** , clique com botão direito na pasta **myFields** e, em seguida, clique em **Propriedades**.
    
4. Na guia **detalhes** , selecione e copie o seguinte valor **Namespace:** e, em seguida, cole-o no bloco de notas ou em algum outro local onde você possa recuperá-lo. Você precisará esse valor de posteriormente para definir o valor da propriedade **SelectionNamespaces** em seu código. 
    
5. Publique o modelo de formulário para uma pasta denominada C:\Test e aceite o nome padrão, modelo1. 
    
6. Abra o modelo de formulário, adicione o nome "Empresa uma" à caixa de texto vinculada ao campo NomeDoCliente e salve o formulário como "Formulário1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Criar um aplicativo de console do código gerenciado para alterar o nome de 'Uma empresa' 'Empresa b'

1. Abra o Visual Studio e crie um novo Visual c# ou aplicativo de Console do Visual Basic chamado UpdateCustomer.
    
2. Estabelece referências à interoperabilidade primários do Microsoft Office InfoPath e assemblies de interoperabilidade do InfoPath XML, conforme descrito acima.
    
3. Adicione o código a seguir ao arquivo Module. vb ou Module1, certificando-se atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando você criou o formulário de exemplo. 
    
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

4. No menu **Debug** para compilar e executar o aplicativo de console, clique em **Iniciar depuração** . 
    
   O aplicativo abre o formulário salvo como Form1.xml e faz um loop em todos os elementos de NomeDoCliente que contêm o valor empresa A e altera o valor para a empresa B. Quando a operação for concluída, uma nova cópia do formulário é salvo como Form2.xml na pasta C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatizar a abertura de um formulário e ao preencher os valores de campo

O exemplo a seguir automatiza abrir um formulário em branco e preencher o primeiro nome, sobrenome e campos de endereço no formulário. Este cenário pressupõe um formulário que contém três caixas de texto que são vinculadas a campos denominados FirstName, LastName e endereço.
  
### <a name="create-the-sample-form-template-and-form"></a>Criar o modelo de formulário de amostra e formulário

1. Abra o InfoPath e crie um formulário em branco.
    
2. Adicione três controles de caixa de texto ao formulário e nomeie campos acoplados a controles: FirstName, LastName e endereço. Adicione outros campos que você deseja.
    
3. No painel de tarefas **campos** , clique com botão direito na pasta **myFields** e, em seguida, clique em **Propriedades**.
    
4. Na guia **detalhes** , selecione e copie o seguinte valor **Namespace:** e, em seguida, cole-o no bloco de notas ou em algum outro local onde você possa recuperá-lo. Você precisará esse valor de posteriormente para definir o valor da propriedade **SelectionNamespaces** em seu código. 
    
5. Publique o modelo de formulário para uma pasta denominada c:\Temp. e aceite o nome padrão, modelo1.
    
6. Abra o modelo de formulário e salvar um formulário em branco como "Formulário1" como c:\Temp..
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Criar um aplicativo de console do código gerenciado para abrir o formulário e preencha os campos

1. Abra o Visual Studio e crie um novo Visual c# ou aplicativo de Console do Visual Basic chamado OpenForm.
    
2. Estabelece referências à interoperabilidade primários do Microsoft Office InfoPath e assemblies de interoperabilidade do InfoPath XML, conforme descrito acima.
    
3. Adicione o código a seguir ao arquivo Module. vb ou Module1, certificando-se atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando você criou o formulário de exemplo. 
    
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

4. No menu **Depurar** , clique em **Iniciar depuração** para compilar e executar o aplicativo de console. 
    
   O aplicativo abre o formulário salvo como Form1.xml e preencha os campos FirstName, LastName e endereço com os valores especificados no código e, então, salve o formulário, deixando o InfoPath aberta. 
    
## <a name="see-also"></a>Confira também

- [Sobre o assembly de interoperabilidade primário do InfoPath do Microsoft Office](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Sobre o assembly de interoperabilidade do InfoPath XML](about-the-infopath-xml-interop-assembly.md)

