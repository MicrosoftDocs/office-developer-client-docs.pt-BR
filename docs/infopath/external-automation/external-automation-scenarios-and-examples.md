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
# <a name="external-automation-scenarios-and-examples"></a>Cenários e exemplos de automação externa

Os membros fornecidos pelo assembly de interoperabilidade primário do Microsoft Office InfoPath (Microsoft.Office.Interop.InfoPath.dll) e pelo assembly de interoperabilidade XML do InfoPath (Microsoft.Office.Interop.InfoPath.Xml.dll) permitem escrever código gerenciado para automatizar o InfoPath. 
  
## <a name="establishing-references-to-the-microsoft-office-infopath-primary-interop-and-infopath-xml-interop-assemblies"></a>Estabelecer referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath

Para escrever um código gerenciado que automatize o InfoPath, você deve estabelecer referências ao assembly de interoperabilidade primário do Microsoft InfoPath e ao assembly de interoperabilidade XML do InfoPath. O assembly de interoperabilidade primário do Microsoft InfoPath fornece suporte para interoperabilidade com o modelo de objeto COM exposto por IPEDITOR.DLL, usando os membros do namespace [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx). O assembly de interoperabilidade XML do InfoPath fornece suporte para interoperabilidade com o modelo de objeto COM exposto pelo Microsoft XML Core Services (MSXML) usando os membros do namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml). 
  
> [!IMPORTANT]
> Os usuários de aplicativos de código gerenciado que automatizam o InfoPath devem ter o InfoPath, o assembly de interoperabilidade primário do Microsoft Office InfoPath e o assembly de interoperabilidade XML do InfoPath instalados em seus computadores. A opção **Suporte à Programação .NET** no programa de instalação do InfoPath está definida como **Executar do Meu Computador** para uma instalação típica do InfoPath.
>  
> Como resultado, desde que o Redistribuível do .NET Framework 1.1 ou o .NET Framework 1.1 Software Development Kit (SDK) ou posterior esteja instalado, esses módulos de interoperabilidade também serão instalados por padrão. Se esses módulos de interoperabilidade não estiverem disponíveis no computador de um usuário, você deve confirmar se o .NET Framework 1.1 ou posterior está instalado e executar **Programas e Recursos** no **Painel de Controle** para alterar a configuração e definir a opção **Suporte à Programação .NET** do InfoPath para **Executar do Meu Computador**. 
  
Os procedimentos a seguir descrevem como definir referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath em um projeto do Visual Studio.
  
Para definir uma referência ao assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath, defina uma referência à **Biblioteca de Tipos do Microsoft InfoPath 3.0** na guia **COM** da caixa de diálogo **Adicionar Referência**. Mesmo que você defina uma referência na guia **COM**, é estabelecida uma referência com o assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath.dll instalado no GAC (Cache de Assembly Global) pelo programa de instalação do InfoPath. 
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopath-primary-interop-assembly"></a>Definir uma referência ao assembly de interoperabilidade primário Microsoft.Office.Interop.InfoPath

1. Abra um projeto de código gerenciado do Visual Studio.
    
2. No **Gerenciador de Soluções**, clique com o botão direito do mouse em **Referências** e clique em **Adicionar Referência**.
    
3. Na guia **COM**, clique duas vezes em **Biblioteca de Tipos do Microsoft InfoPath 3.0** e depois clique em **OK**.
    
Para definir uma referência ao assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.Xml, navegue até o arquivo Microsoft.Office.Interop.InfoPath.Xml.dll instalado por padrão na pasta <_unidade_>:\Arquivos de Programa\Microsoft Office\OFFICE14. Mesmo que você especifique a cópia do assembly no sistema de arquivos local, esse procedimento estabelece uma referência ao assembly Microsoft.Office.Interop.InfoPath.Xml.dll instalado no GAC (Cache de Assembly Global) pelo programa de instalação do InfoPath.
  
### <a name="set-a-reference-to-the-microsoftofficeinteropinfopathxml-interop-assembly"></a>Definir uma referência ao assembly de interoperabilidade Microsoft.Office.Interop.InfoPath.Xml

1. Abra ou crie um projeto de código gerenciado do Visual Studio, como um **Aplicativo de Console** ou um **Aplicativo do Windows**.
    
2. No **Gerenciador de Soluções**, clique com o botão direito do mouse em **Referências** e clique em **Adicionar Referência**.
    
3. Na guia **.NET**, clique em **Procurar**, navegue até a pasta <_unidade_>:\Arquivos de Programa\Microsoft Office\OFFICE14 e clique em Microsoft.Office.Interop.InfoPath.Xml.dll.
    
4. Clique em **OK**.
    
## <a name="automate-changing-the-value-of-a-field"></a>Automatizar a alteração do valor de um campo

Suponha que um dos clientes do usuário de um modelo de formulário de relatório de vendas do InfoPath tenha alterado recentemente seu nome de "Empresa A" para "Empresa B". Um desenvolvedor é solicitado a escrever um código que atualize automaticamente os formulários de relatórios de vendas salvos desse modelo de formulário para refletir a alteração no nome. O cenário a seguir pressupõe um formulário que contém uma caixa de texto associada a um campo denominado customerName.
  
### <a name="create-the-sample-form-template-and-form"></a>Criar um exemplo de modelo de formulário e de formulário

1. Abra o InfoPath e crie um modelo de formulário em branco.
    
2. Adicione um controle **Caixa de Texto** ao formulário e nomeie o campo associado a esse controle como customerName.
    
3. No painel de tarefas **Campos**, clique com o botão direito do mouse na pasta **meusCampos** e clique em **Propriedades**.
    
4. Na guia **Detalhes**, selecione e copie o valor após **Namespace:** e cole-o no Bloco de Notas ou em outro local em que você possa recuperá-lo. Você precisará desse valor mais tarde para definir o valor da propriedade **SelectionNamespaces** no seu código. 
    
5. Publique o modelo de formulário em uma pasta nomeada C:\Test e aceite o nome padrão, Template1. 
    
6. Abra o modelo de formulário, adicione o nome "Empresa A" à caixa de texto associada ao campo customerName e depois salve o formulário como "Form1". 
    
### <a name="create-a-managed-code-console-application-to-change-the-name-from-company-a-to-company-b"></a>Criar um aplicativo de console de código gerenciado para alterar o nome de "Empresa A" para "Empresa B"

1. Abra o Visual Studio e crie um novo Aplicativo de Console do Visual C # ou Visual Basic com o nome UpdateCustomer.
    
2. Estabeleça referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath, conforme descrito acima.
    
3. Adicione o seguinte código ao arquivo Program.cs ou Module1.vb, certificando-se de atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando criou o formulário de exemplo. 
    
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

4. Clique em **Iniciar Depuração** no menu **Depurar** para compilar e executar o aplicativo de console. 
    
   O aplicativo abre o formulário salvo como Form1.xml e circula por todos os elementos customerName que contêm o valor Empresa A, alterando esse valor para Empresa B. Quando a operação é concluída, uma nova cópia do formulário é salva como Form2.xml na pasta C:\Test. 
    
## <a name="automate-opening-a-form-and-populating-field-values"></a>Automatizar a abertura de um formulário e o preenchimento de valores de campos

O exemplo a seguir automatiza a abertura de um formulário em branco e o preenchimento dos campos de nome, sobrenome e endereço no formulário. Esse cenário pressupõe um formulário que contém três caixas de texto associadas aos campos FirstName, LastName e Address.
  
### <a name="create-the-sample-form-template-and-form"></a>Criar um exemplo de modelo de formulário e de formulário

1. Abra o InfoPath e crie um formulário em branco.
    
2. Adicione três controles de caixa de texto ao formulário e forneça os seguintes nomes aos campos associados a esses controles: FirstName, LastName e Address. Adicione outros campos, se desejar.
    
3. No painel de tarefas **Campos**, clique com o botão direito do mouse na pasta **meusCampos** e clique em **Propriedades**.
    
4. Na guia **Detalhes**, selecione e copie o valor após **Namespace:** e cole-o no Bloco de Notas ou em outro local em que você possa recuperá-lo. Você precisará desse valor mais tarde para definir o valor da propriedade **SelectionNamespaces** no seu código. 
    
5. Publique o modelo de formulário em uma pasta chamada C:\Temp e aceite o nome padrão, Template1.
    
6. Abra o modelo de formulário e salve um formulário em branco como "Form1" em C:\Temp.
    
### <a name="create-a-managed-code-console-application-to-open-the-form-and-populate-the-fields"></a>Criar um aplicativo de console de código gerenciado para abrir o formulário e preencher os campos

1. Abra o Visual Studio e crie um novo Aplicativo de Console do Visual C # ou Visual Basic com o nome OpenForm.
    
2. Estabeleça referências ao assembly de interoperabilidade primário do Microsoft Office InfoPath e ao assembly de interoperabilidade XML do InfoPath, conforme descrito acima.
    
3. Adicione o seguinte código ao arquivo Program.cs ou Module1.vb, certificando-se de atualizar o valor do namespace na configuração da propriedade **SelectionNamespaces** com o valor que você copiou quando criou o formulário de exemplo. 
    
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

4. No menu **Depurar**, clique em **Iniciar Depuração** para compilar e executar o aplicativo de console. 
    
   O aplicativo abrirá o formulário salvo como Form1.xml e preencherá os campos FirstName, LastName e Address com os valores especificados no código. Em seguida, ele salvará o formulário, deixando o InfoPath aberto. 
    
## <a name="see-also"></a>Confira também

- [Sobre o assembly de interoperabilidade primário do Microsoft Office InfoPath](about-the-microsoft-office-infopath-primary-interop-assembly.md)
- [Sobre o assembly de interoperabilidade XML do InfoPath](about-the-infopath-xml-interop-assembly.md)

