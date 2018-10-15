---
title: Executar uma regra em um computador local
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 76587a72d9c77a5484d9aa9788173f9f40f57614
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405837"
---
# <a name="execute-a-rule-on-a-local-computer"></a>Executar uma regra em um computador local

Esse exemplo mostra como executar uma regra em um computador local usando a propriedade [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) do objeto [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Se sua caixa de correio estiver hospedada em um servidor Exchange, uma regra pode ser executada no servidor Exchange ou no cliente do Outlook. Se a regra for executada no servidor, o Outlook não precisará executar as condições da regra para que haja avaliação e para que as ações de regra sejam concluídas. Se a regra for executada no cliente, o Outlook deve estar executando essa regra. Se a propriedade[IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) da[regra](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) objeto retornar **verdadeiro**, a regra será executada no cliente.

Para encontrar ações de regra executadas no cliente por padrão (por exemplo, exibindo um alerta de novo email), a condição**OnLocalMachine** será ativada automaticamente e a propriedade [habilitado](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) será definida como **verdadeira** somente o lado do cliente do objeto[RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)). Para ações de regra geralmente executadas no servidor, defina a propriedade**habilitada** somente o lado do cliente do objeto **RuleAction** objeto para permitir a condição**OnLocalMachine**. Isso forçará a regra a executar localmente no cliente. 

Quando a condição **OnLocalMachine** para uma regra estiver habilitada, a condição [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) também será habilitada quando a mesma regra for examinada de outro computador. Uma condição de tipo de regra [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indica que a regra pode ser executada apenas em um computador específico, diferente daquele atual e não podem ser programaticamente habilitada ou desabilitada. Por exemplo, se uma regra for criada no computador e a condição de regra**OnLocalMachine** estiver habilitada, a regra pode ser executada apenas nesse computador. Se a mesma regra for executada em outro computador, a regra mostrará que a condição **OnOtherMachine** está habilitada.

No exemplo código a seguir, DemoOnMachineOnly cria uma regra e permite a condição[OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) e a ação[encaminhar](https://msdn.microsoft.com/library/bb652908\(v=office.15\)), configurando a propriedade **habilitado**como **verdadeiro**. A condição**OnLocalMachine**será habilitada em seguida, forçando uma regra de servidor para executar localmente, e as regras serão salvas. Por padrão, as ações**encaminhar** e **OnlyToMe** condição serão realizadas no servidor. Uma vez que a condição**OnLocalMachine** for habilitada, elas serão realizado via de regra do lado do cliente.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar a namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Regras](rules.md)

