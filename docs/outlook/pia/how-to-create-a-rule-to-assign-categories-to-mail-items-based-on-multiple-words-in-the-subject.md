---
title: Criar uma regra para atribuir categorias a itens de email com base em várias palavras utilizadas no assunto
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f0b8b27eb65ef32f95d5529879dde2721e280e26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349515"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a>Criar uma regra para atribuir categorias a itens de email com base em várias palavras utilizadas no assunto

Este exemplo mostra como configurar uma regra que atribua categorias a itens de email com base em várias palavras no assunto.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No Outlook, os itens podem ser categorizados para exibição e a organização mais fáceis. O modelo de objeto do Outlook fornece o objeto [categoria](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) e o conjunto [categorias](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) representam categorias. Para saber mais sobre o objeto **categoria** e o conjunto **categorias** de um item do Outlook, confira [enumerar e adicionar categorias](how-to-enumerate-and-add-categories.md).

Uma regra, representada pelo objeto [regra](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), pode ser atribuída com várias condições. Você pode começar ou definir uma matriz que represente as condições avaliadas ou as ações a serem concluídas. Por exemplo, a propriedade[texto](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) do objeto[TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) retorna ou reúne uma matriz de elementos da cadeia de caracteres que representa o texto a ser avaliado pela condição de regra. Você pode atribuir uma matriz com uma ou várias sequências de caracteres para avaliação. Para avaliar várias cadeias de caracteres que estejam atribuídas a uma matriz, use a operação OU lógico. 

As propriedades que você pode usar para acessar ou definir uma matriz são as seguintes: [endereço](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [categorias](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [categorias](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [nome do formulário](https://msdn.microsoft.com/library/bb647042\(v=office.15\))e **TextRuleCondition.Text**. Para saber mais sobre regras, confira [criar uma regra para itens de Email do arquivo de um gerente e sinalize-a para acompanhamento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).

No exemplo a seguir o CreateTextAndCategoryRule usa o método CategoryExists para verificar os itens de email do usuário para qualquer categoria pelo nome "Office" ou "Outlook" no conjunto **categorias**. Se nenhuma categoria for encontrada, eles serão adicionados. O exemplo em seguida cria uma matriz de cadeias de caracteres que incluem "Office","Outlook" e "2007". Essa matriz representará condições para serem avaliadas. O CreateTextAndCategoryRule cria uma regra que atribui categorias examinando o assunto para qualquer uma das condições da matriz usando a propriedade **texto** do objeto **TextRuleCondition** e a propriedade [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) do conjunto [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)). Se a condição é atendida, as categorias do Office e do Outlook são atribuídas para o item usando o método[AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) do objeto [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)).

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>Confira também

- [Regras](rules.md)

