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
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a><span data-ttu-id="e3f93-102">Acessar e entrar em uma instância do Outlook</span><span class="sxs-lookup"><span data-stu-id="e3f93-102">Get and sign in to an instance of Outlook</span></span>

<span data-ttu-id="e3f93-103">Este tópico mostra como obter um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) que representa uma instância ativa do Microsoft Outlook, se houver uma em execução no computador local, ou para criar uma nova instância do Outlook, entre no perfil padrão e retorne essa instância do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3f93-103">This topic shows how to obtain an [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that represents an active instance of Microsoft Outlook, if there is one running on the local computer, or to create a new instance of Outlook, sign in to the default profile, and return that instance of Outlook.</span></span>

## <a name="example"></a><span data-ttu-id="e3f93-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3f93-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e3f93-105">Helmut Obertanner forneceu os exemplos de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3f93-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="e3f93-106">A experiência de Helmut é em Ferramentas de Desenvolvedor do Office para Visual Studio e Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3f93-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="e3f93-107">Os exemplos de código a seguir contêm o método GetApplicationObject da classe Sample, implementados como parte de um projeto de suplemento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3f93-107">The following code examples contain the GetApplicationObject method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="e3f93-108">Cada projeto adiciona uma referência para o Outlook PIA, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e3f93-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="e3f93-109">O método GetApplicationObject usa classes na biblioteca de classes .NET Framework para verificar e obter qualquer processo do Outlook em execução no computador local.</span><span class="sxs-lookup"><span data-stu-id="e3f93-109">The GetApplicationObject method uses classes in the .NET Framework class library to check and obtain any Outlook process running on the local computer.</span></span> <span data-ttu-id="e3f93-110">Ele primeiro usa o método [GetProcessesByName](https://msdn.microsoft.com/en-us/library/wbt7d3cy) da classe [Process](https://msdn.microsoft.com/en-us/library/ccf1tfx0) no namespace [System.Diagnostics](https://msdn.microsoft.com/en-us/library/15t15zda) para obter uma matriz de componentes de processo no computador local que compartilham o nome do processo "OUTLOOK".</span><span class="sxs-lookup"><span data-stu-id="e3f93-110">It first uses the [GetProcessesByName](https://msdn.microsoft.com/en-us/library/wbt7d3cy) method of the [Process](https://msdn.microsoft.com/en-us/library/ccf1tfx0) class in the [System.Diagnostics](https://msdn.microsoft.com/en-us/library/15t15zda) namespace to obtain an array of process components on the local computer that share the process name "OUTLOOK".</span></span> <span data-ttu-id="e3f93-111">Para verificar se a matriz contém pelo menos um processo do Outlook, GetApplicationObject usa o Microsoft Language Integrated Query (LINQ).</span><span class="sxs-lookup"><span data-stu-id="e3f93-111">To check whether the array does contain at least one Outlook process, GetApplicationObject uses Microsoft Language Integrated Query (LINQ).</span></span> <span data-ttu-id="e3f93-112">A classe [Enumerable](https://msdn.microsoft.com/en-us/library/bb345746) no namespace [System.Linq](https://msdn.microsoft.com/en-us/library/bb336768) fornece um conjunto de métodos, incluindo o método [Count](https://msdn.microsoft.com/en-us/library/bb357758) que implementa a interface genérica [IEnumerable\<T\>](https://msdn.microsoft.com/en-us/library/9eekhta0).</span><span class="sxs-lookup"><span data-stu-id="e3f93-112">The [Enumerable](https://msdn.microsoft.com/en-us/library/bb345746) class in the [System.Linq](https://msdn.microsoft.com/en-us/library/bb336768) namespace provides a set of methods, including the [Count](https://msdn.microsoft.com/en-us/library/bb357758) method, that implement the [IEnumerable\<T\>](https://msdn.microsoft.com/en-us/library/9eekhta0) generic interface.</span></span> <span data-ttu-id="e3f93-113">Como a classe [Array](https://msdn.microsoft.com/en-us/library/czz5hkty) implementa a interface **IEnumerable(T)**, GetApplicationObject pode aplicar o método **Count** para a matriz retornada por **GetProcessesByName** para ver se há um processo do Outlook em execução.</span><span class="sxs-lookup"><span data-stu-id="e3f93-113">Because the [Array](https://msdn.microsoft.com/en-us/library/czz5hkty) class implements the **IEnumerable(T)** interface, GetApplicationObject can apply the **Count** method to the array returned by **GetProcessesByName** to see whether there is an Outlook process running.</span></span> <span data-ttu-id="e3f93-114">Se houver, o GetApplicationObject usa o método [GetActiveObject](https://msdn.microsoft.com/en-us/library/xt620x09) da classe [Marshal](https://msdn.microsoft.com/en-us/library/asx0thw2) no namespace [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) para obter essa instância do Outlook, e projeta esse objeto para um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3f93-114">If there is, GetApplicationObject uses the [GetActiveObject](https://msdn.microsoft.com/en-us/library/xt620x09) method of the [Marshal](https://msdn.microsoft.com/en-us/library/asx0thw2) class in the [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) namespace to obtain that instance of Outlook, and casts that object to an Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

<span data-ttu-id="e3f93-115">Se o Outlook não estiver sendo executado no computador local, o GetApplicationObject criará uma nova instância do Outlook, usará o método [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para entrar no perfil padrão e retornará a nova instância do Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3f93-115">If Outlook is not running on the local computer, GetApplicationObject creates a new instance of Outlook, uses the [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to sign in to the default profile, and returns that new instance of Outlook.</span></span>

<span data-ttu-id="e3f93-116">A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.</span><span class="sxs-lookup"><span data-stu-id="e3f93-116">The following is the Visual Basic code example, followed by the C\# code example.</span></span>

<span data-ttu-id="e3f93-117">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e3f93-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e3f93-118">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="e3f93-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e3f93-119">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="e3f93-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e3f93-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3f93-120">See also</span></span>

- [<span data-ttu-id="e3f93-121">Sessões</span><span class="sxs-lookup"><span data-stu-id="e3f93-121">Sessions</span></span>](sessions.md)

