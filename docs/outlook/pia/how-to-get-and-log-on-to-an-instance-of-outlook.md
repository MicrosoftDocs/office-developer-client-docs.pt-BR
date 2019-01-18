---
title: Acessar e entrar em uma instância do Outlook
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462097(v=office.15)
ms:contentKeyID: 55119926
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4445d0665ea5a3d36a5ff7c92b5a46cfe4fffaa8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721182"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Acessar e entrar em uma instância do Outlook

Este tópico mostra como obter um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) que representa uma instância ativa do Microsoft Outlook, se houver uma em execução no computador local, ou para criar uma nova instância do Outlook, entre no perfil padrão e retorne essa instância do Outlook.

## <a name="example"></a>Exemplo

> [!NOTE] 
> Helmut Obertanner forneceu os exemplos de código a seguir. A experiência de Helmut é em Ferramentas de Desenvolvedor do Office para Visual Studio e Outlook. 

Os exemplos de código a seguir contêm o método GetApplicationObject da classe Sample, implementados como parte de um projeto de suplemento do Outlook. Cada projeto adiciona uma referência para o Outlook PIA, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).

O método GetApplicationObject usa classes na biblioteca de classes .NET Framework para verificar e obter qualquer processo do Outlook em execução no computador local. Ele primeiro usa o método [GetProcessesByName](https://msdn.microsoft.com/en-us/library/wbt7d3cy) da classe [Process](https://msdn.microsoft.com/en-us/library/ccf1tfx0) no namespace [System.Diagnostics](https://msdn.microsoft.com/en-us/library/15t15zda) para obter uma matriz de componentes de processo no computador local que compartilham o nome do processo "OUTLOOK". Para verificar se a matriz contém pelo menos um processo do Outlook, GetApplicationObject usa o Microsoft Language Integrated Query (LINQ). A classe [Enumerable](https://msdn.microsoft.com/en-us/library/bb345746) no namespace [System.Linq](https://msdn.microsoft.com/en-us/library/bb336768) fornece um conjunto de métodos, incluindo o método [Count](https://msdn.microsoft.com/en-us/library/bb357758) que implementa a interface genérica [IEnumerable\<T\>](https://msdn.microsoft.com/en-us/library/9eekhta0). Como a classe [Array](https://msdn.microsoft.com/en-us/library/czz5hkty) implementa a interface **IEnumerable(T)**, GetApplicationObject pode aplicar o método **Count** para a matriz retornada por **GetProcessesByName** para ver se há um processo do Outlook em execução. Se houver, o GetApplicationObject usa o método [GetActiveObject](https://msdn.microsoft.com/en-us/library/xt620x09) da classe [Marshal](https://msdn.microsoft.com/en-us/library/asx0thw2) no namespace [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) para obter essa instância do Outlook, e projeta esse objeto para um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) do Outlook.

Se o Outlook não estiver sendo executado no computador local, o GetApplicationObject criará uma nova instância do Outlook, usará o método [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para entrar no perfil padrão e retornará a nova instância do Outlook.

A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública. As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>Confira também

- [Sessões](sessions.md)

