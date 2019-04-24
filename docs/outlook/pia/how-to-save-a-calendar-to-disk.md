---
title: Salvar um calendário no disco
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361044"
---
# <a name="save-a-calendar-to-disk"></a>Salvar um calendário no disco

Este exemplo mostra como salvar um calendário inteiro no disco no formato de arquivo iCalendar (ICS).

## <a name="example"></a>Exemplo

Este exemplo de código usa o objeto [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) que é compatível com o salvamento de um calendário inteiro ou um intervalo de compromissos do calendário para o disco. O Outlook otimiza automaticamente um arquivo .ics para que os compromissos recorrentes não sejam salvos como compromissos individuais no arquivo .ics. Dependendo do tamanho do calendário que está sendo salvo, salvar um calendário em disco pode levar um tempo significativo. Ao salvar o calendário, a janela do Outlook parece não responder ao usuário.

O exemplo de código primeiro chama [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) na pasta Calendário padrão para receber um objeto **CalendarSharing**. Em seguida, ele define propriedades do objeto **CalendarSharing** para especificar critérios para a exportação, como se deve salvar o calendário todo e se deseja incluir detalhes dos compromissos marcados como "particulares".

Para salvar as informações do calendário no formato de arquivo .ics, o exemplo de código chama o método [ForwardAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) do objeto **CalendarSharing**.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a>Confira também

- [Calendar](calendar.md)

