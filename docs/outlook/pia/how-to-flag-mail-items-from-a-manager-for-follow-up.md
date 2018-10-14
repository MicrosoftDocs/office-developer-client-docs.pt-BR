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
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a>Sinalizar itens de email de um gerente para acompanhamento

Este exemplo mostra como sinalizar para acompanhamento itens de email que foram recebidos do gerente do usuário.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O Microsoft Outlook fornece um sistema de sinalização de tarefas em que determinados itens do Outlook, como itens de email ou itens de contatos, podem ser sinalizados para acompanhamento. Quando você sinaliza um item do Outlook para acompanhamento, informações sobre esse item do Outlook, além de outras informações com base em tarefas, são exibidas na **Barra de Tarefas Pendentes** e no módulo de navegação de Calendário na interface de usuário do Outlook. A **Barra de Tarefas Pendentes** é exibida como um painel vertical em uma configuração comum da janela do explorador do Outlook. Ela contém um controle do navegador de datas, compromissos futuros e itens que foram sinalizados para acompanhamento. A **Barra de Tarefas Pendentes** em si não é expansível, e você pode só definir opções de configuração para a **Barra de Tarefas Pendentes** por meio da interface de usuário do Outlook. Sinalizar itens permite organizar e priorizar tarefas e itens pendentes.

O exemplo a seguir marcas de um grupo de itens para um intervalo de acompanhamento especificado. O exemplo coloca todos os itens na Caixa de Entrada do usuário que sejam do gerente do usuário atual usando uma consulta DAV de Pesquisa e Localização (DASL) para filtrar mensagens do tipo "IPM.NOTE" com o nome do gerente como remetente. Ele marca, em seguida, todos os itens de acordo com o valor [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) da propriedade [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)). Todos os itens de alta prioridade estão sinalizados para acompanhamento hoje e todos os itens de importância normal estão sinalizados para acompanhamento esta semana, usando o método [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).


> [!NOTE]
> A propriedade **Importance** e o método **MarkAsTask** são membros de objeto **Item**.


Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Tarefas](tasks.md)

