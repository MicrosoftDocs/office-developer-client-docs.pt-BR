---
title: Implementar um invólucro para inspetores e rastrear eventos em nível de item em cada inspetor
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d5fee97e27b616232f2f45eb42faf659eee52cda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405767"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a><span data-ttu-id="6c94f-102">Implementar um invólucro para inspetores e rastrear eventos em nível de item em cada inspetor</span><span class="sxs-lookup"><span data-stu-id="6c94f-102">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>

<span data-ttu-id="6c94f-103">Este tópico contém dois exemplos de código que mostram como implementar um invólucro para uma coleção [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) e como usar esse invólucro para rastrear eventos em nível de item em cada objeto [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) na coleção.</span><span class="sxs-lookup"><span data-stu-id="6c94f-103">This topic contains two code examples that show how to implement a wrapper for an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) collection and to use that wrapper to track item-level events in each [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) object in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="6c94f-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6c94f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6c94f-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6c94f-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="6c94f-106">Os dois exemplos de código a seguir implementam as classes Connect e OutlookInspector.</span><span class="sxs-lookup"><span data-stu-id="6c94f-106">The following two code examples implement the Connect and OutlookInspector classes.</span></span> <span data-ttu-id="6c94f-107">O primeiro exemplo de código envolve métodos e manipuladores de eventos que você inclui na classe Connect para implementar um invólucro de uma colação **Inspectors**.</span><span class="sxs-lookup"><span data-stu-id="6c94f-107">The first code example involves methods and event handlers you include in the Connect class to implement a wrapper for an **Inspectors** collection.</span></span> <span data-ttu-id="6c94f-108">O segundo exemplo de código envolve uma implementação simples da classe **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="6c94f-108">The second code example involves a simple implementation of the **OutlookInspector** class.</span></span>

<span data-ttu-id="6c94f-109">Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6c94f-109">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="6c94f-110">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="6c94f-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6c94f-111">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="6c94f-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="6c94f-112">No seguinte exemplo de código, um evento [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) ocorre depois que uma nova janela de inspetor foi criada e antes de ela ser exibida.</span><span class="sxs-lookup"><span data-stu-id="6c94f-112">In the following code example, a [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) event occurs after a new inspector window has been created and before it is displayed.</span></span> <span data-ttu-id="6c94f-113">Uma ação do usuário também pode criar uma nova janela de inspetor.</span><span class="sxs-lookup"><span data-stu-id="6c94f-113">A user action may also create a new inspector window.</span></span> <span data-ttu-id="6c94f-114">É declarada uma variável de instância em nível de classe chamada inspetores na classe **Connect**, e um evento **NewInspector** é conectado.</span><span class="sxs-lookup"><span data-stu-id="6c94f-114">A class-level instance variable named inspectors in the **Connect** class is declared, and a **NewInspector** event is hooked up.</span></span> 

<span data-ttu-id="6c94f-115">No método \_NewInspector de inspetores, o método **FindOutlookInspector** verifica se a nova janela de inspetor já está na lista inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="6c94f-115">In the inspectors\_NewInspector method, the **FindOutlookInspector** method checks whether the new inspector window is already in the inspectorWindows list.</span></span> <span data-ttu-id="6c94f-116">Se FindOutlookInspector não encontrar o objeto **Inspector** em inspectorWindows, o método **AddInspector** adiciona uma instância da classe **OutlookInspector** a inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="6c94f-116">If FindOutlookInspector does not find the **Inspector** object in inspectorWindows, the **AddInspector** method adds an instance of the **OutlookInspector** class to inspectorWindows.</span></span> <span data-ttu-id="6c94f-117">Você pode usar a classe **OutlookInspector** para elevar os eventos para esta janela de inspetor específica.</span><span class="sxs-lookup"><span data-stu-id="6c94f-117">You can use the **OutlookInspector** class to raise events for this particular inspector window.</span></span> <span data-ttu-id="6c94f-118">A implementação da classe **OutlookInspector** é exibida no segundo exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="6c94f-118">The implementation of the **OutlookInspector** class is shown in the second code example.</span></span>

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

<span data-ttu-id="6c94f-119">O seguinte exemplo de código envolve uma implementação da classe **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="6c94f-119">The following code example is an implementation of the **OutlookInspector** class.</span></span> <span data-ttu-id="6c94f-120">Esta classe é usada para elevar eventos para a janela do Inspetor a partir do exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="6c94f-120">This class is used to raise events for the inspector window from the preceding code example.</span></span> <span data-ttu-id="6c94f-121">Várias janelas de inspetor podem ser abertas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6c94f-121">Multiple inspector windows can be open simultaneously.</span></span> <span data-ttu-id="6c94f-122">Eventos em nível de item, como [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) e [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) são rastreados através de sua conexão neste construtor de classe.</span><span class="sxs-lookup"><span data-stu-id="6c94f-122">Item-level events such as [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)), and [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) are tracked by hooking them up in this class constructor.</span></span> <span data-ttu-id="6c94f-123">Um evento [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) para um objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) também é conectado neste construtor de classe.</span><span class="sxs-lookup"><span data-stu-id="6c94f-123">A [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) event for a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is also hooked up in this class constructor.</span></span> <span data-ttu-id="6c94f-124">Você pode definir outras variáveis de instância de item em nível de classe, se necessário.</span><span class="sxs-lookup"><span data-stu-id="6c94f-124">You can define other class-level item instance variables as needed.</span></span> <span data-ttu-id="6c94f-125">Todos os eventos conectados no construtor OutlookInspector estão desconectados no manipulador de eventos OutlookInspectorWindow\_Close.</span><span class="sxs-lookup"><span data-stu-id="6c94f-125">All the events that were hooked up in the OutlookInspector constructor are unhooked in the OutlookInspectorWindow\_Close event handler.</span></span>

<span data-ttu-id="6c94f-126">Observe que, no nível de modelo de objeto, um objeto **inspetor do Outlook** não é específico para nenhum tipo de item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6c94f-126">Note that at the object model level, an **Outlook inspector** object is not specific to any Outlook item type.</span></span> <span data-ttu-id="6c94f-127">Esta amostra de código faz uso da classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente a propriedade OutlookItem.Class para verificar a classe de mensagem do item atual no inspetor, antes de definir o item como um item de contato.</span><span class="sxs-lookup"><span data-stu-id="6c94f-127">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of the current item in the inspector, before assuming the item is a contact item.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6c94f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c94f-128">See also</span></span>

- [<span data-ttu-id="6c94f-129">Amostras de tarefas usando eventos do Outlook</span><span class="sxs-lookup"><span data-stu-id="6c94f-129">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

