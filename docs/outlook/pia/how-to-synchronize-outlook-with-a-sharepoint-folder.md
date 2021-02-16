---
title: Sincronizar o Outlook com uma pasta do SharePoint
TOCTitle: Synchronize Outlook with a SharePoint folder
ms:assetid: fecb04ab-39c6-43e1-9a21-12ecb29d94fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424483(v=office.15)
ms:contentKeyID: 55119853
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ab8da62d75b5714967c3fbdc0d0f985370e617aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540634"
---
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a><span data-ttu-id="55bcd-102">Sincronizar o Outlook com uma pasta do SharePoint</span><span class="sxs-lookup"><span data-stu-id="55bcd-102">Synchronize Outlook with a SharePoint folder</span></span>

<span data-ttu-id="55bcd-103">Este exemplo mostra como conectar o Outlook programaticamente com uma pasta do SharePoint e como sincronizar o conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="55bcd-103">This example shows how to programmatically connect Outlook with a SharePoint folder and to synchronize the folder contents.</span></span>

## <a name="example"></a><span data-ttu-id="55bcd-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="55bcd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="55bcd-105">O exemplo de código a seguir é um trecho da [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="55bcd-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="55bcd-106">No Outlook, você pode sincronizar calendários, listas de contatos, listas de tarefas, quadros de discussão e bibliotecas de documentos para pastas do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="55bcd-106">In Outlook, you can synchronize calendars, contact lists, task lists, discussion boards, and document libraries to SharePoint folders.</span></span> <span data-ttu-id="55bcd-107">Com base na URL fornecida após a sincronização, o Outlook criará uma nova pasta do mesmo tipo de base, como pasta do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="55bcd-107">Based on the URL provided upon synchronization, Outlook will create a new folder of the same base type as the SharePoint folder.</span></span> <span data-ttu-id="55bcd-108">Por exemplo, a sincronização de uma pasta de calendário do SharePoint criará uma nova pasta de calendário no Outlook.</span><span class="sxs-lookup"><span data-stu-id="55bcd-108">For example, synchronizing to a SharePoint calendar folder will create a new calendar folder in Outlook.</span></span> <span data-ttu-id="55bcd-109">Pastas de sincronização do SharePoint são armazenadas em sua Pasta Pessoal do Outlook (. pst) fora da caixa de correio do usuário.</span><span class="sxs-lookup"><span data-stu-id="55bcd-109">SharePoint synchronization folders are stored in their own Outlook Personal Folders (.pst) file outside of the user’s mailbox.</span></span> <span data-ttu-id="55bcd-110">Você pode se conectar a uma pasta do SharePoint usando o método[OpenSharedFolder (cadeia de caracteres, objeto, objeto, objeto)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="55bcd-110">You can connect to a SharePoint folder by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="55bcd-111">Observe que você deve usar uma URL stssync: / / que  forneça detalhes sobre o servidor do SharePoint, o caminho da pasta e outras informações que o Outlook precisa para abrir uma pasta do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="55bcd-111">Note that you must use a stssync:// URL that provides details about the SharePoint server, folder path, and other information that Outlook needs to open a SharePoint folder.</span></span>

<span data-ttu-id="55bcd-112">Ao se conectar a uma pasta do SharePoint por programação, você deve determinar a URL adequada a ser usada para criar a relação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="55bcd-112">When connecting to a SharePoint folder programmatically, you must determine the proper URL to use to create the sharing relationship.</span></span> <span data-ttu-id="55bcd-113">Como a URL stssync: / / não é fornecida na interface do usuário do SharePoint para a pasta, conecte manualmente a pasta de destino para o Outlook.</span><span class="sxs-lookup"><span data-stu-id="55bcd-113">Because the stssync:// URL is not provided in the SharePoint user interface for the folder, manually link the destination folder into Outlook.</span></span> <span data-ttu-id="55bcd-114">Então use o primeiro procedimento, DisplaySharePointUrl, no exemplo a seguir, para obter a URL correta.</span><span class="sxs-lookup"><span data-stu-id="55bcd-114">Then use the first procedure, DisplaySharePointUrl, in the following code example, to get the correct URL.</span></span> <span data-ttu-id="55bcd-115">O DisplaySharePointUrl usa o objeto[tabela](https://msdn.microsoft.com/library/bb652856\(v=office.15\))para procurar as informações de associação de compartilhamento na pasta atual para a janela de navegador ativo.</span><span class="sxs-lookup"><span data-stu-id="55bcd-115">DisplaySharePointUrl uses the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to look for the sharing binding information in the current folder for the active explorer window.</span></span> <span data-ttu-id="55bcd-116">Se um ou mais contextos de associação forem encontrados, as URLs de todos os contextos de compartilhamento disponíveis serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="55bcd-116">If one or more binding contexts are found, the URLs for all available sharing contexts will be displayed.</span></span>

<span data-ttu-id="55bcd-117">Agora você tem a URL correta para criar a relação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="55bcd-117">Now you have the proper URL to create the sharing relationship.</span></span> <span data-ttu-id="55bcd-118">Para sincronizar a nova pasta do SharePoint no Outlook, copie e cole a URL para a tarefa a variável de cadeia de caracteres calendarUrl no segundo procedimento AddSpsFolder.</span><span class="sxs-lookup"><span data-stu-id="55bcd-118">To synchronize the new SharePoint folder in Outlook, copy and paste the URL to the assignment of the string variable calendarUrl in the second procedure, AddSpsFolder.</span></span> <span data-ttu-id="55bcd-119">O AddSpsFolder automatiza a sincronização da nova pasta do SharePoint no Outlook usando o método **NameSpace.OpenSharedFolder** com uma`stssync://` URL (nesse caso, a URL produzida pela procedimento DisplaySharePointUrl) .</span><span class="sxs-lookup"><span data-stu-id="55bcd-119">AddSpsFolder automates the synchronization of the new SharePoint folder in Outlook by using the **NameSpace.OpenSharedFolder** method with a `stssync://` URL (in this case, the URL produced by the DisplaySharePointUrl procedure).</span></span> <span data-ttu-id="55bcd-120">O AddSpsFolderalso fornece um nome de pasta personalizada  "Exemplo SPS calendário" e especifica o Outlook para usar o tempo de vida padrão (TTL) da pasta.</span><span class="sxs-lookup"><span data-stu-id="55bcd-120">AddSpsFolderalso provides a custom folder name, “Example SPS Calendar”, and specifies Outlook to use the default Time to Live (TTL) for the folder.</span></span> <span data-ttu-id="55bcd-121">As pastas do SharePoint sempre fazem download de anexos, assim você não precisa especificar isso nela.</span><span class="sxs-lookup"><span data-stu-id="55bcd-121">SharePoint folders always download item attachments, so you do not have to specify that here.</span></span>

<span data-ttu-id="55bcd-122">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="55bcd-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="55bcd-123">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="55bcd-123">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="55bcd-124">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="55bcd-124">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySharePointUrl()
{
    const string PROP_SYNC_URL = 
        "http://schemas.microsoft.com/mapi/id/{00062040-0000-0000-C000-000000000046}/8A24001E";

    Outlook.Folder folder = Application.ActiveExplorer().CurrentFolder as Outlook.Folder;
    Outlook.Table table = folder.GetTable(Type.Missing, Outlook.OlTableContents.olHiddenItems);
    table.Columns.RemoveAll();
    table.Columns.Add("MessageClass");
    table.Columns.Add(PROP_SYNC_URL);

    StringBuilder sb = new StringBuilder();
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        string msgClass, spsUrl;
        msgClass = row["MessageClass"] as string;
        spsUrl = row[PROP_SYNC_URL] as string;

        if (msgClass == "IPM.Sharing.Binding.In")
        {
            sb.Append(spsUrl);
            sb.Append("\r\n");
        }
    }
    if (sb.Length > 0)
    {
        System.Windows.Forms.MessageBox.Show(
            "The following SharePoint Folder URLs were found:\r\n" + sb.ToString());
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("No SharePoint URLs were found in this folder.");
    }
}

private void AddSpsFolder()
{
    string calendarUrl = "stssync://sts/?ver=1.1&type=calendar&cmd=add-folder&base-url=
        https://example.org/calendar&list-url=/Lists/Calendar/calendar.aspx&guid=&site-name=
        Example%20Site&list-name=Calendar";
    string folderName = "Example SPS Calendar";
    bool useDefaultTTL = true;
    Outlook.Folder calendarFolder =
        Application.Session.OpenSharedFolder(calendarUrl, folderName, Type.Missing, useDefaultTTL) 
        as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(calendarFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="55bcd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="55bcd-125">See also</span></span>

- [<span data-ttu-id="55bcd-126">Compartilhamento de grupo</span><span class="sxs-lookup"><span data-stu-id="55bcd-126">Group sharing</span></span>](group-sharing.md)

