---
title: Escopos adequadamente variáveis em manipuladores de eventos
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8a1a418a315167cc96be5b9b5f65a0f4cd9ce44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342249"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a><span data-ttu-id="3fad6-102">Escopos adequadamente variáveis em manipuladores de eventos</span><span class="sxs-lookup"><span data-stu-id="3fad6-102">Scoping variables appropriately in event handlers</span></span>

<span data-ttu-id="3fad6-103">Um erro comum na programação de manipuladores de evento é conectar o manipulador de eventos em um objeto que foram declarado com um escopo limitado demais para lidar com o evento.</span><span class="sxs-lookup"><span data-stu-id="3fad6-103">A common mistake in programming event handlers is connecting the event handler to an object that has been declared with a scope too limited for the purpose of handling the event.</span></span> <span data-ttu-id="3fad6-104">O objeto deve ter uma vida que abranja não apenas a função que conecta o método de retorno como um manipulador de eventos do objeto, mas também sobre o método de retorno em que o evento é realmente tratado.</span><span class="sxs-lookup"><span data-stu-id="3fad6-104">The object must have a life that spans not just over the function that connects the callback method as an event handler of the object, but also over the callback method itself where the event is actually handled.</span></span> <span data-ttu-id="3fad6-105">Caso contrário, se o objeto estiver fora do escopo definido no método de retorno, o método de retorno não será chamado e o evento não é tratado como desejar.</span><span class="sxs-lookup"><span data-stu-id="3fad6-105">Otherwise, if the object is out of scope and is no longer defined in the callback method, the callback method is not called and the event is not handled as desired.</span></span>

<span data-ttu-id="3fad6-106">O exemplo a seguir tenta conectar o método de retorno MyNewInspector para o evento[NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3fad6-106">The following example attempts to connect the MyNewInspector callback method to the [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) event.</span></span> <span data-ttu-id="3fad6-107">No entanto, o método de retorno é conectado no código de exemplo para o evento NewInspector de um objeto[Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\))que tem um escopo limitado a função Connect.</span><span class="sxs-lookup"><span data-stu-id="3fad6-107">However, the callback method is hooked up in the code sample to the NewInspector event of an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) object that has a scope limited to the Connect function.</span></span> <span data-ttu-id="3fad6-108">Quando o método de retorno é chamado, a função conectar-se já terá sido encerrada, o objeto Inspectors já terá tido o lixo coletado e então MyNewInspector não será chamado.</span><span class="sxs-lookup"><span data-stu-id="3fad6-108">When the callback method is eventually called, the Connect function has already exited, the Inspectors object has already been garbage collected, and so MyNewInspector is never called.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyApp.Inspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

<span data-ttu-id="3fad6-109">Nesse caso, o correto a se fazer é armazenar o objeto Inspectors em uma variável mais permanente cuja sua vida se estende pela MyClass inteira, incluindo o método de retorno MyNewInspector.</span><span class="sxs-lookup"><span data-stu-id="3fad6-109">The correct thing to do in this case is to store the Inspectors object in a more permanent variable whose lifetime spans over the entire MyClass, including the MyNewInspector callback method.</span></span> <span data-ttu-id="3fad6-110">No exemplo a seguir MyInspectors tem um escopo de toda a  MyClass e garante que o método de retorno está conectado durante toda a vida útil da classe.</span><span class="sxs-lookup"><span data-stu-id="3fad6-110">In the following example, MyInspectors has a scope of the entire MyClass and ensures that the callback method is connected for the lifetime of the class.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;
    private Outlook.Inspectors MyInspectors;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyInspectors = MyApp.Inspectors;
        MyInspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

<span data-ttu-id="3fad6-111">Em virtude das diferenças sintáticas por conta dos vários idiomas que conectam manipuladores de eventos, esse problema com idiomas será menos comum no Visual Basic onde você pode se conectar a um evento especificando uma instância do objeto pai e definir o método de retorno ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3fad6-111">By virtue of the syntactic differences in how various languages connect event handlers, this issue is less common in languages such as Visual Basic where you can connect an event specifying an instance of the parent object, and define the callback method at the same time.</span></span> <span data-ttu-id="3fad6-112">O exemplo a seguir no Visual Basic usa a palavra-chave identificadora para se conectar a região\_expandida do método de retorno para o [evento](https://msdn.microsoft.com/library/bb609515\(v=office.15\))expandido.</span><span class="sxs-lookup"><span data-stu-id="3fad6-112">The following example in Visual Basic uses the Handles keyword to connect the Region\_Expanded callback method to the [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) event.</span></span> <span data-ttu-id="3fad6-113">Uma instância do objeto pai, a região, tem um escopo que ocupa o MyClass incluindo a região\_método de retorno expandido.</span><span class="sxs-lookup"><span data-stu-id="3fad6-113">An instance of the parent object, Region, has a scope that spans MyClass including the Region\_Expanded callback method.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Public Class MyClass
    ' The Region object has a lifetime spanning the class 
    ' including the callback method Region_Expanded
    Private WithEvents Region As Outlook.FormRegion
    ...
    Private Sub Region_Expanded() Handles Region.Expanded
        MsgBox("My EventHandler caught an Expanded event.")
    End Sub
End Class
```

<span data-ttu-id="3fad6-114">Neste exemplo, como a região\_método de retorno expandido está conectada ao evento expandido para o tempo de vida da classe, o método de retorno é chamado caso seja apropriado.</span><span class="sxs-lookup"><span data-stu-id="3fad6-114">In this example, because the Region\_Expanded callback method is connected to the Expanded event for the lifetime of the class, the callback method is called as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fad6-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fad6-115">See also</span></span>

- [<span data-ttu-id="3fad6-116">Conectar aos manipuladores de eventos personalizados</span><span class="sxs-lookup"><span data-stu-id="3fad6-116">Connecting to custom event handlers</span></span>](connecting-to-custom-event-handlers.md)

