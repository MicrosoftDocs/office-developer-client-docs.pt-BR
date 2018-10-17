---
title: Exibir a caixa de diálogo Escolher Nomes para resolver os destinatários
TOCTitle: Display the Select Names dialog box to resolve recipients
ms:assetid: 841dd4cd-6d69-46d5-8c83-e28c95b631a9
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646055(v=office.15)
ms:contentKeyID: 55119876
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 56fb1a4abbcfca3a504315c4a0f9ba75a663aa02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405648"
---
# <a name="display-the-select-names-dialog-box-to-resolve-recipients"></a>Exibir a caixa de diálogo Escolher Nomes para resolver os destinatários

Este exemplo tenta resolver os destinatários fornecidos pelo parâmetro *recips* e exibe a caixa de diálogo **Escolher nomes** do Outlook para cada destinatário ambíguo que não pode ser resolvido.

## <a name="example"></a>Exemplo

Este exemplo de código chama o objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) para exibir a caixa de diálogo **Selecionar Nomes**, que mostra o catálogo de endereços do Outlook. Por meio dessa caixa de diálogo, o usuário pode selecionar um nome do catálogo de endereços. Se o nome não for resolvido, o destinatário será removido de recips. Se o nome for resolvido, o exemplo de código retornará o objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) do destinatário para recips.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ResolveRecipients(ByVal recips As Outlook.Recipients)
    If recips Is Nothing Then
        Throw New ArgumentNullException()
    End If
    If recips.ResolveAll() Then
        Return
    Else
        For i As Integer = recips.Count To 1 Step -1
            If Not (recips(i).Resolve()) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.Recipients.Add(recips(i).Name)
                snd.NumberOfRecipientSelectors = _
                    Outlook.OlRecipientSelectors.olShowTo
                snd.AllowMultipleSelection = False
                snd.Display()
                If Not (snd.Recipients.ResolveAll()) Then
                    recips.Remove(i)
                Else
                    recips.Remove(i)
                    recips.Add(snd.Recipients(1).Address)
                End If
                snd = Nothing
            End If
        Next
    End If
End Sub
```


```csharp
private void ResolveRecipients(Outlook.Recipients recips)
{
    if (recips == null)
    {
        throw new ArgumentNullException();
    }
    if (recips.ResolveAll())
    {
        return;
    }
    else
    {
        for (int i = recips.Count; i > 0; i--)
        {
            if (!recips[i].Resolve())
            {
                Outlook.SelectNamesDialog snd =
                    Application.Session.
                    GetSelectNamesDialog();
                snd.Recipients.Add(recips[i].Name);
                snd.NumberOfRecipientSelectors =
                    Outlook.OlRecipientSelectors.olShowTo;
                snd.AllowMultipleSelection = false;
                snd.Display();
                if (!snd.Recipients.ResolveAll())
                {
                    recips.Remove(i);
                }
                else
                {
                    recips.Remove(i);
                    recips.Add(snd.Recipients[1].Address);
                }
                snd = null;
            }
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Destinatários](recipients.md)

