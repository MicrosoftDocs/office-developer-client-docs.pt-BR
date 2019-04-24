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
# <a name="subscribe-to-an-rss-feed"></a>Assinar um RSS feed

Este exemplo mostra como assinar um RSS feed usando o método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O modelo de objeto do Outlook oferece suporte ao fornecimento de acesso a dados compartilhados, como calendários da Internet, RSS feeds e dados de listas e bibliotecas de documentos do Microsoft SharePoint. Ele permite conectar a essas fontes de dados e configurar os contextos de sincronização para continuar a sondar esses recursos compartilhados. O modelo de objeto do Outlook fornece o método [OpenSharedFolder(String, Object, Object, Object)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para baixar e sincronizar com um determinado tipo de pasta compartilhada.

No exemplo a seguir, AddRssFeed se inscreve em um novo RSS feed chamado "RSS Feed de Exemplo" chamando o método **OpenSharedFolder** com uma URL que faz referência ao novo RSS feed. Os dois últimos parâmetros de **OpenSharedFolder** são definidos como **true** para indicar que anexos devem ser baixados, e que o Outlook deve usar a taxa de atualização fornecida no RSS feed.


> [!NOTE]
> Você deve especificar o identificador de protocolo correto para a URL da pasta no método **OpenSharedFolder** para assinar um RSS feed. Por exemplo, você deve usar uma URL que comece com `feed://` em vez de `https://`. O Outlook não consegue abrir RSS feeds que exijam autenticação, a menos que a autenticação Windows NT LAN Manager (LAN) esteja disponível e não possa carregar RSS feeds de locais de protocolo SSL.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Compartilhamento de grupo](group-sharing.md)

