---
title: Criar uma regra para atribuir categorias a itens de email com base em várias palavras utilizadas no assunto
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1ff096454aa15a0a45c423913140eb50e6de9678
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406320"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a><span data-ttu-id="a25d8-102">Criar uma regra para atribuir categorias a itens de email com base em várias palavras utilizadas no assunto</span><span class="sxs-lookup"><span data-stu-id="a25d8-102">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>

<span data-ttu-id="a25d8-103">Este exemplo mostra como configurar uma regra que atribua categorias a itens de email com base em várias palavras no assunto.</span><span class="sxs-lookup"><span data-stu-id="a25d8-103">This example shows how to set up a rule that assigns categories to mail items based on multiple words in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="a25d8-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a25d8-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a25d8-105">O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a25d8-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="a25d8-106">No Outlook, os itens podem ser categorizados para exibição e a organização mais fáceis.</span><span class="sxs-lookup"><span data-stu-id="a25d8-106">In Outlook, items can be categorized for easier organization and display.</span></span> <span data-ttu-id="a25d8-107">O modelo de objeto do Outlook fornece o objeto [categoria](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) e o conjunto [categorias](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) representam categorias.</span><span class="sxs-lookup"><span data-stu-id="a25d8-107">The Outlook object model provides the [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object and the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection to represent categories.</span></span> <span data-ttu-id="a25d8-108">Para saber mais sobre o objeto **categoria** e o conjunto**categorias**de um item do Outlook, confira [enumerar e adicionar categorias](how-to-enumerate-and-add-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a25d8-108">For more information about the **Category** object and the **Categories** collection for an Outlook item, see [Enumerate and Add Categories](how-to-enumerate-and-add-categories.md).</span></span>

<span data-ttu-id="a25d8-109">Uma regra, representada pelo objeto [regra](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), pode ser atribuída com várias condições.</span><span class="sxs-lookup"><span data-stu-id="a25d8-109">A rule, represented by a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object, can be assigned with multiple conditions.</span></span> <span data-ttu-id="a25d8-110">Você pode começar ou definir uma matriz que represente as condições avaliadas ou as ações a serem concluídas.</span><span class="sxs-lookup"><span data-stu-id="a25d8-110">You can get or set an array that represents conditions to be evaluated or actions to be completed.</span></span> <span data-ttu-id="a25d8-111">Por exemplo, a propriedade[texto](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) do objeto[TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) retorna ou reúne uma matriz de elementos da cadeia de caracteres que representa o texto a ser avaliado pela condição de regra.</span><span class="sxs-lookup"><span data-stu-id="a25d8-111">For example, the [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) property of the [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) object returns or sets an array of string elements that represents the text to be evaluated by the rule condition.</span></span> <span data-ttu-id="a25d8-112">Você pode atribuir uma matriz com uma ou várias sequências de caracteres para avaliação.</span><span class="sxs-lookup"><span data-stu-id="a25d8-112">You can assign an array with one string or multiple strings for evaluation.</span></span> <span data-ttu-id="a25d8-113">Para avaliar várias cadeias de caracteres que estejam atribuídas a uma matriz, use a operação OU lógico.</span><span class="sxs-lookup"><span data-stu-id="a25d8-113">To evaluate multiple text strings that are assigned in an array, use the logical OR operation.</span></span> 

<span data-ttu-id="a25d8-114">As propriedades que você pode usar para acessar ou definir uma matriz são as seguintes: [endereço](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [categorias](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [categorias](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [nome do formulário](https://msdn.microsoft.com/library/bb647042\(v=office.15\))e **TextRuleCondition.Text**.</span><span class="sxs-lookup"><span data-stu-id="a25d8-114">The properties that you can use to get or set an array are as follows: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)), and **TextRuleCondition.Text**.</span></span> <span data-ttu-id="a25d8-115">Para saber mais sobre regras, confira [criar uma regra para itens de Email do arquivo de um gerente e sinalize-a para acompanhamento](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="a25d8-115">For more information about rules, see [Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span>

<span data-ttu-id="a25d8-116">No exemplo a seguir o CreateTextAndCategoryRule usa o método CategoryExists para verificar os itens de email do usuário para qualquer categoria pelo nome "Office" ou "Outlook" no conjunto **categorias**.</span><span class="sxs-lookup"><span data-stu-id="a25d8-116">In the following example, CreateTextAndCategoryRule uses the CategoryExists method to check the user’s mail items for any categories by the name “Office” or “Outlook” in the **Categories** collection.</span></span> <span data-ttu-id="a25d8-117">Se nenhuma categoria for encontrada, eles serão adicionados.</span><span class="sxs-lookup"><span data-stu-id="a25d8-117">If no categories are found, they are added.</span></span> <span data-ttu-id="a25d8-118">O exemplo em seguida cria uma matriz de cadeias de caracteres que incluem "Office","Outlook" e "2007".</span><span class="sxs-lookup"><span data-stu-id="a25d8-118">The example then creates an array of strings that include “Office, “Outlook”, and “2007”.</span></span> <span data-ttu-id="a25d8-119">Essa matriz representará condições para serem avaliadas.</span><span class="sxs-lookup"><span data-stu-id="a25d8-119">This array will represent the conditions to be evaluated.</span></span> <span data-ttu-id="a25d8-120">O CreateTextAndCategoryRule cria uma regra que atribui categorias examinando o assunto para qualquer uma das condições da matriz usando a propriedade **texto** do objeto **TextRuleCondition** e a propriedade[BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) do conjunto [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a25d8-120">CreateTextAndCategoryRule then creates a rule that assigns categories by examining the subject for any of the conditions in the array by using the **Text** property of the **TextRuleCondition** object and the [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) property of the [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collection.</span></span> <span data-ttu-id="a25d8-121">Se a condição é atendida, as categorias do Office e do Outlook são atribuídas para o item usando o método[AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) do objeto [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="a25d8-121">If the condition is satisfied, the categories of Office and Outlook are assigned to the item by using the [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) method of the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) object.</span></span>

<span data-ttu-id="a25d8-122">Se você usar o Visual Studio para testar este exemplo de código, primeiro você deve adicionar uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável Outlook quando você importa a namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a25d8-122">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="a25d8-123">A instrução**usando** não deve se situar antes de funções no exemplo de código mas deve ser adicionada antes da declaração classe pública.</span><span class="sxs-lookup"><span data-stu-id="a25d8-123">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a25d8-124">A seguinte linha de código mostra como fazer a importação e de tarefa em C\#.</span><span class="sxs-lookup"><span data-stu-id="a25d8-124">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="a25d8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a25d8-125">See also</span></span>

- [<span data-ttu-id="a25d8-126">Regras</span><span class="sxs-lookup"><span data-stu-id="a25d8-126">Rules</span></span>](rules.md)

