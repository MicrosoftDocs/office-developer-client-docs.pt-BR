---
title: Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dba46c851050c3f948ec829ae2340e0492ca135f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713804"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a><span data-ttu-id="85cb6-102">Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento</span><span class="sxs-lookup"><span data-stu-id="85cb6-102">Create a rule to file mail items from a manager and flag them for follow-up</span></span>

<span data-ttu-id="85cb6-103">Este exemplo mostra como configurar uma regra de itens de correio de arquivo do gerente do usuário e como sinalizar para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="85cb6-103">This example shows how to set up a rule to file mail items from the user’s manager and flag them for follow up.</span></span>

## <a name="example"></a><span data-ttu-id="85cb6-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="85cb6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="85cb6-105">O exemplo a seguir é um trecho da [Programação de Aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="85cb6-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="85cb6-106">As regras do Outlook podem operar tanto do lado do servidor quanto do cliente, dependendo do tipo de conta e regra.</span><span class="sxs-lookup"><span data-stu-id="85cb6-106">Outlook rules can operate either server-side or client-side, depending on the type of account and rule.</span></span> <span data-ttu-id="85cb6-107">Há várias maneiras de implementar regras para aplicar nos seus próprios esquemas organizacionais quando estiver organizando itens na caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="85cb6-107">There are many ways you can implement rules to enforce your own organizational schemes when you organize items in your mailbox.</span></span> <span data-ttu-id="85cb6-108">Por exemplo, você pode criar uma hierarquia de subpastas que organiza emails não lidos e emails lidos pela área de assunto.</span><span class="sxs-lookup"><span data-stu-id="85cb6-108">For example, you can create a subfolder hierarchy that organizes unread mail and read mail by subject area.</span></span> <span data-ttu-id="85cb6-109">Ou você pode criar uma hierarquia de subpastas que correspondem ao remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="85cb6-109">Or, you can create a subfolder hierarchy that corresponds to the sender of the message.</span></span> <span data-ttu-id="85cb6-110">Você pode também categorizar seus emails e usar pastas de pesquisa para agregar os emails por categoria.</span><span class="sxs-lookup"><span data-stu-id="85cb6-110">You can also categorize your mail and then use search folders to aggregate the mail by category.</span></span>

<span data-ttu-id="85cb6-111">O modelo de objeto **regras**, que inclui o objeto [regra](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) que representa uma regra no Outlook, permite que você crie regras para, programaticamente, impor um determinado esquema organizacional, para criar uma regra específica que é exclusiva para a sua solução ou para garantir que determinadas regras sejam implantadas para um grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="85cb6-111">The **Rules** object model, which includes a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object that represents a rule in Outlook, allows you to create rules programmatically to enforce a certain organizational scheme, create a specific rule that is unique to your solution, or ensure that certain rules are deployed to a group of users.</span></span> <span data-ttu-id="85cb6-112">Usando o modelo de objeto **regras**, você pode, programaticamente, adicionar, editar e excluir regras.</span><span class="sxs-lookup"><span data-stu-id="85cb6-112">By using the **Rules** object model, you can programmatically add, edit, and delete rules.</span></span> <span data-ttu-id="85cb6-113">Usando o conjunto[regras](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) e o objeto **regra**, você também pode acessar, adicionar e excluir regras definidas para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="85cb6-113">By using the [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) collection and the **Rule** object, you can also access, add, and delete rules defined for a session.</span></span> 

<span data-ttu-id="85cb6-114">O objeto **regra** tem a propriedade [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)), que indica se a regra é uma regra de envio ou recebimento.</span><span class="sxs-lookup"><span data-stu-id="85cb6-114">A **Rule** object has a [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) property that indicates whether the rule is a send or receive rule.</span></span> <span data-ttu-id="85cb6-115">Quando uma regra é criada, a propriedade **RuleType** é especificada e não pode ser alterada sem excluir e recriar a regra com uma propriedade **RuleType** diferente.</span><span class="sxs-lookup"><span data-stu-id="85cb6-115">When a rule is created, the **RuleType** property is specified, and cannot be changed without deleting and re-creating the rule with a different **RuleType** property.</span></span> <span data-ttu-id="85cb6-116">Os objetos [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) e [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) e seus conjuntos de objetos, ações derivadas e objetos de condição também são usados para mais suporte ao editar ações de regras e condições da regra.</span><span class="sxs-lookup"><span data-stu-id="85cb6-116">The [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) and [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) objects, their collection objects, and derived action and condition objects are also used to further support editing rule actions and rule conditions.</span></span>

<span data-ttu-id="85cb6-117">O modelo de objeto **regras** não dá suporte a todas as regras criadas por você, usando o Assistente de Alerta e Regras na interface de usuário do Outlook, mas ele dá suporte às regras de ações e condições mais comuns.</span><span class="sxs-lookup"><span data-stu-id="85cb6-117">The **Rules** object model does not support all rules that you can create by using the Rules and Alert Wizard in the Outlook user interface, but it supports the most commonly used rule actions and conditions.</span></span> <span data-ttu-id="85cb6-118">Quaisquer regras criadas usando o Assistente de Alertas e Regras que são aplicadas às mensagens, o que inclui itens de email, solicitações de reunião, solicitações de tarefas, documentos, confirmações de entrega, recibos de leitura, respostas de votação e notificações de ausência temporária, também podem ser criadas de forma programática.</span><span class="sxs-lookup"><span data-stu-id="85cb6-118">Any rules created by using the Rules and Alerts Wizard that are applied to messages, which include mail items, meeting requests, task requests, documents, delivery receipts, read receipts, voting responses, and out-of-office notices, can also be created programmatically.</span></span>

<span data-ttu-id="85cb6-119">Uma regra pode ser executada no servidor Exchange ou no cliente do Outlook, desde que a caixa de correio do usuário esteja hospedada em um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cb6-119">A rule can execute on the Exchange server or on the Outlook client, provided that the current user’s mailbox is hosted on an Exchange server.</span></span> <span data-ttu-id="85cb6-120">A propriedade [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) do objeto **regra** retorna **verdadeiro** para indicar que a regra é executada no cliente, e o Outlook deve estar em execução para essa regra ser executada.</span><span class="sxs-lookup"><span data-stu-id="85cb6-120">The [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the **Rule** object returns **true** to indicate that the rule executes on a client, and Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="85cb6-121">Se a regra for executada no servidor, o Outlook não precisará executar as condições da regra para que haja avaliação e para que as ações de regra sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="85cb6-121">If the rule executes on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span>

> [!NOTE]
> <span data-ttu-id="85cb6-122">Não existe uma coleção separada que represente condições de exceções da regra.</span><span class="sxs-lookup"><span data-stu-id="85cb6-122">There is no separate collection that represents rule exception conditions.</span></span> <span data-ttu-id="85cb6-123">Use a propriedade [Exceções](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) do objeto **Regra** para obter uma coleção [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) que represente condições de exceções da regra.</span><span class="sxs-lookup"><span data-stu-id="85cb6-123">Use the [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) property of the **Rule** object to get a [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) collection that represents rule exception conditions.</span></span>

<span data-ttu-id="85cb6-124">Para criar regras pelo modelo de objeto do Outlook, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="85cb6-124">To create rules through the Outlook object model, follow these steps:</span></span>

1.  <span data-ttu-id="85cb6-125">Obtenha o conjunto **regras** a partir da propriedade [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), chamando o método[GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) no objeto padrão[Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="85cb6-125">Get the **Rules** collection from the [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object by calling the [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) method on the default [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="85cb6-126">Use um bloqueio **try...catch** para o caso de o usuário estar offline ou desconectado do servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cb6-126">Use a **try…catch** block to account for the user being offline or disconnected from the Exchange server.</span></span> <span data-ttu-id="85cb6-127">Isso impede que o Outlook gere um erro.</span><span class="sxs-lookup"><span data-stu-id="85cb6-127">This prevents Outlook from raising an error.</span></span>

2.  <span data-ttu-id="85cb6-128">Chame o método [criar (cadeia de caracteres, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) no objeto **regras** para criar uma instância variável ou objeto **regra**, especificando um nome e um parâmetro [ OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="85cb6-128">Call the [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) method on the **Rules** object to create an instance variable or a **Rule** object, specifying a Name and a [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) parameter.</span></span>

3.  <span data-ttu-id="85cb6-129">Use as coleções [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) e [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) para habilitar exceções, condições e ações no objeto **regra**.</span><span class="sxs-lookup"><span data-stu-id="85cb6-129">Use the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) and [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collections to enable actions, conditions, and exceptions on the **Rule** object.</span></span> <span data-ttu-id="85cb6-130">Observe que qualquer condição habilitada no conjunto retornado **RuleConditions** pela propriedade [exceções](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) será tratada como uma exceção à condição de regra, e outras ações personalizadas internas ou condições não poderão ser adicionadas à coleção.</span><span class="sxs-lookup"><span data-stu-id="85cb6-130">Note that any condition enabled in the **RuleConditions** collection, returned by the [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) property, is treated as a rule exception condition, and additional built-in custom actions or conditions cannot be added to the collection.</span></span>

4.  <span data-ttu-id="85cb6-131">Configure a propriedade [habilitada](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) como **verdadeira** para que cada regra de ação, condição ou exceção sejam operacionais.</span><span class="sxs-lookup"><span data-stu-id="85cb6-131">Set the [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) property to **true** for any given rule action, condition, or exception to be operational.</span></span> <span data-ttu-id="85cb6-132">Algumas ações ou condições, assim como a propriedade [pasta](https://msdn.microsoft.com/library/bb646755\(v=office.15\)), exigem que você defina propriedades adicionais na ação ou na condição para salvar o objeto **regra** sem um erro.</span><span class="sxs-lookup"><span data-stu-id="85cb6-132">Some actions or conditions, such as the [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) property, require that you set additional properties on the action or condition to save the **Rule** object without an error.</span></span>

5.  <span data-ttu-id="85cb6-133">Por fim, chame o método [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) no conjunto **regras** para salvar regras criadas ou modificadas.</span><span class="sxs-lookup"><span data-stu-id="85cb6-133">Finally, call the [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) method on the **Rules** collection to save the created or modified rules.</span></span> <span data-ttu-id="85cb6-134">Coloque o método **Salvar** em um bloqueio \*\*try...catch \*\* para lidar com exceções.</span><span class="sxs-lookup"><span data-stu-id="85cb6-134">Enclose the **Save** method in a **try…catch** block to handle exceptions.</span></span>

<span data-ttu-id="85cb6-135">No exemplo de código a seguir, o CreateManagerRule implementa as etapas descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="85cb6-135">In the following code example, CreateManagerRule implements the steps previously described.</span></span> <span data-ttu-id="85cb6-136">O CreateManagerRule primeiro verifica se a propriedade [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) representa um objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), indicando que o usuário atual é um usuário do Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cb6-136">CreateManagerRule first verifies whether the [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) property represents an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, indicating that the current user is an Exchange user.</span></span> <span data-ttu-id="85cb6-137">Se o usuário atual for um usuário do Exchange, o CreateManagerRule terá acesso ao gerente do usuário atual, chamando o método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) no objeto **ExchangeUser** da propriedade \*\* CurrentUser\*\* do objeto **NameSpace**.</span><span class="sxs-lookup"><span data-stu-id="85cb6-137">If the current user is an Exchange user, CreateManagerRule gets the current user’s manager by calling the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method on the **ExchangeUser** object of the **CurrentUser** property of the **NameSpace** object.</span></span> <span data-ttu-id="85cb6-138">Uma regra de recebimento é criada, em seguida, para mover as mensagens recebidas para uma subpasta da Caixa de Entrada nas seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="85cb6-138">A receive rule is then created to move received messages to a subfolder of the Inbox for the following conditions:</span></span>

- <span data-ttu-id="85cb6-139">A mensagem é do gerente do usuário.</span><span class="sxs-lookup"><span data-stu-id="85cb6-139">The message is from the user’s manager.</span></span>

- <span data-ttu-id="85cb6-140">O destinatário está na linha **Para:** da mensagem.</span><span class="sxs-lookup"><span data-stu-id="85cb6-140">The recipient is on the **To:** line of the message.</span></span>

- <span data-ttu-id="85cb6-141">A mensagem não é uma solicitação de reunião ou atualização.</span><span class="sxs-lookup"><span data-stu-id="85cb6-141">The message is not a meeting request or update.</span></span>

<span data-ttu-id="85cb6-142">Por fim, a mensagem está sinalizada para acompanhamento hoje.</span><span class="sxs-lookup"><span data-stu-id="85cb6-142">Finally, the message is flagged for follow-up today.</span></span> <span data-ttu-id="85cb6-143">O CreateManagerRule também ilustra o tratamento apropriado de erro para condições que podem gerar uma exceção, como quando o usuário está offline ou desconectado no modo cache do Exchange.</span><span class="sxs-lookup"><span data-stu-id="85cb6-143">CreateManagerRule also illustrates appropriate error handling for conditions that could raise an exception such as the user being offline or disconnected in cached Exchange mode.</span></span>

<span data-ttu-id="85cb6-144">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="85cb6-144">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="85cb6-145">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="85cb6-145">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="85cb6-146">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="85cb6-146">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateManagerRule()
{
    Outlook.ExchangeUser manager;
    Outlook.Folder managerFolder;
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        Outlook.Rules rules;
        try
        {
            rules = Application.Session.DefaultStore.GetRules();
        }
        catch
        {
            Debug.WriteLine("Could not obtain rules collection.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            Outlook.Folders folders =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).Folders;
            try
            {
                managerFolder =
                    folders[displayName] as Outlook.Folder;
            }
            catch
            {
                managerFolder =
                    folders.Add(displayName, Type.Missing)
                    as Outlook.Folder;
            }
            Outlook.Rule rule = rules.Create(displayName,
                Outlook.OlRuleType.olRuleReceive);

            // Rule conditions
            // From condition
            rule.Conditions.From.Recipients.Add(
                manager.PrimarySmtpAddress);
            rule.Conditions.From.Recipients.ResolveAll();
            rule.Conditions.From.Enabled = true;

            // Sent only to me
            rule.Conditions.ToMe.Enabled = true;

            // Rule exceptions
            // Meeting invite or update
            rule.Exceptions.MeetingInviteOrUpdate.Enabled = true;

            // Rule actions
            // MarkAsTask action
            rule.Actions.MarkAsTask.MarkInterval =
                Outlook.OlMarkInterval.olMarkToday;
            rule.Actions.MarkAsTask.FlagTo = "Follow-up";
            rule.Actions.MarkAsTask.Enabled = true;

            // MoveToFolder action
            rule.Actions.MoveToFolder.Folder = managerFolder;
            rule.Actions.MoveToFolder.Enabled = true;
            try
            {
                rules.Save(true);
            }
            catch (Exception ex)
            {
                Debug.WriteLine(ex.Message);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="85cb6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="85cb6-147">See also</span></span>

- [<span data-ttu-id="85cb6-148">Regras</span><span class="sxs-lookup"><span data-stu-id="85cb6-148">Rules</span></span>](rules.md)

