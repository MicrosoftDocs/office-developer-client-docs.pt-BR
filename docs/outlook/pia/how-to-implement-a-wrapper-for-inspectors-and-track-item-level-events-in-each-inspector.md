---
title: Implementar um invólucro para inspetores e rastrear eventos em nível de item em cada inspetor
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8454c1e969fbccc80f5cb0341b6b55815132ade1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698670"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a>Implementar um invólucro para inspetores e rastrear eventos em nível de item em cada inspetor

Este tópico contém dois exemplos de código que mostram como implementar um invólucro para uma coleção [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) e como usar esse invólucro para rastrear eventos em nível de item em cada objeto [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) na coleção.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Os dois exemplos de código a seguir implementam as classes Connect e OutlookInspector. O primeiro exemplo de código envolve métodos e manipuladores de eventos que você inclui na classe Connect para implementar um invólucro de uma colação **Inspectors**. O segundo exemplo de código envolve uma implementação simples da classe **OutlookInspector**.

Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

No seguinte exemplo de código, um evento [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) ocorre depois que uma nova janela de inspetor foi criada e antes de ela ser exibida. Uma ação do usuário também pode criar uma nova janela de inspetor. É declarada uma variável de instância em nível de classe chamada inspetores na classe **Connect**, e um evento **NewInspector** é conectado. 

No método \_NewInspector de inspetores, o método **FindOutlookInspector** verifica se a nova janela de inspetor já está na lista inspectorWindows. Se FindOutlookInspector não encontrar o objeto **Inspector** em inspectorWindows, o método **AddInspector** adiciona uma instância da classe **OutlookInspector** a inspectorWindows. Você pode usar a classe **OutlookInspector** para elevar os eventos para esta janela de inspetor específica. A implementação da classe **OutlookInspector** é exibida no segundo exemplo de código.

```csharp
class Connect
{
    // Connect class-level Instance Variables
    // Outlook inspectors collection
    private Outlook.Inspectors inspectors;

    // Collection of tracked inspector windows              
    private List<OutlookInspector> inspectorWindows;    

    // Hook up NewInspector event
    inspectors.NewInspector += new 
        Outlook.InspectorsEvents_NewInspectorEventHandler(
        inspectors_NewInspector);

    // NewInspector event creates new instance of OutlookInspector
    void inspectors_NewInspector(Outlook.Inspector Inspector)
    {
        // Check to see if this is a new window you don't
        // already track
        OutlookInspector existingWindow = 
            FindOutlookInspector(Inspector);
        if (existingWindow == null)
        {
            AddInspector(Inspector);
        }
    }

    // Adds an instance of **OutlookInspector** class
    private void AddInspector(Outlook.Inspector inspector)
    {
        OutlookInspector window = new OutlookInspector(inspector);
        window.Close +=
            new EventHandler(WrappedInspectorWindow_Close);
    }

    // Looks up the window wrapper for a given Inspector 
    // window object
    private OutlookInspector FindOutlookInspector(object window)
    {
        foreach (OutlookInspector inspector in inspectorWindows)
        {
            if (inspector.Window == window)
            {
                return inspector;
            }
        }
        return null;
    }
}
```

O seguinte exemplo de código envolve uma implementação da classe **OutlookInspector**. Esta classe é usada para elevar eventos para a janela do Inspetor a partir do exemplo de código anterior. Várias janelas de inspetor podem ser abertas ao mesmo tempo. Eventos em nível de item, como [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) e [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) são rastreados através de sua conexão neste construtor de classe. Um evento [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) para um objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) também é conectado neste construtor de classe. Você pode definir outras variáveis de instância de item em nível de classe, se necessário. Todos os eventos conectados no construtor OutlookInspector estão desconectados no manipulador de eventos OutlookInspectorWindow\_Close.

Observe que, no nível de modelo de objeto, um objeto **inspetor do Outlook** não é específico para nenhum tipo de item do Outlook. Esta amostra de código faz uso da classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente a propriedade OutlookItem.Class para verificar a classe de mensagem do item atual no inspetor, antes de definir o item como um item de contato.

```csharp
// This class tracks the state of an Outlook Inspector window 
// and ensures that what happens in this window is handled correctly.
class OutlookInspector
{
    // OutlookInspector class-level instance variables 
    // wrapped window object
    private Outlook.Inspector m_Window;             

    // Use these instance variables to handle item-level events
    // wrapped MailItem
    private Outlook.MailItem m_Mail;    
    // wrapped AppointmentItem        
    private Outlook.AppointmentItem m_Appointment;  
    // wrapped ContactItem
    private Outlook.ContactItem m_Contact;
    // wrapped TaskItem      
    private Outlook.ContactItem m_Task;             

    // OutlookInspector constructor
    public OutlookInspector(Outlook.Inspector inspector)
    {
        m_Window = inspector;

        // Hook up the close event
        ((Outlook.InspectorEvents_Event)inspector).Close +=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Hook up item-level events as needed
        OutlookItem olItem = new OutlookItem(inspector.CurrentItem);
        if(olItem.Class==Outlook.OlObjectClass.olContact)
        {
            m_Contact = olItem.InnerObject as Outlook.ContactItem;
            m_Contact.Open +=
                new Outlook.ItemEvents_10_OpenEventHandler(
                m_Contact_Open);
            m_Contact.PropertyChange +=
                new Outlook.ItemEvents_10_PropertyChangeEventHandler(
                m_Contact_PropertyChange);
            m_Contact.CustomPropertyChange +=
                new Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
                m_Contact_CustomPropertyChange);
        }
    }

    // Event Handler for the inspector close event.
    private void OutlookInspectorWindow_Close()
    {
        // Unhook events from any item-level instance variables
        m_Contact.Open -= 
            Outlook.ItemEvents_10_OpenEventHandler(
            m_Contact_Open);
        m_Contact.PropertyChange -= 
            Outlook.ItemEvents_10_PropertyChangeEventHandler(
            m_Contact_PropertyChange);
        m_Contact.CustomPropertyChange -= 
            Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
            m_Contact_CustomPropertyChange);
        ((Outlook.ItemEvents_Event)m_Contact).Close -= 
            Outlook.ItemEvents_CloseEventHandler(
            m_Contact_Close);

        // Unhook events from the window
        ((Outlook.InspectorEvents_Event)m_Window).Close -=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Raise the OutlookInspector close event
        if (Close != null)
        {
            Close(this, EventArgs.Empty);
        }
        // Release item-level instance variables
        m_Mail = null;
        m_Appointment = null;
        m_Contact = null;
        m_Task = null;
        m_Window = null;
    }
}
```

## <a name="see-also"></a>Confira também

- [Amostras de tarefas usando eventos do Outlook](sample-tasks-using-outlook-events.md)

