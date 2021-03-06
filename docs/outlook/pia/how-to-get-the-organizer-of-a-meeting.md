---
title: Obter o organizador de uma reunião
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e19b293b581984e9dbb1fe27c9564cb78a73caa1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542532"
---
# <a name="get-the-organizer-of-a-meeting"></a>Obter o organizador de uma reunião

Este exemplo mostra como retornar via programação o organizador de uma reunião.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo de código a seguir, GetMeetingOrganizer obtém um parâmetro do tipo [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa uma reunião e usa o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) e o método [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) para obter o [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) para o objeto **AppointmentItem**. Uma vez que **EntryID** é obtido, o exemplo usa o método [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)) para retornar o objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) que representa o organizador da reunião.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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
        @"http://schemas.microsoft.com/mapi/proptag/0x00410102";
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

## <a name="see-also"></a>Confira também

- [Solicitações de reunião](meeting-requests.md)

