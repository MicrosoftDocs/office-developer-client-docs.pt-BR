---
title: Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatível com o 2003 InfoPath, código de limpeza, modelos de formulário do InfoPath 2003 compatível, código inicialização
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: Por padrão, o FormCode.cs FormCode.vb arquivo ou criado para um projeto de modelo de formulário compatível com o InfoPath 2003 contém o código-fonte para a lógica de programação do formulário. O modelo do projeto gera uma classe no FormCode.cs ou arquivo FormCode.vb como classes nos exemplos a seguir onde você pode definir a inicialização e limpeza código, bem como manipuladores de eventos de formulário. Os arquivos FormCode.cs e FormCode.vb aplicam um nível de montagem no atributo de System.ComponentModel.DescriptionAttribute, isso identifica a classe como a única classe onde são implementados manipuladores de eventos. O atributo InfoPathNamespace (que é implementado pelo InfoPathNamespaceAttribute) é aplicado a uma classe para identificar os namespaces de seleção DOM XML usados de acordo com a classe. Os namespaces mencionados na InfoPathNamespace são mantidos pelo sistema de projeto do InfoPath.
ms.openlocfilehash: 659214a21dacf75b12f36cb6ad1e7f09c5af8800
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538365"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a><span data-ttu-id="7816c-108">Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="7816c-108">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>

<span data-ttu-id="7816c-109">Por padrão, o FormCode.cs FormCode.vb arquivo ou criado para um projeto de modelo de formulário compatível com o InfoPath 2003 contém o código-fonte para a lógica de programação do formulário.</span><span class="sxs-lookup"><span data-stu-id="7816c-109">By default, the FormCode.cs or FormCode.vb file that is created for a form template project that is compatible with InfoPath 2003 contains all the source code for the programming logic of the form.</span></span> <span data-ttu-id="7816c-110">O modelo do projeto gera uma classe no FormCode.cs ou arquivo FormCode.vb como classes nos exemplos a seguir onde você pode definir a inicialização e limpeza código, bem como manipuladores de eventos de formulário.</span><span class="sxs-lookup"><span data-stu-id="7816c-110">The template for the project generates a class in the FormCode.cs or FormCode.vb file much like the classes in the following examples where you can define initialization and clean-up code, as well as handlers for form events.</span></span> <span data-ttu-id="7816c-111">Os arquivos FormCode.cs e FormCode.vb se aplicam a um nível de conjunto do atributo**System.ComponentModel.DescriptionAttribute**, que identifica a classe como a única a classe onde são implementados manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="7816c-111">The FormCode.cs and FormCode.vb files apply an assembly-level **System.ComponentModel.DescriptionAttribute** attribute, which identifies the class as the only class where event handlers are implemented.</span></span> <span data-ttu-id="7816c-112">O atributo\*\* InfoPathNamespace\*\* (que é implementado pelo [ InfoPathNamespaceAttribute)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) é aplicado a uma classe para identificar os namespaces de seleção DOM XML usados de acordo com a classe.</span><span class="sxs-lookup"><span data-stu-id="7816c-112">The **InfoPathNamespace** attribute (which is implemented by the [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) type) is applied to a class to identify the XML DOM selection namespaces used within the class.</span></span> <span data-ttu-id="7816c-113">Os namespaces mencionados na\*\* InfoPathNamespace\*\* são mantidos pelo sistema de projeto do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7816c-113">The namespaces referenced in the **InfoPathNamespace** are maintained by the InfoPath project system.</span></span> 
  
<span data-ttu-id="7816c-114">A classe de FormCode fornece `_Startup` os `_Shutdown` métodos usados para executar a inicialização e tipos de treino de limpeza para os componentes necessários além funcionalidade padrão do InfoPath enquanto o formulário estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="7816c-114">The FormCode class itself provides  `_Startup` and  `_Shutdown` methods that are used to perform initialization and clean-up routines for any components that are required in addition to standard InfoPath functionality while the form is open.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7816c-115">Não ligue membros do modelo de objeto do InfoPath das `_Startup` e `_Shutdown` métodos.</span><span class="sxs-lookup"><span data-stu-id="7816c-115">Do not call members of the InfoPath object model from within the  `_Startup` and  `_Shutdown` methods.</span></span> <span data-ttu-id="7816c-116">Você deve inicializar e ligar somente membros dos componentes externo nesses métodos.</span><span class="sxs-lookup"><span data-stu-id="7816c-116">You should initialize and call only members of external components in these methods.</span></span> 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
    public partial class FormCode
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // You can add additional initialization code here.
        }
        public void _Shutdown()
        {
        }
    }
}
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
    ' The namespace prefixes defined in this attribute must remain synchronized with
    ' those in the form definition file (.xsf).
    <InfoPathNamespace( _
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
    Public Class FormCode
        Private thisXDocument As XDocument
        Private thisApplication As Application
        Public Sub _Startup(app As Application, doc As XDocument)
            thisXDocument = doc
            thisApplication = app
            ' You can add additional initialization code here.
        End Sub
        Public Sub _Shutdown()
        End Sub
    End Class
End Namespace
```

## <a name="the-startup-method"></a><span data-ttu-id="7816c-117">O método Startup</span><span class="sxs-lookup"><span data-stu-id="7816c-117">The _Startup Method</span></span>

<span data-ttu-id="7816c-118">Além de oferecer um local para programar a inicialização componentes adicionais, o `_Startup` método inicializa a `thisXDocument` e `thisApplication` variáveis que podem ser usadas no seu código do formulário para acessar os membros da [ XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) e [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes no modelo de objeto do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7816c-118">In addition to providing a place to write initialization code for additional components, the  `_Startup` method initializes the  `thisXDocument` and  `thisApplication` variables that can be used in your form code to access the members of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) and [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes in the InfoPath object model.</span></span> <span data-ttu-id="7816c-119">O código necessário para inicializar duas variáveis é gerado automaticamente pelo modelo de projeto.</span><span class="sxs-lookup"><span data-stu-id="7816c-119">The code necessary to initialize the two variables is generated automatically by the project template.</span></span> 
  
```cs
    private XDocument thisXDocument;
    private Application thisApplication;
    public void _Startup(Application app, XDocument doc)
    {
        thisXDocument = doc;
        thisApplication = app;
        // You can add additional initialization code here.
    }
```

```vb
    Private thisXDocument As XDocument
    Private thisApplication As Application
    Public Sub _Startup(app As Application, doc As XDocument)
        thisXDocument = doc
        thisApplication = app
        ' You can add additional initialization code here.
    End Sub

```

<span data-ttu-id="7816c-120">Os exemplos a seguir mostram um manipulador de eventos simples para um botão que usa `thisXDocument` variáveis para acessar o [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx)do método[tipo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) UIObject.</span><span class="sxs-lookup"><span data-stu-id="7816c-120">The following examples show a simple event handler for a button that uses the  `thisXDocument` variable to access the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) type.</span></span> 
  
```cs
[InfoPathEventHandler(MatchPath="CTRL1_5", EventType=InfoPathEventType.OnClick)]
public void CTRL1_5_OnClick(DocActionEvent e)
{
    // Write your code here.
    thisXDocument.UI.Alert("Hello!");
}
```

```vb
<InfoPathEventHandler(MatchPath:="CTRL1_5", EventType:=InfoPathEventType.OnClick)> _
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
    ' Write your code here.
    thisXDocument.UI.Alert("Hello!")
End Sub
```

<span data-ttu-id="7816c-121">Confira informações sobre como criar um manipulador de eventos [adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="7816c-121">For information on how to create an event handler, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="the-shutdown-method"></a><span data-ttu-id="7816c-122">O método _ShutDown</span><span class="sxs-lookup"><span data-stu-id="7816c-122">The _ShutDown Method</span></span>

<span data-ttu-id="7816c-123">O`_Shutdown` método é o último a ser acionado quando um formulário está fechado.</span><span class="sxs-lookup"><span data-stu-id="7816c-123">The  `_Shutdown` method is the last method called when a form is closed.</span></span> <span data-ttu-id="7816c-124">Você pode escrever qualquer código que seja necessário nesse método para limpar ou finalizar componentes usados no formulário.</span><span class="sxs-lookup"><span data-stu-id="7816c-124">You can write any code in this method that is needed to clean up or finalize components used in the form.</span></span> 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a><span data-ttu-id="7816c-125">Exemplo de código de inicialização e limpeza</span><span class="sxs-lookup"><span data-stu-id="7816c-125">Initialization and Clean-up Code Example</span></span>

<span data-ttu-id="7816c-126">O exemplo a seguir mostra como inicializar conexão ao banco de dados do Microsoft SQL Server no`_Startup` método e fechar a conexão `_Shutdown` no método.</span><span class="sxs-lookup"><span data-stu-id="7816c-126">The following example shows how to initialize a connection to a Microsoft SQL Server database in the  `_Startup` method and close the connection in the  `_Shutdown` method.</span></span> <span data-ttu-id="7816c-127">Para que este exemplo funcione corretamente, primeiro você deve definir uma referência a montagem System. Data do .NET Framework clicando em **adicionar referência** no item **Project** do menus e selecionando o Componente System.Data.dll na guia **.NET**. Observe também que a `using System.Data.SqlClient` (ou `Imports System.Data.SqlClient)` diretiva foi adicionada na parte superior do arquivo de código de formulário para reduzir pressionamentos de teclas.</span><span class="sxs-lookup"><span data-stu-id="7816c-127">In order for this example to work correctly, you must first set a reference to the System.Data assembly of the .NET Framework by clicking **Add Reference** on the **Project** menu, and then selecting the System.Data.dll component on the **.NET** tab. Also note that the  `using System.Data.SqlClient` (or  `Imports System.Data.SqlClient)` directive was added at the top of the form code file to reduce keystrokes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7816c-128">Os usuários de um formulário do InfoPath com código de forma que se conecta a um banco de dados do SQL Server podem exigir permissões de segurança dependendo de como o formulário está implantado e é definido de política de segurança.</span><span class="sxs-lookup"><span data-stu-id="7816c-128">Users of an InfoPath form that contains form code that connects to a SQL Server database may require security permissions depending on how the form is deployed and security policy is defined.</span></span> <span data-ttu-id="7816c-129">Confira mais informações em segurança [sobre o modelo de segurança para modelos de formulário com o código](about-the-security-model-for-form-templates-with-code.md) e [definir configurações de segurança para modelos de formulário com o código](how-to-configure-security-settings-for-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="7816c-129">For more information on security see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md) and [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span></span> 
  
```cs
using System;
using System.Data.SqlClient;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
    public partial class Template1
    {
        private XDocument    thisXDocument;
        private Application    thisApplication;
        private SqlConnection sqlConnect;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // Initialize variable for SQL Server connection.
            sqlConnect= new SqlConnection("server=localhost;Trusted_Connection=yes;database=Northwind");
        }
        public void _Shutdown()
        {
            // Close SQL Server connection at shut down.
            sqlConnect.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Data.SqlClient
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
        ' The namespace prefixes defined in this attribute must remain synchronized with
        ' those in the form definition file (.xsf).
        <InfoPathNamespace( _
            "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
        Public Class Template1
            Private thisXDocument As XDocument
            Private thisApplication As Application
            Private sqlConnect As SqlConnection
            Public Sub _Startup(app As Application, doc As XDocument)
                thisXDocument = doc
                thisApplication = app
                ' Initialize variable for SQL Server connection.
                sqlConnect = New SqlConnection _("server=localhost;Trusted_Connection=yes;database=Northwind")
            End Sub
        Public Sub _Shutdown()
            ' Close SQL Server connection.
            sqlConnect.Close()
        End Sub
    End Class
End Namespace
```

## <a name="see-also"></a><span data-ttu-id="7816c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7816c-130">See also</span></span>



[<span data-ttu-id="7816c-131">Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="7816c-131">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

