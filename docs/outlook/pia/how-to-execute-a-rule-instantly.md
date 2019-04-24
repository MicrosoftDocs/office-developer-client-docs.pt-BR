---
title: Executar uma regra instantaneamente
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6bb6ac5422b9785660cb3ec0020c01244002c6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320367"
---
# <a name="execute-a-rule-instantly"></a>Executar uma regra instantaneamente

Este exemplo mostra como executar uma regra instantaneamente usando o método [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) do objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Você pode fazer uma regra ser executada imediatamente chamando o método **Execute** no objeto **Rule**. Os parâmetros para o método **Execute** são opcionais. Se eles não forem especificados, a regra será aplicada a todas as mensagens na Caixa de Entrada, mas não às subpastas da Caixa de Entrada, e os valores padrão para os parâmetros serão usados. A tabela a seguir lista os valores padrão para os parâmetros opcionais do método **Execute**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parâmetro</p></th>
<th><p>Valor padrão</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowProgress</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Pasta</p></td>
<td><p>Caixa de Entrada</p></td>
</tr>
<tr class="odd">
<td><p>IncludeSubfolders</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>RuleExecuteOption</p></td>
<td><p>OlRuleExecuteOption.olRuleExecuteAllMessages</p></td>
</tr>
</tbody>
</table>


Você pode cancelar a execução de uma regra usando o Assistente de Regras e Alertas. Também é possível cancelar a execução de uma regra definindo o parâmetro *ShowProgress* como **true** e cancelando a caixa de diálogo de progresso. Depois de cancelar a caixa de diálogo de progresso, **Execute** retornará um erro.

No exemplo de código a seguir, ExecuteManagerRule é a regra criada no procedimento CreateManagerRule do tópico [Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md). ExecuteManagerRule, em seguida, verifica se a regra não é uma referência nula. Se a regra não for uma referência nula, ExecuteManagerRule chama o método **Execute** na regra com parâmetros padrão, instantaneamente executando a regra.

> [!NOTE]
> Para aplicar uma regra uma vez, independentemente de se a propriedade [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) retorna **true**, use o método **Rule.Execute**. Para aplicar a regra para a sessão atual e sessões futuras, use a propriedade **Rule.Enabled** e o método [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)).

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
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

- [Regras](rules.md)

