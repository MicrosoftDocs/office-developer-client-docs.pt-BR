---
title: Assinar um RSS feed
TOCTitle: Subscribe to an RSS feed
ms:assetid: 7ecefbcd-1a34-48e8-afac-7d54e79fd159
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424473(v=office.15)
ms:contentKeyID: 55119852
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b92c733c5030ce12eb691bba57afb5ce6b9d1dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335396"
---
# <a name="subscribe-to-an-rss-feed"></a><span data-ttu-id="d8c99-102">Assinar um RSS feed</span><span class="sxs-lookup"><span data-stu-id="d8c99-102">Subscribe to an RSS feed</span></span>

<span data-ttu-id="d8c99-103">Este exemplo mostra como assinar um RSS feed usando o método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d8c99-103">This example shows how to subscribe to an RSS feed by using the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="d8c99-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d8c99-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d8c99-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d8c99-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d8c99-106">O modelo de objeto do Outlook oferece suporte ao fornecimento de acesso a dados compartilhados, como calendários da Internet, RSS feeds e dados de listas e bibliotecas de documentos do Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d8c99-106">The Outlook object model supports providing access to shared data, such as Internet calendars, RSS feeds, and data from Microsoft SharePoint lists and document libraries.</span></span> <span data-ttu-id="d8c99-107">Ele permite conectar a essas fontes de dados e configurar os contextos de sincronização para continuar a sondar esses recursos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="d8c99-107">It enables connecting to these shared sources of data and setting up the synchronization contexts to continue to poll those shared resources.</span></span> <span data-ttu-id="d8c99-108">O modelo de objeto do Outlook fornece o método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para baixar e sincronizar com um determinado tipo de pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="d8c99-108">The Outlook object model provides the [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to download and synchronize with a particular type of shared folder.</span></span>

<span data-ttu-id="d8c99-109">No exemplo a seguir, AddRssFeed se inscreve em um novo RSS feed chamado "RSS Feed de Exemplo" chamando o método **OpenSharedFolder** com uma URL que faz referência ao novo RSS feed.</span><span class="sxs-lookup"><span data-stu-id="d8c99-109">In the following example, AddRssFeed subscribes to a new RSS feed named “Example RSS Feed” by calling the **OpenSharedFolder** method with a URL that refers to the new RSS feed.</span></span> <span data-ttu-id="d8c99-110">Os dois últimos parâmetros de **OpenSharedFolder** são definidos como **true** para indicar que anexos devem ser baixados, e que o Outlook deve usar a taxa de atualização fornecida no RSS feed.</span><span class="sxs-lookup"><span data-stu-id="d8c99-110">The last two parameters of **OpenSharedFolder** method are set to **true** to indicate that attachments should be downloaded, and Outlook should use the refresh ratio provided in the RSS feed.</span></span>


> [!NOTE]
> <span data-ttu-id="d8c99-111">Você deve especificar o identificador de protocolo correto para a URL da pasta no método **OpenSharedFolder** para assinar um RSS feed.</span><span class="sxs-lookup"><span data-stu-id="d8c99-111">You must specify the correct protocol handler for the folder URL in the **OpenSharedFolder** method to subscribe to an RSS feed.</span></span> <span data-ttu-id="d8c99-112">Por exemplo, você deve usar uma URL que comece com `feed://` em vez de `https://`.</span><span class="sxs-lookup"><span data-stu-id="d8c99-112">For example, you must use a URL that begins with `feed://` instead of `https://`.</span></span> <span data-ttu-id="d8c99-113">O Outlook não consegue abrir RSS feeds que exijam autenticação, a menos que a autenticação Windows NT LAN Manager (LAN) esteja disponível e não possa carregar RSS feeds de locais de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="d8c99-113">Outlook cannot open RSS feeds that require authentication unless Windows NT LAN Manager (NTLM) authentication is available, and it cannot load RSS feeds from Secure Sockets Layer (SSL) locations.</span></span>

<span data-ttu-id="d8c99-114">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d8c99-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d8c99-115">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="d8c99-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d8c99-116">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="d8c99-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AddRssFeed()
{
    string feedUrl = "feed://example.org/rssfeed.xml";
    Outlook.Folder subscriptionFolder =
        Application.Session.OpenSharedFolder(feedUrl, "Example RSS Feed", true, true) as Outlook.Folder;
    Outlook.Explorer exp =
        Application.Explorers.Add(subscriptionFolder, Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
    exp.Display();
}
```

## <a name="see-also"></a><span data-ttu-id="d8c99-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8c99-117">See also</span></span>

- [<span data-ttu-id="d8c99-118">Compartilhamento de grupo</span><span class="sxs-lookup"><span data-stu-id="d8c99-118">Group sharing</span></span>](group-sharing.md)

