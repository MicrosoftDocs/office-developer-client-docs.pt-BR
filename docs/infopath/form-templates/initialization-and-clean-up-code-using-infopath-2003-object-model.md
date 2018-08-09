---
title: Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com 2003 do InfoPath, o código de limpeza, modelos de formulário compatíveis com o InfoPath 2003, código de inicialização
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: Por padrão, o FormCode.cs FormCode.vb arquivo ou que é criado para um projeto de modelo de formulário que é compatível com o InfoPath 2003 contém o código-fonte para a lógica de programação do formulário. O modelo para o projeto gera uma classe no FormCode.cs ou FormCode.vb arquivo muito semelhante as classes nos exemplos a seguir onde é possível definir a inicialização e o código de limpeza, bem como manipuladores de eventos do formulário. Os arquivos FormCode.cs e FormCode.vb aplicam um atributo de System.ComponentModel.DescriptionAttribute de nível de assembly, que identifica a classe como a única classe onde os manipuladores de eventos são implementados. O atributo InfoPathNamespace (que é implementado pelo tipo InfoPathNamespaceAttribute) é aplicado a uma classe para identificar os espaços para nome XML DOM seleção usados dentro da classe. Os espaços para nome referenciados no InfoPathNamespace são mantidos pelo sistema do projeto do InfoPath.
ms.openlocfilehash: 7111a8525b092998e21d4c267b5884f50fdb9777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765627"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a><span data-ttu-id="74c80-108">Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="74c80-108">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>

<span data-ttu-id="74c80-109">Por padrão, o FormCode.cs FormCode.vb arquivo ou que é criado para um projeto de modelo de formulário que é compatível com o InfoPath 2003 contém o código-fonte para a lógica de programação do formulário.</span><span class="sxs-lookup"><span data-stu-id="74c80-109">By default, the FormCode.cs or FormCode.vb file that is created for a form template project that is compatible with InfoPath 2003 contains all the source code for the programming logic of the form.</span></span> <span data-ttu-id="74c80-110">O modelo para o projeto gera uma classe no FormCode.cs ou FormCode.vb arquivo muito semelhante as classes nos exemplos a seguir onde é possível definir a inicialização e o código de limpeza, bem como manipuladores de eventos do formulário.</span><span class="sxs-lookup"><span data-stu-id="74c80-110">The template for the project generates a class in the FormCode.cs or FormCode.vb file much like the classes in the following examples where you can define initialization and clean-up code, as well as handlers for form events.</span></span> <span data-ttu-id="74c80-111">Os arquivos FormCode.cs e FormCode.vb aplicam um atributo de **System.ComponentModel.DescriptionAttribute** de nível de assembly, que identifica a classe como a única classe onde os manipuladores de eventos são implementados.</span><span class="sxs-lookup"><span data-stu-id="74c80-111">The FormCode.cs and FormCode.vb files apply an assembly-level **System.ComponentModel.DescriptionAttribute** attribute, which identifies the class as the only class where event handlers are implemented.</span></span> <span data-ttu-id="74c80-112">O atributo **InfoPathNamespace** (que é implementado pelo tipo [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) é aplicado a uma classe para identificar os espaços para nome XML DOM seleção usados dentro da classe.</span><span class="sxs-lookup"><span data-stu-id="74c80-112">The **InfoPathNamespace** attribute (which is implemented by the [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) type) is applied to a class to identify the XML DOM selection namespaces used within the class.</span></span> <span data-ttu-id="74c80-113">Os espaços para nome referenciados no **InfoPathNamespace** são mantidos pelo sistema do projeto do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="74c80-113">The namespaces referenced in the **InfoPathNamespace** are maintained by the InfoPath project system.</span></span> 
  
<span data-ttu-id="74c80-114">A classe FormCode próprio fornece `_Startup` e `_Shutdown` métodos que são usados para executar a inicialização e rotinas de limpeza para quaisquer componentes que são necessários além da funcionalidade padrão do InfoPath enquanto o formulário está aberto.</span><span class="sxs-lookup"><span data-stu-id="74c80-114">The FormCode class itself provides  `_Startup` and  `_Shutdown` methods that are used to perform initialization and clean-up routines for any components that are required in addition to standard InfoPath functionality while the form is open.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="74c80-115">Não chamar membros do modelo de objeto do InfoPath de dentro do `_Startup` e `_Shutdown` métodos.</span><span class="sxs-lookup"><span data-stu-id="74c80-115">Do not call members of the InfoPath object model from within the  `_Startup` and  `_Shutdown` methods.</span></span> <span data-ttu-id="74c80-116">Você deve inicializar e chamar apenas os membros de componentes externos nesses métodos.</span><span class="sxs-lookup"><span data-stu-id="74c80-116">You should initialize and call only members of external components in these methods.</span></span> 
  
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

## <a name="the-startup-method"></a><span data-ttu-id="74c80-117">Método Startup</span><span class="sxs-lookup"><span data-stu-id="74c80-117">The _Startup Method</span></span>

<span data-ttu-id="74c80-118">Além de fornecer um lugar para escrever o código de inicialização de componentes adicionais, o `_Startup` método inicializa o `thisXDocument` e `thisApplication` variáveis que podem ser usados para acessar os membros da [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) e [aplicativo em seu código de formulário ](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx)classes no modelo de objeto do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="74c80-118">In addition to providing a place to write initialization code for additional components, the  `_Startup` method initializes the  `thisXDocument` and  `thisApplication` variables that can be used in your form code to access the members of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) and [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes in the InfoPath object model.</span></span> <span data-ttu-id="74c80-119">O código necessário para inicializar as duas variáveis é gerado automaticamente pelo modelo de projeto.</span><span class="sxs-lookup"><span data-stu-id="74c80-119">The code necessary to initialize the two variables is generated automatically by the project template.</span></span> 
  
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

<span data-ttu-id="74c80-120">Os seguintes exemplos mostram um manipulador de eventos simples de um botão que usa o `thisXDocument` variável para acessar o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do tipo [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="74c80-120">The following examples show a simple event handler for a button that uses the  `thisXDocument` variable to access the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) type.</span></span> 
  
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

<span data-ttu-id="74c80-121">Para obter informações sobre como criar um manipulador de eventos, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="74c80-121">For information on how to create an event handler, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="the-shutdown-method"></a><span data-ttu-id="74c80-122">O método _ShutDown</span><span class="sxs-lookup"><span data-stu-id="74c80-122">The _ShutDown Method</span></span>

<span data-ttu-id="74c80-123">O `_Shutdown` é o método último chamado quando um formulário é fechado.</span><span class="sxs-lookup"><span data-stu-id="74c80-123">The  `_Shutdown` method is the last method called when a form is closed.</span></span> <span data-ttu-id="74c80-124">Você pode escrever qualquer código neste método que não é necessário para limpar ou finalizar componentes usados no formulário.</span><span class="sxs-lookup"><span data-stu-id="74c80-124">You can write any code in this method that is needed to clean up or finalize components used in the form.</span></span> 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a><span data-ttu-id="74c80-125">Exemplo de código de inicialização e a limpeza</span><span class="sxs-lookup"><span data-stu-id="74c80-125">Initialization and Clean-up Code Example</span></span>

<span data-ttu-id="74c80-126">O exemplo a seguir mostra como inicializar uma conexão para um banco de dados do Microsoft SQL Server no `_Startup` método e feche a conexão in a `_Shutdown` método.</span><span class="sxs-lookup"><span data-stu-id="74c80-126">The following example shows how to initialize a connection to a Microsoft SQL Server database in the  `_Startup` method and close the connection in the  `_Shutdown` method.</span></span> <span data-ttu-id="74c80-127">Na ordem para que esse exemplo funcione corretamente, você deve primeiro definir uma referência para o assembly System. Data do .NET Framework clicando em **Adicionar referência** no menu **projeto** e, em seguida, em seguida, selecionando o componente de System.Data.dll no **.NET** guia. Observe também que o `using System.Data.SqlClient` (ou `Imports System.Data.SqlClient)` diretiva foi adicionada na parte superior do arquivo de código de formulário para reduzir os pressionamentos de teclas.</span><span class="sxs-lookup"><span data-stu-id="74c80-127">In order for this example to work correctly, you must first set a reference to the System.Data assembly of the .NET Framework by clicking **Add Reference** on the **Project** menu, and then selecting the System.Data.dll component on the **.NET** tab. Also note that the  `using System.Data.SqlClient` (or  `Imports System.Data.SqlClient)` directive was added at the top of the form code file to reduce keystrokes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="74c80-128">Os usuários de um formulário do InfoPath que contém o código de formulário que se conecta a um banco de dados do SQL Server podem exigir permissões de segurança, dependendo de como o formulário é implantado e diretiva de segurança é definida.</span><span class="sxs-lookup"><span data-stu-id="74c80-128">Users of an InfoPath form that contains form code that connects to a SQL Server database may require security permissions depending on how the form is deployed and security policy is defined.</span></span> <span data-ttu-id="74c80-129">Para obter mais informações sobre segurança, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md) e [Configurar as definições de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="74c80-129">For more information on security see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md) and [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="74c80-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="74c80-130">See also</span></span>



[<span data-ttu-id="74c80-131">Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="74c80-131">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

