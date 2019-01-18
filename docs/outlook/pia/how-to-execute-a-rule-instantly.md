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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708645"
---
# <a name="execute-a-rule-instantly"></a><span data-ttu-id="a7efb-102">Executar uma regra instantaneamente</span><span class="sxs-lookup"><span data-stu-id="a7efb-102">Execute a rule instantly</span></span>

<span data-ttu-id="a7efb-103">Este exemplo mostra como executar uma regra instantaneamente usando o método [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) do objeto [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a7efb-103">This example shows how to execute a rule instantly by using the [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) method of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="a7efb-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a7efb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a7efb-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a7efb-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a7efb-106">Você pode fazer uma regra ser executada imediatamente chamando o método **Execute** no objeto **Rule**.</span><span class="sxs-lookup"><span data-stu-id="a7efb-106">You can cause a rule to execute immediately by calling the **Execute** method on the **Rule** object.</span></span> <span data-ttu-id="a7efb-107">Os parâmetros para o método **Execute** são opcionais. Se eles não forem especificados, a regra será aplicada a todas as mensagens na Caixa de Entrada, mas não às subpastas da Caixa de Entrada, e os valores padrão para os parâmetros serão usados.</span><span class="sxs-lookup"><span data-stu-id="a7efb-107">The parameters to the **Execute** method are optional; if they are not specified, the rule will be applied to all messages in the Inbox but not to the subfolders of the Inbox, and default values for the parameters will be used.</span></span> <span data-ttu-id="a7efb-108">A tabela a seguir lista os valores padrão para os parâmetros opcionais do método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="a7efb-108">The following table lists the default values for the optional parameters of the **Execute** method.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7efb-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7efb-109">Parameter</span></span></p></th>
<th><p><span data-ttu-id="a7efb-110">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="a7efb-110">Default value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7efb-111">ShowProgress</span><span class="sxs-lookup"><span data-stu-id="a7efb-111">ShowProgress</span></span></p></td>
<td><p><span data-ttu-id="a7efb-112">False</span><span class="sxs-lookup"><span data-stu-id="a7efb-112">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7efb-113">Pasta</span><span class="sxs-lookup"><span data-stu-id="a7efb-113">Folder</span></span></p></td>
<td><p><span data-ttu-id="a7efb-114">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="a7efb-114">Inbox</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7efb-115">IncludeSubfolders</span><span class="sxs-lookup"><span data-stu-id="a7efb-115">IncludeSubfolders</span></span></p></td>
<td><p><span data-ttu-id="a7efb-116">False</span><span class="sxs-lookup"><span data-stu-id="a7efb-116">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7efb-117">RuleExecuteOption</span><span class="sxs-lookup"><span data-stu-id="a7efb-117">RuleExecuteOption</span></span></p></td>
<td><p><span data-ttu-id="a7efb-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span><span class="sxs-lookup"><span data-stu-id="a7efb-118">OlRuleExecuteOption.olRuleExecuteAllMessages</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7efb-119">Você pode cancelar a execução de uma regra usando o Assistente de Regras e Alertas.</span><span class="sxs-lookup"><span data-stu-id="a7efb-119">You can cancel a rule execution by using the Rules and Alerts Wizard.</span></span> <span data-ttu-id="a7efb-120">Também é possível cancelar a execução de uma regra definindo o parâmetro *ShowProgress* como **true** e cancelando a caixa de diálogo de progresso.</span><span class="sxs-lookup"><span data-stu-id="a7efb-120">You can also cancel a rule execution by setting the *ShowProgress* parameter to **true** and then canceling the progress dialog box.</span></span> <span data-ttu-id="a7efb-121">Depois de cancelar a caixa de diálogo de progresso, **Execute** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="a7efb-121">Once you cancel the progress dialog box, **Execute** will return an error.</span></span>

<span data-ttu-id="a7efb-122">No exemplo de código a seguir, ExecuteManagerRule é a regra criada no procedimento CreateManagerRule do tópico [Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="a7efb-122">In the following code example, ExecuteManagerRule gets the rule that was created in the procedure CreateManagerRule from the topic [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span> <span data-ttu-id="a7efb-123">ExecuteManagerRule, em seguida, verifica se a regra não é uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="a7efb-123">ExecuteManagerRule then checks whether the rule is not a null reference.</span></span> <span data-ttu-id="a7efb-124">Se a regra não for uma referência nula, ExecuteManagerRule chama o método **Execute** na regra com parâmetros padrão, instantaneamente executando a regra.</span><span class="sxs-lookup"><span data-stu-id="a7efb-124">If the rule is not a null reference, ExecuteManagerRule calls the **Execute** method on the rule with default parameters, instantly executing the rule.</span></span>

> [!NOTE]
> <span data-ttu-id="a7efb-125">Para aplicar uma regra uma vez, independentemente de se a propriedade [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) retorna **true**, use o método **Rule.Execute**.</span><span class="sxs-lookup"><span data-stu-id="a7efb-125">To apply a rule once, regardless of whether the [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) property returns **true**, use the **Rule.Execute** method.</span></span> <span data-ttu-id="a7efb-126">Para aplicar a regra para a sessão atual e sessões futuras, use a propriedade **Rule.Enabled** e o método [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="a7efb-126">To apply the rule for the current session and beyond the current session, use both the **Rule.Enabled** property and the [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) method.</span></span>

<span data-ttu-id="a7efb-127">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a7efb-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a7efb-128">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="a7efb-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a7efb-129">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="a7efb-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a7efb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7efb-130">See also</span></span>

- [<span data-ttu-id="a7efb-131">Regras</span><span class="sxs-lookup"><span data-stu-id="a7efb-131">Rules</span></span>](rules.md)

