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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705383"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a><span data-ttu-id="90a44-102">Importar dados XML de compromisso para objetos de compromisso do Outlook</span><span class="sxs-lookup"><span data-stu-id="90a44-102">Import appointment XML data into Outlook appointment objects</span></span>

<span data-ttu-id="90a44-103">Este tópico mostra como ler dados de compromisso formatados em XML, salvar os dados em objetos [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) do Outlook no calendário padrão e retornar os objetos de compromisso em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="90a44-103">This topic shows how to read appointment data formatted in XML, save the data to Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) objects in the default calendar, and return the appointment objects in an array.</span></span>

## <a name="example"></a><span data-ttu-id="90a44-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="90a44-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="90a44-105">Helmut Obertanner forneceu os exemplos de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="90a44-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="90a44-106">A experiência de Helmut é em Ferramentas de Desenvolvedor do Office para Visual Studio e Outlook.</span><span class="sxs-lookup"><span data-stu-id="90a44-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="90a44-107">Os exemplos de código a seguir contêm o método CreateAppointmentsFromXml da classe Sample, implementados como parte de um projeto de suplemento do Outlook.</span><span class="sxs-lookup"><span data-stu-id="90a44-107">The following code examples contain the CreateAppointmentsFromXml method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="90a44-108">Cada projeto adiciona uma referência para o Outlook PIA, que se baseia no namespace [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="90a44-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="90a44-109">O método CreateAppointmentsFromXml aceita dois parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="90a44-109">The CreateAppointmentsFromXml method accepts two input parameters:</span></span>

  - <span data-ttu-id="90a44-110">"application" é um objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) confiável do Outlook.</span><span class="sxs-lookup"><span data-stu-id="90a44-110">application is a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

  - <span data-ttu-id="90a44-111">"xml" é uma cadeia de caracteres XML ou uma cadeia de caracteres que representa um caminho para um arquivo XML válido.</span><span class="sxs-lookup"><span data-stu-id="90a44-111">xml is either an XML string, or a string that represents a path to a valid XML file.</span></span> <span data-ttu-id="90a44-112">Para as finalidades dos seguintes exemplos de código, o XML delimita os dados do compromisso usando as seguintes marcas XML:</span><span class="sxs-lookup"><span data-stu-id="90a44-112">For the purpose of the following code examples, the XML delimits appointment data by using the following XML tags:</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="90a44-113">Dados de compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-113">Appointment data</span></span></p></th>
    <th><p><span data-ttu-id="90a44-114">Marca XML de delimitação</span><span class="sxs-lookup"><span data-stu-id="90a44-114">Delimiting XML tag</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="90a44-115">Todo o conjunto de dados do compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-115">Entire set of appointment data</span></span></p></td>
    <td><p><span data-ttu-id="90a44-116">appointments</span><span class="sxs-lookup"><span data-stu-id="90a44-116">appointments</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="90a44-117">Cada compromisso no conjunto</span><span class="sxs-lookup"><span data-stu-id="90a44-117">Each appointment in the set</span></span></p></td>
    <td><p><span data-ttu-id="90a44-118">appointment</span><span class="sxs-lookup"><span data-stu-id="90a44-118">appointment</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="90a44-119">Hora de início de um compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-119">Start time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="90a44-120">starttime</span><span class="sxs-lookup"><span data-stu-id="90a44-120">starttime</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="90a44-121">Hora de término de um compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-121">End time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="90a44-122">endtime</span><span class="sxs-lookup"><span data-stu-id="90a44-122">endtime</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="90a44-123">Título de um compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-123">Title of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="90a44-124">subject</span><span class="sxs-lookup"><span data-stu-id="90a44-124">subject</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="90a44-125">Local de um compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-125">Location of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="90a44-126">location</span><span class="sxs-lookup"><span data-stu-id="90a44-126">location</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="90a44-127">Detalhes de um compromisso</span><span class="sxs-lookup"><span data-stu-id="90a44-127">Details of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="90a44-128">body</span><span class="sxs-lookup"><span data-stu-id="90a44-128">body</span></span></p></td>
    </tr>
    </tbody>
    </table>


<span data-ttu-id="90a44-129">O exemplo a seguir mostra dados de entrada para o parâmetro *xml*.</span><span class="sxs-lookup"><span data-stu-id="90a44-129">The following example shows input data for the *xml* parameter.</span></span>

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

<span data-ttu-id="90a44-130">O método CreateAppointmentsFromXml emprega a implementação do Microsoft COM do Modelo de Objeto de Documento XML (DOM) para carregar e processar os dados XML que o xml fornece.</span><span class="sxs-lookup"><span data-stu-id="90a44-130">The CreateAppointmentsFromXml method uses the Microsoft COM implementation of the XML Document Object Model (DOM) to load and process the XML data that xml provides.</span></span> <span data-ttu-id="90a44-131">CreateAppointmentsFromXml verifica primeiro se o xml especifica uma fonte válida de dados XML.</span><span class="sxs-lookup"><span data-stu-id="90a44-131">CreateAppointmentsFromXml first checks whether xml specifies a valid source of XML data.</span></span> <span data-ttu-id="90a44-132">Se sim, ele carrega os dados em um documento XML, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="90a44-132">If so, it loads the data into an XML document, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)).</span></span> <span data-ttu-id="90a44-133">Caso contrário, CreateAppointmentsFromXml gera uma exceção.</span><span class="sxs-lookup"><span data-stu-id="90a44-133">Otherwise, CreateAppointmentsFromXml throws an exception.</span></span> <span data-ttu-id="90a44-134">Para mais informações sobre o DOM XML, confira [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="90a44-134">For more information about the XML DOM, see [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span></span>

<span data-ttu-id="90a44-135">Para cada nó filho de compromisso delimitado pela marca "appointment" nos dados XML, o CreateAppointmentsFromXml procura marcas específicas, usa o DOM para extrair os dados e atribui os dados às propriedades correspondentes de um objeto **AppointmentItem**: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) e [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="90a44-135">For each appointment child node delimited by the appointment tag in the XML data, CreateAppointmentsFromXml looks for specific tags, uses the DOM to extract the data, and assigns the data to corresponding properties of an **AppointmentItem** object: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span></span> <span data-ttu-id="90a44-136">CreateAppointmentsFromXml salva o compromisso no calendário padrão.</span><span class="sxs-lookup"><span data-stu-id="90a44-136">CreateAppointmentsFromXml then saves the appointment to the default calendar.</span></span>

<span data-ttu-id="90a44-137">CreateAppointmentsFromXml usa o método [Adicionar](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) da classe [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) no namespace [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) para agregar esses objetos AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="90a44-137">CreateAppointmentsFromXml uses the [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) method of the [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) class in the [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) namespace to aggregate these AppointmentItem objects.</span></span> <span data-ttu-id="90a44-138">Quando o método tiver processado todos os compromissos nos dados XML, ele retorna os objetos AppointmentItem em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="90a44-138">When the method has processed all the appointments in the XML data, it returns the AppointmentItem objects in an array.</span></span>

<span data-ttu-id="90a44-139">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="90a44-139">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="90a44-140">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="90a44-140">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="90a44-141">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="90a44-141">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="90a44-142">A seguir está um exemplo de código do Visual Basic, seguido do exemplo de código C\#.</span><span class="sxs-lookup"><span data-stu-id="90a44-142">The following is the Visual Basic code example, followed by the C\# code example.</span></span>



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

## <a name="see-also"></a><span data-ttu-id="90a44-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="90a44-143">See also</span></span>

- [<span data-ttu-id="90a44-144">Compromissos</span><span class="sxs-lookup"><span data-stu-id="90a44-144">Appointments</span></span>](appointments.md)

