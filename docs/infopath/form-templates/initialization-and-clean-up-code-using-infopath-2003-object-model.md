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
ms.openlocfilehash: 1ae81c261ad9927195c0a4ac6d80f58a16a6ebf1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383118"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003

Por padrão, o FormCode.cs FormCode.vb arquivo ou criado para um projeto de modelo de formulário compatível com o InfoPath 2003 contém o código-fonte para a lógica de programação do formulário. O modelo do projeto gera uma classe no FormCode.cs ou arquivo FormCode.vb como classes nos exemplos a seguir onde você pode definir a inicialização e limpeza código, bem como manipuladores de eventos de formulário. Os arquivos FormCode.cs e FormCode.vb se aplicam a um nível de conjunto do atributo**System.ComponentModel.DescriptionAttribute**, que identifica a classe como a única a classe onde são implementados manipuladores de eventos. O atributo** InfoPathNamespace** (que é implementado pelo [ InfoPathNamespaceAttribute)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) é aplicado a uma classe para identificar os namespaces de seleção DOM XML usados de acordo com a classe. Os namespaces mencionados na** InfoPathNamespace** são mantidos pelo sistema de projeto do InfoPath. 
  
A classe de FormCode fornece `_Startup` os `_Shutdown` métodos usados para executar a inicialização e tipos de treino de limpeza para os componentes necessários além funcionalidade padrão do InfoPath enquanto o formulário estiver aberto. 
  
> [!IMPORTANT]
> Não ligue membros do modelo de objeto do InfoPath das `_Startup` e `_Shutdown` métodos. Você deve inicializar e ligar somente membros dos componentes externo nesses métodos. 
  
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
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
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
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
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

## <a name="the-startup-method"></a>O método Startup

Além de oferecer um local para programar a inicialização componentes adicionais, o `_Startup` método inicializa a `thisXDocument` e `thisApplication` variáveis que podem ser usadas no seu código do formulário para acessar os membros da [ XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) e [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes no modelo de objeto do InfoPath. O código necessário para inicializar duas variáveis é gerado automaticamente pelo modelo de projeto. 
  
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

Os exemplos a seguir mostram um manipulador de eventos simples para um botão que usa `thisXDocument` variáveis para acessar o [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx)do método[tipo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) UIObject. 
  
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

Confira informações sobre como criar um manipulador de eventos [adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="the-shutdown-method"></a>O método _ShutDown

O`_Shutdown` método é o último a ser acionado quando um formulário está fechado. Você pode escrever qualquer código que seja necessário nesse método para limpar ou finalizar componentes usados no formulário. 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a>Exemplo de código de inicialização e limpeza

O exemplo a seguir mostra como inicializar conexão ao banco de dados do Microsoft SQL Server no`_Startup` método e fechar a conexão `_Shutdown` no método. Para que este exemplo funcione corretamente, primeiro você deve definir uma referência a montagem System. Data do .NET Framework clicando em **adicionar referência** no item **Project** do menus e selecionando o Componente System.Data.dll na guia **.NET**. Observe também que a `using System.Data.SqlClient` (ou `Imports System.Data.SqlClient)` diretiva foi adicionada na parte superior do arquivo de código de formulário para reduzir pressionamentos de teclas. 
  
> [!NOTE]
> Os usuários de um formulário do InfoPath com código de forma que se conecta a um banco de dados do SQL Server podem exigir permissões de segurança dependendo de como o formulário está implantado e é definido de política de segurança. Confira mais informações em segurança [sobre o modelo de segurança para modelos de formulário com o código](about-the-security-model-for-form-templates-with-code.md) e [definir configurações de segurança para modelos de formulário com o código](how-to-configure-security-settings-for-form-templates-with-code.md). 
  
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
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
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
            "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
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

## <a name="see-also"></a>Confira também



[Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

