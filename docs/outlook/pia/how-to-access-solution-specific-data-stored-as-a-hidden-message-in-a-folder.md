---
title: Acessar dados específicos da solução armazenados como uma mensagem oculta em uma pasta
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c64caf831f79ab61e5e3e0b9d712a511a7ba4f31
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537945"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a><span data-ttu-id="be73c-102">Acessar dados específicos da solução armazenados como uma mensagem oculta em uma pasta</span><span class="sxs-lookup"><span data-stu-id="be73c-102">Access solution-specific data stored as a hidden message in a folder</span></span>

<span data-ttu-id="be73c-103">Este exemplo mostra como usar o objeto [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) para recuperar dados que são armazenados como uma mensagem oculta de uma classe de mensagem específica em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="be73c-103">This example shows how to use the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="be73c-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="be73c-104">Example</span></span>

<span data-ttu-id="be73c-105">O objeto **StorageItem** geralmente é usado para ocultar dados específicos da solução que não podem ser exibidos programaticamente.</span><span class="sxs-lookup"><span data-stu-id="be73c-105">The **StorageItem** object is typically used to hide solution-specific data that cannot be displayed programmatically.</span></span> <span data-ttu-id="be73c-106">Em um ambiente do Exchange, o objeto **StorageItem** é usado para fazer roaming de configurações da solução e garantir que essas configurações estejam disponíveis online e offline.</span><span class="sxs-lookup"><span data-stu-id="be73c-106">In an Exchange environment, the **StorageItem** object is used to roam solution settings and ensure that these settings are available online and offline.</span></span> <span data-ttu-id="be73c-107">Você pode atribuir uma classe de mensagem personalizada ao objeto **StorageItem** ou identificar o objeto por assunto.</span><span class="sxs-lookup"><span data-stu-id="be73c-107">You can assign a custom message class to the **StorageItem** object, or identify the object by subject.</span></span>

<span data-ttu-id="be73c-108">O exemplo de código a seguir recupera os dados XML que estão armazenados como uma mensagem oculta na pasta Calendário com a classe de mensagens igual a IPM.Configuration.WorkHours.</span><span class="sxs-lookup"><span data-stu-id="be73c-108">The following code sample retrieves the XML data that is stored as a hidden message in the Calendar folder with the message class equal to IPM.Configuration.WorkHours.</span></span>

<span data-ttu-id="be73c-109">O objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) retorna o XML como um objeto que contém um fluxo de bytes em vez de uma representação de string do XML.</span><span class="sxs-lookup"><span data-stu-id="be73c-109">The [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object returns the XML as an object that contains a byte stream rather than a string representation of the XML.</span></span> <span data-ttu-id="be73c-110">O exemplo de código usa **System.Text.Encoding.Ascii.GetString** para converter o fluxo de bytes em uma sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="be73c-110">The code sample uses **System.Text.Encoding.Ascii.GetString** to convert the byte stream to a string.</span></span>

<span data-ttu-id="be73c-111">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="be73c-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="be73c-112">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="be73c-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="be73c-113">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="be73c-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Function GetWorkHoursXML() As String
    Try
        Dim storage As Outlook.StorageItem = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage( _
            "IPM.Configuration.WorkHours", _
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass)
        Dim pa As Outlook.PropertyAccessor = storage.PropertyAccessor
        ' PropertyAccessor will return a byte array for this property
        Dim rawXmlBytes As Byte() = CType(pa.GetProperty( _
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102"), _
            Byte())
        ' Use Encoding to convert the array to a string
        Return System.Text.Encoding.ASCII.GetString(rawXmlBytes)
    Catch
        Return String.Empty
    End Try
End Function
```

```csharp
private string GetWorkHoursXML()
{
    try
    {
        Outlook.StorageItem storage =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage(
            "IPM.Configuration.WorkHours",
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass);
        Outlook.PropertyAccessor pa = storage.PropertyAccessor;
        // PropertyAccessor will return a byte array for this property
        byte[] rawXmlBytes = (byte[])pa.GetProperty(
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102");
        // Use Encoding to convert the array to a string
        return System.Text.Encoding.ASCII.GetString(rawXmlBytes);
    }
    catch
    {
        return string.Empty;
    }
}
```


## <a name="see-also"></a><span data-ttu-id="be73c-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="be73c-114">See also</span></span>

- [<span data-ttu-id="be73c-115">Pastas</span><span class="sxs-lookup"><span data-stu-id="be73c-115">Folders</span></span>](folders.md)

