---
title: Exibir um calendário compartilhado de um destinatário
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9230a63af66e8143a7da488ce41dadafe359429
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709212"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a><span data-ttu-id="ba710-102">Exibir um calendário compartilhado de um destinatário</span><span class="sxs-lookup"><span data-stu-id="ba710-102">Display a shared calendar of a recipient</span></span>

<span data-ttu-id="ba710-103">Este exemplo mostra como exibir o calendário compartilhado de um destinatário usando os métodos [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) e [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ba710-103">This example shows how to display a recipient's shared calendar by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) and [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) methods.</span></span>

## <a name="example"></a><span data-ttu-id="ba710-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ba710-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ba710-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="ba710-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ba710-106">Itens enviáveis, como objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)), sempre expõem a propriedade [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) que, por sua vez, permite acessar o conjunto [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) do item enviável.</span><span class="sxs-lookup"><span data-stu-id="ba710-106">Sendable items such as [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects always expose the [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) property which, in turn, enables you to access the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the sendable item.</span></span> <span data-ttu-id="ba710-107">Para criar um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) que não está associado ao conjunto **Recipients** de um item, use o método [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ba710-107">To create a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object that is not bound to the **Recipients** collection of an item, use the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="ba710-108">Em seguida, passe este objeto **Recipient** não associado para o método [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)), que retorna uma pasta compartilhada do Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba710-108">Then pass this unbound **Recipient** object to the [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) method, which returns a shared Exchange folder.</span></span> <span data-ttu-id="ba710-109">Você pode então abrir a pasta compartilhada do Exchange e exibir essa pasta em uma janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="ba710-109">You can then open the shared Exchange folder and display that folder in an explorer window.</span></span> <span data-ttu-id="ba710-110">GetSharedDefaultFolder é usado nos cenários de representante do Exchange, onde o representante tem permissão para acessara pasta do delegante.</span><span class="sxs-lookup"><span data-stu-id="ba710-110">GetSharedDefaultFolder is used in Exchange delegate scenarios where the delegate has permission to access the folder of the delegator.</span></span> <span data-ttu-id="ba710-111">Antes de passar o objeto **Recipient** para o método GetSharedDefaultFolder, você deve resolvê-lo.</span><span class="sxs-lookup"><span data-stu-id="ba710-111">Before you pass the **Recipient** object to the GetSharedDefaultFolder method, you must resolve it.</span></span> <span data-ttu-id="ba710-112">Para resolver um objeto **Recipient**, ligue para seu método [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ba710-112">To resolve a **Recipient** object, call its [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) method.</span></span>

<span data-ttu-id="ba710-113">No exemplo código a seguir, DisplayManagerCalendar abre e exibe a pasta Calendário do gerente do usuário atual chamando **CreateRecipient** e **GetSharedDefaultFolder**.</span><span class="sxs-lookup"><span data-stu-id="ba710-113">In the following code example, DisplayManagerCalendar opens and displays the Calendar folder of the current user’s manager by calling **CreateRecipient** and **GetSharedDefaultFolder**.</span></span> <span data-ttu-id="ba710-114">Uma caixa de diálogo de alerta é exibida se o usuário não tiver permissão para abrir a pasta Calendário do gerenciador ou se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="ba710-114">An alert dialog box is displayed if the user does not have permission to open the manager’s Calendar folder or an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="ba710-115">Quando você cria um objeto **Recipient** usando o método **CreateRecipient** do objeto **Namespace** ou o método [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) do conjunto **Recipients**, você deve fornecer um nome de destinatário.</span><span class="sxs-lookup"><span data-stu-id="ba710-115">When you create a **Recipient** object by using the **CreateRecipient** method of the **Namespace** object or the [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) method of the **Recipients** collection, you must provide a recipient name.</span></span> <span data-ttu-id="ba710-116">O **Recipient** é resolvido em relação a esse nome.</span><span class="sxs-lookup"><span data-stu-id="ba710-116">The **Recipient** is then resolved against this name.</span></span> <span data-ttu-id="ba710-117">Um nome de destinatário pode ter qualquer um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="ba710-117">A recipient name can take any of the following formats:</span></span>
> - <span data-ttu-id="ba710-118">Nome para exibição</span><span class="sxs-lookup"><span data-stu-id="ba710-118">Display name</span></span>
> - <span data-ttu-id="ba710-119">Alias</span><span class="sxs-lookup"><span data-stu-id="ba710-119">Alias</span></span>
> - <span data-ttu-id="ba710-120">Endereço SMTP</span><span class="sxs-lookup"><span data-stu-id="ba710-120">Simple Mail Transfer Protocol (SMTP) address</span></span>

<span data-ttu-id="ba710-121">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ba710-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ba710-122">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="ba710-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ba710-123">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="ba710-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="ba710-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba710-124">See also</span></span>

- [<span data-ttu-id="ba710-125">Calendar</span><span class="sxs-lookup"><span data-stu-id="ba710-125">Calendar</span></span>](calendar.md)

