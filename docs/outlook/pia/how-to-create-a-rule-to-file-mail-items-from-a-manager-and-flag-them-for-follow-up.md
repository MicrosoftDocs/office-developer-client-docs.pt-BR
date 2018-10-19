---
title: Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2fc6f5fe60b2f643590e8f7545804cf6d8a4c11c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405984"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a>Criar uma regra para itens de email do arquivo de um gerente e sinalizá-la para acompanhamento

Este exemplo mostra como configurar uma regra de itens de correio de arquivo do gerente do usuário e como sinalizar para acompanhamento.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo a seguir é um trecho da [Programação de Aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

As regras do Outlook podem operar tanto do lado do servidor quanto do cliente, dependendo do tipo de conta e regra. Há várias maneiras de implementar regras para aplicar nos seus próprios esquemas organizacionais quando estiver organizando itens na caixa de correio. Por exemplo, você pode criar uma hierarquia de subpastas que organiza emails não lidos e emails lidos pela área de assunto. Ou você pode criar uma hierarquia de subpastas que correspondem ao remetente da mensagem. Você pode também categorizar seus emails e usar pastas de pesquisa para agregar os emails por categoria.

O modelo de objeto **regras**, que inclui o objeto [regra](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) que representa uma regra no Outlook, permite que você crie regras para, programaticamente, impor um determinado esquema organizacional, para criar uma regra específica que é exclusiva para a sua solução ou para garantir que determinadas regras sejam implantadas para um grupo de usuários. Usando o modelo de objeto **regras**, você pode, programaticamente, adicionar, editar e excluir regras. Usando o conjunto[regras](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) e o objeto **regra**, você também pode acessar, adicionar e excluir regras definidas para uma sessão. 

O objeto **regra** tem a propriedade [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)), que indica se a regra é uma regra de envio ou recebimento. Quando uma regra é criada, a propriedade **RuleType** é especificada e não pode ser alterada sem excluir e recriar a regra com uma propriedade **RuleType** diferente. Os objetos [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) e [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) e seus conjuntos de objetos, ações derivadas e objetos de condição também são usados para mais suporte ao editar ações de regras e condições da regra.

O modelo de objeto **regras** não dá suporte a todas as regras criadas por você, usando o Assistente de Alerta e Regras na interface de usuário do Outlook, mas ele dá suporte às regras de ações e condições mais comuns. Quaisquer regras criadas usando o Assistente de Alertas e Regras que são aplicadas às mensagens, o que inclui itens de email, solicitações de reunião, solicitações de tarefas, documentos, confirmações de entrega, recibos de leitura, respostas de votação e notificações de ausência temporária, também podem ser criadas de forma programática.

Uma regra pode ser executada no servidor Exchange ou no cliente do Outlook, desde que a caixa de correio do usuário esteja hospedada em um servidor Exchange. A propriedade [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) do objeto **regra** retorna **verdadeiro** para indicar que a regra é executada no cliente, e o Outlook deve estar em execução para essa regra ser executada. Se a regra for executada no servidor, o Outlook não precisará executar as condições da regra para que haja avaliação e para que as ações de regra sejam concluídas.

> [!NOTE]
> Não existe uma coleção separada que represente condições de exceções da regra. Use a propriedade [Exceções](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) do objeto **Regra** para obter uma coleção [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) que represente condições de exceções da regra.

Para criar regras pelo modelo de objeto do Outlook, siga estas etapas:

1.  Obtenha o conjunto **regras** a partir da propriedade [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)), chamando o método[GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) no objeto padrão[Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)). Use um bloqueio **try...catch** para o caso de o usuário estar offline ou desconectado do servidor Exchange. Isso impede que o Outlook gere um erro.

2.  Chame o método [criar (cadeia de caracteres, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) no objeto **regras** para criar uma instância variável ou objeto **regra**, especificando um nome e um parâmetro [ OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).

3.  Use as coleções [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) e [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) para habilitar exceções, condições e ações no objeto **regra**. Observe que qualquer condição habilitada no conjunto retornado **RuleConditions** pela propriedade [exceções](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) será tratada como uma exceção à condição de regra, e outras ações personalizadas internas ou condições não poderão ser adicionadas à coleção.

4.  Configure a propriedade [habilitada](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) como **verdadeira** para que cada regra de ação, condição ou exceção sejam operacionais. Algumas ações ou condições, assim como a propriedade [pasta](https://msdn.microsoft.com/library/bb646755\(v=office.15\)), exigem que você defina propriedades adicionais na ação ou na condição para salvar o objeto **regra** sem um erro.

5.  Por fim, chame o método [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) no conjunto **regras** para salvar regras criadas ou modificadas. Coloque o método **Salvar** em um bloqueio **try...catch ** para lidar com exceções.

No exemplo de código a seguir, o CreateManagerRule implementa as etapas descritas anteriormente. O CreateManagerRule primeiro verifica se a propriedade [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) representa um objeto [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), indicando que o usuário atual é um usuário do Exchange. Se o usuário atual for um usuário do Exchange, o CreateManagerRule terá acesso ao gerente do usuário atual, chamando o método [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) no objeto **ExchangeUser** da propriedade ** CurrentUser** do objeto **NameSpace**. Uma regra de recebimento é criada, em seguida, para mover as mensagens recebidas para uma subpasta da Caixa de Entrada nas seguintes condições:

- A mensagem é do gerente do usuário.

- O destinatário está na linha **Para:** da mensagem.

- A mensagem não é uma solicitação de reunião ou atualização.

Por fim, a mensagem está sinalizada para acompanhamento hoje. O CreateManagerRule também ilustra o tratamento apropriado de erro para condições que podem gerar uma exceção, como quando o usuário está offline ou desconectado no modo cache do Exchange.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Regras](rules.md)

