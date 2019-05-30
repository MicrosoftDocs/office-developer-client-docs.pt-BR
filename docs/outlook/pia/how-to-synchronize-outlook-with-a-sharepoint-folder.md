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
# <a name="synchronize-outlook-with-a-sharepoint-folder"></a>Sincronizar o Outlook com uma pasta do SharePoint

Este exemplo mostra como conectar o Outlook programaticamente com uma pasta do SharePoint e como sincronizar o conteúdo da pasta.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho da [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No Outlook, você pode sincronizar calendários, listas de contatos, listas de tarefas, quadros de discussão e bibliotecas de documentos para pastas do SharePoint. Com base na URL fornecida após a sincronização, o Outlook criará uma nova pasta do mesmo tipo de base, como pasta do SharePoint. Por exemplo, a sincronização de uma pasta de calendário do SharePoint criará uma nova pasta de calendário no Outlook. Pastas de sincronização do SharePoint são armazenadas em sua Pasta Pessoal do Outlook (. pst) fora da caixa de correio do usuário. Você pode se conectar a uma pasta do SharePoint usando o método[OpenSharedFolder (cadeia de caracteres, objeto, objeto, objeto)](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Observe que você deve usar uma URL stssync: / / que  forneça detalhes sobre o servidor do SharePoint, o caminho da pasta e outras informações que o Outlook precisa para abrir uma pasta do SharePoint.

Ao se conectar a uma pasta do SharePoint por programação, você deve determinar a URL adequada a ser usada para criar a relação de compartilhamento. Como a URL stssync: / / não é fornecida na interface do usuário do SharePoint para a pasta, conecte manualmente a pasta de destino para o Outlook. Então use o primeiro procedimento, DisplaySharePointUrl, no exemplo a seguir, para obter a URL correta. O DisplaySharePointUrl usa o objeto[tabela](https://msdn.microsoft.com/library/bb652856\(v=office.15\))para procurar as informações de associação de compartilhamento na pasta atual para a janela de navegador ativo. Se um ou mais contextos de associação forem encontrados, as URLs de todos os contextos de compartilhamento disponíveis serão exibidas.

Agora você tem a URL correta para criar a relação de compartilhamento. Para sincronizar a nova pasta do SharePoint no Outlook, copie e cole a URL para a tarefa a variável de cadeia de caracteres calendarUrl no segundo procedimento AddSpsFolder. O AddSpsFolder automatiza a sincronização da nova pasta do SharePoint no Outlook usando o método**NameSpace.OpenSharedFolder**com uma`stssync://` URL (nesse caso, a URL produzida pela procedimento DisplaySharePointUrl) . O AddSpsFolderalso fornece um nome de pasta personalizada  "Exemplo SPS calendário" e especifica o Outlook para usar o tempo de vida padrão (TTL) da pasta. As pastas do SharePoint sempre fazem download de anexos, assim você não precisa especificar isso nela.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Compartilhamento de grupo](group-sharing.md)

