---
title: Importar dados XML de compromisso para objetos de compromisso do Outlook
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0af86772fced3e69d1d28cf8d98a544e3b4d90d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320059"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a>Importar dados XML de compromisso para objetos de compromisso do Outlook

Este tópico mostra como ler dados de compromisso formatados em XML, salvar os dados em objetos [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) do Outlook no calendário padrão e retornar os objetos de compromisso em uma matriz.

## <a name="example"></a>Exemplo

> [!NOTE] 
> Helmut Obertanner forneceu os exemplos de código a seguir. A experiência de Helmut é em Ferramentas de Desenvolvedor do Office para Visual Studio e Outlook. 


Os exemplos de código a seguir contêm o método CreateAppointmentsFromXml da classe Sample, implementados como parte de um projeto de suplemento do Outlook. Cada projeto adiciona uma referência para o Outlook PIA, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).

O método CreateAppointmentsFromXml aceita dois parâmetros de entrada:

  - "application" é um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) confiável do Outlook.

  - "xml" é uma cadeia de caracteres XML ou uma cadeia de caracteres que representa um caminho para um arquivo XML válido. Para as finalidades dos seguintes exemplos de código, o XML delimita os dados do compromisso usando as seguintes marcas XML:
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Dados de compromisso</p></th>
    <th><p>Marca XML de delimitação</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Todo o conjunto de dados do compromisso</p></td>
    <td><p>appointments</p></td>
    </tr>
    <tr class="even">
    <td><p>Cada compromisso no conjunto</p></td>
    <td><p>appointment</p></td>
    </tr>
    <tr class="odd">
    <td><p>Hora de início de um compromisso</p></td>
    <td><p>starttime</p></td>
    </tr>
    <tr class="even">
    <td><p>Hora de término de um compromisso</p></td>
    <td><p>endtime</p></td>
    </tr>
    <tr class="odd">
    <td><p>Título de um compromisso</p></td>
    <td><p>subject</p></td>
    </tr>
    <tr class="even">
    <td><p>Local de um compromisso</p></td>
    <td><p>location</p></td>
    </tr>
    <tr class="odd">
    <td><p>Detalhes de um compromisso</p></td>
    <td><p>body</p></td>
    </tr>
    </tbody>
    </table>


O exemplo a seguir mostra dados de entrada para o parâmetro *xml*.

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

O método CreateAppointmentsFromXml emprega a implementação do Microsoft COM do Modelo de Objeto de Documento XML (DOM) para carregar e processar os dados XML que o xml fornece. CreateAppointmentsFromXml verifica primeiro se o xml especifica uma fonte válida de dados XML. Se sim, ele carrega os dados em um documento XML, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Caso contrário, CreateAppointmentsFromXml gera uma exceção. Para mais informações sobre o DOM XML, confira [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).

Para cada nó filho de compromisso delimitado pela marca "appointment" nos dados XML, o CreateAppointmentsFromXml procura marcas específicas, usa o DOM para extrair os dados e atribui os dados às propriedades correspondentes de um objeto **AppointmentItem**: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) e [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)). CreateAppointmentsFromXml salva o compromisso no calendário padrão.

CreateAppointmentsFromXml usa o método [Adicionar](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) da classe [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) no namespace [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) para agregar esses objetos AppointmentItem. Quando o método tiver processado todos os compromissos nos dados XML, ele retorna os objetos AppointmentItem em uma matriz.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

