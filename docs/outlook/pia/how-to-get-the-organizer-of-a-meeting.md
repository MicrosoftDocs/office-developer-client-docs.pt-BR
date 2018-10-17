---
title: Obter o organizador de uma reunião
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87d8486b29039f87cb0cbedd2693ce1b4d38b1dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406768"
---
# <a name="get-the-organizer-of-a-meeting"></a><span data-ttu-id="82eb7-102">Obter o organizador de uma reunião</span><span class="sxs-lookup"><span data-stu-id="82eb7-102">Get the organizer of a meeting</span></span>

<span data-ttu-id="82eb7-103">Este exemplo mostra como retornar via programação o organizador de uma reunião.</span><span class="sxs-lookup"><span data-stu-id="82eb7-103">This example shows how to programmatically return the organizer of a meeting.</span></span>

## <a name="example"></a><span data-ttu-id="82eb7-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="82eb7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="82eb7-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="82eb7-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="82eb7-106">No exemplo de código a seguir, GetMeetingOrganizer obtém um parâmetro do tipo [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa uma reunião e usa o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) e o método [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) para obter o [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) para o objeto **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="82eb7-106">In the following code example, GetMeetingOrganizer takes a parameter of type [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) that represents a meeting, and uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method to obtain the [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) for the **AppointmentItem** object.</span></span> <span data-ttu-id="82eb7-107">Uma vez que **EntryID** é obtido, o exemplo usa o método [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) para retornar o objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) que representa o organizador da reunião.</span><span class="sxs-lookup"><span data-stu-id="82eb7-107">Once the **EntryID** is obtained, the example uses the [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) method to return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object that represents the organizer of the meeting.</span></span>

<span data-ttu-id="82eb7-108">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="82eb7-108">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="82eb7-109">A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="82eb7-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="82eb7-110">A seguinte linha de código mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="82eb7-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"https://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="82eb7-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="82eb7-111">See also</span></span>

- [<span data-ttu-id="82eb7-112">Solicitações de reunião</span><span class="sxs-lookup"><span data-stu-id="82eb7-112">Meeting requests</span></span>](meeting-requests.md)

