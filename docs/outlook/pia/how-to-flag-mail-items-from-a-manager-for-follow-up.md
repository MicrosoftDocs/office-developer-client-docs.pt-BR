---
title: Sinalizar itens de email de um gerente para acompanhamento
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 73c4a7ec8118b95edac06ae8ab5bc59902612ebc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406362"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a><span data-ttu-id="7f6b4-102">Sinalizar itens de email de um gerente para acompanhamento</span><span class="sxs-lookup"><span data-stu-id="7f6b4-102">Flag mail items from a manager for follow-up</span></span>

<span data-ttu-id="7f6b4-103">Este exemplo mostra como sinalizar para acompanhamento itens de email que foram recebidos do gerente do usuário.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-103">This example shows how to flag email items that were received from the user’s manager for follow-up.</span></span>

## <a name="example"></a><span data-ttu-id="7f6b4-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7f6b4-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7f6b4-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="7f6b4-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="7f6b4-106">O Microsoft Outlook fornece um sistema de sinalização de tarefas em que determinados itens do Outlook, como itens de email ou itens de contatos, podem ser sinalizados para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-106">Microsoft Outlook provides a task flagging system in which certain Outlook items such as mail items or contact items can be flagged for follow-up.</span></span> <span data-ttu-id="7f6b4-107">Quando você sinaliza um item do Outlook para acompanhamento, informações sobre esse item do Outlook, além de outras informações com base em tarefas, são exibidas na **Barra de Tarefas Pendentes** e no módulo de navegação de Calendário na interface de usuário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-107">When you flag an Outlook item for follow-up, information about that Outlook item, along with other task-based information, is displayed on the **To-Do Bar** and Calendar navigation module in the Outlook user interface.</span></span> <span data-ttu-id="7f6b4-108">A **Barra de Tarefas Pendentes** é exibida como um painel vertical em uma configuração comum da janela do explorador do Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-108">The **To-Do Bar** is displayed as a vertical pane in a typical configuration of the Outlook explorer window.</span></span> <span data-ttu-id="7f6b4-109">Ela contém um controle do navegador de datas, compromissos futuros e itens que foram sinalizados para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-109">It contains a date navigator control, upcoming appointments, and items that have been flagged for follow-up.</span></span> <span data-ttu-id="7f6b4-110">A **Barra de Tarefas Pendentes** em si não é expansível, e você pode só definir opções de configuração para a **Barra de Tarefas Pendentes** por meio da interface de usuário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-110">The **To-Do Bar** itself is not extensible, and you can set configuration options for the **To-Do Bar** only through the Outlook user interface.</span></span> <span data-ttu-id="7f6b4-111">Sinalizar itens permite organizar e priorizar tarefas e itens pendentes.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-111">Flagging items allows to you organize and prioritize tasks and to-do items.</span></span>

<span data-ttu-id="7f6b4-112">O exemplo a seguir marcas de um grupo de itens para um intervalo de acompanhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-112">The following code example marks a group of items for a specified follow-up interval.</span></span> <span data-ttu-id="7f6b4-113">O exemplo coloca todos os itens na Caixa de Entrada do usuário que sejam do gerente do usuário atual usando uma consulta DAV de Pesquisa e Localização (DASL) para filtrar mensagens do tipo "IPM.NOTE" com o nome do gerente como remetente.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-113">The example gets all items in the current user’s Inbox that are from the current user’s manager by using a DAV Searching and Locating (DASL) query to filter for messages of type “IPM.NOTE” with the manager’s name as the sender.</span></span> <span data-ttu-id="7f6b4-114">Ele marca, em seguida, todos os itens de acordo com o valor [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) da propriedade [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7f6b4-114">It then flags all items according to the [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) value of the [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) property.</span></span> <span data-ttu-id="7f6b4-115">Todos os itens de alta prioridade estão sinalizados para acompanhamento hoje e todos os itens de importância normal estão sinalizados para acompanhamento esta semana, usando o método [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7f6b4-115">All high-importance items are flagged for follow-up today and all normal-importance items are flagged for follow-up this week by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>


> [!NOTE]
> <span data-ttu-id="7f6b4-116">A propriedade **Importance** e o método **MarkAsTask** são membros de objeto **Item**.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-116">The **Importance** property and the **MarkAsTask** method are **Item** object members.</span></span>


<span data-ttu-id="7f6b4-117">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-117">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="7f6b4-118">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7f6b4-119">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "https://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager;
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            string filter = "@SQL=" + "\""
                + PR_SENT_REPRESENTING_NAME + "\""
                + " = '" + displayName + "'" + " AND " + "\""
                + PR_MESSAGE_CLASS + "\"" + " = 'IPM.NOTE'";
            Outlook.Items items =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).
                Items.Restrict(filter);
            foreach (Outlook.MailItem mail in items)
            {
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceHigh)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkToday);
                    mail.Save();
                }
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceNormal)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkThisWeek);
                    mail.Save();
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7f6b4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f6b4-120">See also</span></span>

- [<span data-ttu-id="7f6b4-121">Tarefas</span><span class="sxs-lookup"><span data-stu-id="7f6b4-121">Tasks</span></span>](tasks.md)

