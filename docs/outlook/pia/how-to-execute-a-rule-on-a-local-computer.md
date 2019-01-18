---
title: Executar uma regra em um computador local
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9840133b7cd70b72e0bedf57931dfa9e53c67b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709933"
---
# <a name="execute-a-rule-on-a-local-computer"></a><span data-ttu-id="0fb71-102">Executar uma regra em um computador local</span><span class="sxs-lookup"><span data-stu-id="0fb71-102">Execute a rule on a local computer</span></span>

<span data-ttu-id="0fb71-103">Esse exemplo mostra como executar uma regra em um computador local usando a propriedade [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) do objeto [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0fb71-103">This example shows how to execute a rule on a local computer by using the [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="0fb71-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0fb71-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0fb71-105">O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0fb71-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="0fb71-106">Se sua caixa de correio estiver hospedada em um servidor Exchange, uma regra pode ser executada no servidor Exchange ou no cliente do Outlook.</span><span class="sxs-lookup"><span data-stu-id="0fb71-106">If your mailbox is hosted on an Exchange server, a rule can be executed on the Exchange server or on the Outlook client.</span></span> <span data-ttu-id="0fb71-107">Se a regra for executada no servidor, o Outlook não precisará executar as condições da regra para que haja avaliação e para que as ações de regra sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="0fb71-107">If the rule is executed on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span> <span data-ttu-id="0fb71-108">Se a regra for executada no cliente, o Outlook deve estar executando essa regra.</span><span class="sxs-lookup"><span data-stu-id="0fb71-108">If the rule is executed on the client, Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="0fb71-109">Se a propriedade[IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) da[regra](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) objeto retornar **verdadeiro**, a regra será executada no cliente.</span><span class="sxs-lookup"><span data-stu-id="0fb71-109">If the [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object returns **true**, the rule is executed on the client.</span></span>

<span data-ttu-id="0fb71-110">Para encontrar ações de regra executadas no cliente por padrão (por exemplo, exibindo um alerta de novo email), a condição**OnLocalMachine** será ativada automaticamente e a propriedade [habilitado](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) será definida como **verdadeira** somente o lado do cliente do objeto[RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0fb71-110">For rule actions that execute on the client by default (such as displaying a new mail alert), the **OnLocalMachine** condition will automatically be enabled, and the [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) property is set to **true** for a client-side-only [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) object.</span></span> <span data-ttu-id="0fb71-111">Para ações de regra geralmente executadas no servidor, defina a propriedade**habilitada** somente o lado do cliente do objeto **RuleAction** objeto para permitir a condição**OnLocalMachine**.</span><span class="sxs-lookup"><span data-stu-id="0fb71-111">For rule actions that generally execute on the server, set the **Enabled** property of the client-side-only **RuleAction** object to enable the **OnLocalMachine** condition.</span></span> <span data-ttu-id="0fb71-112">Isso forçará a regra a executar localmente no cliente.</span><span class="sxs-lookup"><span data-stu-id="0fb71-112">This will force the rule to execute locally on the client.</span></span> 

<span data-ttu-id="0fb71-113">Quando a condição **OnLocalMachine** para uma regra estiver habilitada, a condição [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) também será habilitada quando a mesma regra for examinada de outro computador.</span><span class="sxs-lookup"><span data-stu-id="0fb71-113">When the **OnLocalMachine** condition for a rule is enabled, the [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) condition will also be enabled when the same rule is examined from another machine.</span></span> <span data-ttu-id="0fb71-114">Uma condição de tipo de regra [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indica que a regra pode ser executada apenas em um computador específico, diferente daquele atual e não podem ser programaticamente habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0fb71-114">A rule condition of type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indicates that the rule can execute only on a specific computer other than the current one, and cannot be programmatically enabled or disabled.</span></span> <span data-ttu-id="0fb71-115">Por exemplo, se uma regra for criada no computador e a condição de regra**OnLocalMachine** estiver habilitada, a regra pode ser executada apenas nesse computador.</span><span class="sxs-lookup"><span data-stu-id="0fb71-115">For example, if a rule is created on the current computer and the **OnLocalMachine** rule condition is enabled, the rule can execute only on that computer.</span></span> <span data-ttu-id="0fb71-116">Se a mesma regra for executada em outro computador, a regra mostrará que a condição **OnOtherMachine** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0fb71-116">If the same rule is executed on another computer, the rule will show that the **OnOtherMachine** rule condition is enabled.</span></span>

<span data-ttu-id="0fb71-117">No exemplo código a seguir, DemoOnMachineOnly cria uma regra e permite a condição[OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) e a ação[encaminhar](https://msdn.microsoft.com/library/bb652908\(v=office.15\)), configurando a propriedade **habilitado**como **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="0fb71-117">In the following code example, DemoOnMachineOnly creates a rule and enables the [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) condition and [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) action by setting the **Enabled** properties to **true**.</span></span> <span data-ttu-id="0fb71-118">A condição**OnLocalMachine**será habilitada em seguida, forçando uma regra de servidor para executar localmente, e as regras serão salvas.</span><span class="sxs-lookup"><span data-stu-id="0fb71-118">The **OnLocalMachine** condition is then enabled, forcing a server-side rule to execute locally, and the rules are saved.</span></span> <span data-ttu-id="0fb71-119">Por padrão, as ações**encaminhar** e **OnlyToMe** condição serão realizadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="0fb71-119">By default, a **Forward** action and **OnlyToMe** condition will operate on the server.</span></span> <span data-ttu-id="0fb71-120">Uma vez que a condição**OnLocalMachine** for habilitada, elas serão realizado via de regra do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="0fb71-120">Once the **OnLocalMachine** condition has been enabled, they will operate as a client-side rule.</span></span>

<span data-ttu-id="0fb71-121">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar a namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0fb71-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0fb71-122">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="0fb71-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0fb71-123">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="0fb71-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a><span data-ttu-id="0fb71-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fb71-124">See also</span></span>

- [<span data-ttu-id="0fb71-125">Regras</span><span class="sxs-lookup"><span data-stu-id="0fb71-125">Rules</span></span>](rules.md)

