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
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003

Por padrão, o FormCode.cs FormCode.vb arquivo ou que é criado para um projeto de modelo de formulário que é compatível com o InfoPath 2003 contém o código-fonte para a lógica de programação do formulário. O modelo para o projeto gera uma classe no FormCode.cs ou FormCode.vb arquivo muito semelhante as classes nos exemplos a seguir onde é possível definir a inicialização e o código de limpeza, bem como manipuladores de eventos do formulário. Os arquivos FormCode.cs e FormCode.vb aplicam um atributo de **System.ComponentModel.DescriptionAttribute** de nível de assembly, que identifica a classe como a única classe onde os manipuladores de eventos são implementados. O atributo **InfoPathNamespace** (que é implementado pelo tipo [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) é aplicado a uma classe para identificar os espaços para nome XML DOM seleção usados dentro da classe. Os espaços para nome referenciados no **InfoPathNamespace** são mantidos pelo sistema do projeto do InfoPath. 
  
A classe FormCode próprio fornece `_Startup` e `_Shutdown` métodos que são usados para executar a inicialização e rotinas de limpeza para quaisquer componentes que são necessários além da funcionalidade padrão do InfoPath enquanto o formulário está aberto. 
  
> [!IMPORTANT]
> Não chamar membros do modelo de objeto do InfoPath de dentro do `_Startup` e `_Shutdown` métodos. Você deve inicializar e chamar apenas os membros de componentes externos nesses métodos. 
  
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

## <a name="the-startup-method"></a>Método Startup

Além de fornecer um lugar para escrever o código de inicialização de componentes adicionais, o `_Startup` método inicializa o `thisXDocument` e `thisApplication` variáveis que podem ser usados para acessar os membros da [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) e [aplicativo em seu código de formulário ](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx)classes no modelo de objeto do InfoPath. O código necessário para inicializar as duas variáveis é gerado automaticamente pelo modelo de projeto. 
  
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

Os seguintes exemplos mostram um manipulador de eventos simples de um botão que usa o `thisXDocument` variável para acessar o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do tipo [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
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

Para obter informações sobre como criar um manipulador de eventos, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="the-shutdown-method"></a>O método _ShutDown

O `_Shutdown` é o método último chamado quando um formulário é fechado. Você pode escrever qualquer código neste método que não é necessário para limpar ou finalizar componentes usados no formulário. 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a>Exemplo de código de inicialização e a limpeza

O exemplo a seguir mostra como inicializar uma conexão para um banco de dados do Microsoft SQL Server no `_Startup` método e feche a conexão in a `_Shutdown` método. Na ordem para que esse exemplo funcione corretamente, você deve primeiro definir uma referência para o assembly System. Data do .NET Framework clicando em **Adicionar referência** no menu **projeto** e, em seguida, em seguida, selecionando o componente de System.Data.dll no **.NET** guia. Observe também que o `using System.Data.SqlClient` (ou `Imports System.Data.SqlClient)` diretiva foi adicionada na parte superior do arquivo de código de formulário para reduzir os pressionamentos de teclas. 
  
> [!NOTE]
> Os usuários de um formulário do InfoPath que contém o código de formulário que se conecta a um banco de dados do SQL Server podem exigir permissões de segurança, dependendo de como o formulário é implantado e diretiva de segurança é definida. Para obter mais informações sobre segurança, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md) e [Configurar as definições de segurança para modelos de formulário com código](how-to-configure-security-settings-for-form-templates-with-code.md). 
  
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

## <a name="see-also"></a>Confira também



[Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

