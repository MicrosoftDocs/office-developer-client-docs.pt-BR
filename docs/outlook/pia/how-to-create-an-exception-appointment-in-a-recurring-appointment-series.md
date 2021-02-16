---
title: Criar um compromisso de exceção em uma série de compromissos recorrentes
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356431"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a>Criar um compromisso de exceção em uma série de compromissos recorrentes

Este exemplo usa um objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) para criar uma exceção para um padrão de recorrência padrão para um compromisso.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Depois de excluir ou alterar uma ocorrência de compromisso de um compromisso recorrente, o Outlook cria um objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)). O objeto Exception permite que você crie uma exceção para um padrão de recorrência padrão. As propriedades do objeto contêm as alterações feitas à instância do compromisso. O conjunto [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) contém todos os objetos de Exception para um compromisso recorrente, e é associado o objeto [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) do compromisso.

Para obter o objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) que representa a exceção ao padrão de recorrência original do compromisso recorrente, use a propriedade [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) da Exception. Usando os métodos e propriedades do AppointmentItem retornado, você pode definir as propriedades da exceção de compromisso.

Ao trabalhar com itens de compromisso recorrente, você deve liberar referências anteriores, obter novas referências para o item de compromisso recorrente antes de acessar ou modificar o item e liberar essas referências assim que tiver terminado e salvado as alterações. Essa prática aplica o objeto **AppointmentItem** recorrente e a qualquer objeto [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Para liberar uma referência no Visual Basic, defina esse objeto existente como Nothing. No C\#, libere explicitamente a memória para esse objeto.

Observe que, mesmo depois que você liberar a sua referência e tenta obter uma referência de nova, se ainda houver uma referência ativa, conduzida por outro suplemento ou no Outlook, como um dos objetos acima, sua nova referência continuarão a apontar para uma cópia desatualizada do objeto. Portanto, é importante que você libera seus referências tão logo terminar com um compromisso recorrente.

No exemplo código a seguir, CreateExceptionExample altera o assunto do compromisso recorrente que foi criado no tópico [Encontrar um compromisso específico em uma série de compromissos recorrentes](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md) e, em seguida, usa a propriedade AppointmentItem do objeto Exception resultante para recuperar o AppointmentItem que corresponde à exceção do compromisso. CreateExceptionExample em seguida altera as horas de início e término da exceção do compromisso.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Compromissos](appointments.md)

