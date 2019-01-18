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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708134"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a>Escopos adequadamente variáveis em manipuladores de eventos

Um erro comum na programação de manipuladores de evento é conectar o manipulador de eventos em um objeto que foram declarado com um escopo limitado demais para lidar com o evento. O objeto deve ter uma vida que abranja não apenas a função que conecta o método de retorno como um manipulador de eventos do objeto, mas também sobre o método de retorno em que o evento é realmente tratado. Caso contrário, se o objeto estiver fora do escopo definido no método de retorno, o método de retorno não será chamado e o evento não é tratado como desejar.

O exemplo a seguir tenta conectar o método de retorno MyNewInspector para o evento[NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)). No entanto, o método de retorno é conectado no código de exemplo para o evento NewInspector de um objeto[Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\))que tem um escopo limitado a função Connect. Quando o método de retorno é chamado, a função conectar-se já terá sido encerrada, o objeto Inspectors já terá tido o lixo coletado e então MyNewInspector não será chamado.

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

Nesse caso, o correto a se fazer é armazenar o objeto Inspectors em uma variável mais permanente cuja sua vida se estende pela MyClass inteira, incluindo o método de retorno MyNewInspector. No exemplo a seguir MyInspectors tem um escopo de toda a  MyClass e garante que o método de retorno está conectado durante toda a vida útil da classe.

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

Em virtude das diferenças sintáticas por conta dos vários idiomas que conectam manipuladores de eventos, esse problema com idiomas será menos comum no Visual Basic onde você pode se conectar a um evento especificando uma instância do objeto pai e definir o método de retorno ao mesmo tempo. O exemplo a seguir no Visual Basic usa a palavra-chave identificadora para se conectar a região\_expandida do método de retorno para o [evento](https://msdn.microsoft.com/library/bb609515\(v=office.15\))expandido. Uma instância do objeto pai, a região, tem um escopo que ocupa o MyClass incluindo a região\_método de retorno expandido.

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

Neste exemplo, como a região\_método de retorno expandido está conectada ao evento expandido para o tempo de vida da classe, o método de retorno é chamado caso seja apropriado.

## <a name="see-also"></a>Confira também

- [Conectar aos manipuladores de eventos personalizados](connecting-to-custom-event-handlers.md)

