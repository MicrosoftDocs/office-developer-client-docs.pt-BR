---
title: Ação da macro EncontrarRegistro
TOCTitle: FindRecord macro action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 086993095daef3ff4ad87aed9f572a09124a9d31
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709968"
---
# <a name="findrecord-macro-action"></a><span data-ttu-id="0e9e9-102">Ação da macro EncontrarRegistro</span><span class="sxs-lookup"><span data-stu-id="0e9e9-102">FindRecord macro action</span></span>

<span data-ttu-id="0e9e9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e9e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e9e9-p101">Você pode usar a ação **EncontrarRegistro** para localizar a primeira instância de dados que atende aos critérios especificados pelos argumentos **EncontrarRegistro**. Esses dados podem estar no registro atual, em um registro sucessivo ou anterior, ou no primeiro registro. Você pode localizar registros na folha de dados da tabela ativa, na folha de dados de consulta ou no formulário.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p101">You can use the **FindRecord** action to find the first instance of data that meets the criteria specified by the **FindRecord** arguments. This data can be in the current record, in a succeeding or prior record, or in the first record. You can find records in the active table datasheet, query datasheet, form datasheet, or form.</span></span>

## <a name="setting"></a><span data-ttu-id="0e9e9-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="0e9e9-107">Setting</span></span>

<span data-ttu-id="0e9e9-108">A ação **EncontrarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-108">The **FindRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e9e9-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="0e9e9-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0e9e9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e9e9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e9e9-111"><strong>Localizar</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-111"><strong>Find What</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-112">Especifica os dados que você deseja localizar no registro.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-112">Specifies the data you want to find in the record.</span></span> <span data-ttu-id="0e9e9-113">Insira o texto, número ou data que você deseja localizar ou digite uma expressão, que é precedida por um sinal de igualdade (<strong>=</strong>), na caixa <strong>Localizar</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-113">Enter the text, number, or date you want to find or type an expression, which is preceded by an equal sign (<strong>=</strong>), in the <strong>Find What</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="0e9e9-114">Você pode usar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-114">You can use wildcard characters.</span></span> <span data-ttu-id="0e9e9-115">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9e9-116"><strong>Match</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-116"><strong>Match</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-p103">Especifica onde os dados estão localizados no campo. Você pode especificar uma pesquisa dos: dados em qualquer parte do campo (<strong>Qualquer Parte do Campo</strong>); dados que preenchem o campo inteiro (<strong>Campo Inteiro</strong>); ou dados localizados no início do campo (<strong>Início do Campo</strong>). O padrão é <strong>Campo Inteiro</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p103">Specifies where the data is located in the field. You can specify a search for data in any part of the field (<strong>Any Part of Field</strong>), for data that fills the entire field (<strong>Whole Field</strong>), or for data located at the beginning of the field (<strong>Start of Field</strong>). The default is <strong>Whole Field</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9e9-120"><strong>Diferenciar Maiúsc. de Minúsc.</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-120"><strong>Match Case</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-p104">Especifica se a pesquisa diferencia maiúsculas de minúsculas. Clique em <strong>Sim</strong> (conduzir uma pesquisa com diferenciação de maiúsculas e minúsculas) ou <strong>Não</strong> (pesquisar sem fazer coincidir exatamente as letras maiúsculas e minúsculas). O padrão é <strong>Não</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p104">Specifies whether the search is case-sensitive. Click <strong>Yes</strong> (conduct a case-sensitive search) or <strong>No</strong> (search without matching uppercase and lowercase letters exactly). The default is <strong>No</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9e9-124"><strong>Search</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-124"><strong>Search</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-p105">Especifica se a pesquisa continua partindo do registro atual e sobe até o início dos registros (<strong>Acima</strong>); desce até o final dos registros (<strong>Abaixo</strong>); ou desce até o final dos registros e partindo do início dos registros até o registro atual, para que todos os registros sejam pesquisados (<strong>Todos</strong>). O padrão é <strong>Tudo</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p105">Specifies whether the search proceeds from the current record up to the beginning of the records (<strong>Up</strong>); down to the end of the records (<strong>Down</strong>); or down to the end of the records and then from the beginning of the records to the current record, so all records are searched (<strong>All</strong>). The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9e9-127"><strong>Pesquisar como Formatado</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-127"><strong>Search As Formatted</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-128">Especifica se a pesquisa inclui dados formatados.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-128">Specifies whether the search includes formatted data.</span></span> <span data-ttu-id="0e9e9-129">Clique em <strong>Sim</strong> (Microsoft Office Access 2007 procurará os dados como é exibido no campo e formatado) ou <strong>não</strong> (Access procura os dados como ele está armazenado no banco de dados, não é sempre o mesmo como ele é exibido).</span><span class="sxs-lookup"><span data-stu-id="0e9e9-129">Click <strong>Yes</strong> (Microsoft Office Access 2007 searches for the data as it is formatted and displayed in the field) or <strong>No</strong> (Access searches for the data as it is stored in the database, which isn't always the same as it's displayed).</span></span> <span data-ttu-id="0e9e9-130">O padrão é <strong>Não</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-130">The default is <strong>No</strong>.</span></span> <span data-ttu-id="0e9e9-131">Você pode usar esse recurso para restringir a pesquisa aos dados em um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-131">You can use this feature to restrict the search to data in a particular format.</span></span> <span data-ttu-id="0e9e9-132">Por exemplo, clique em <strong>Sim</strong> e digite <strong>1.234</strong> no argumento <strong>Localizar</strong> para localizar um valor 1.234 em um campo formatado para incluir vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-132">For example, click <strong>Yes</strong> and type <strong>1,234</strong> in the <strong>Find What</strong> argument to find a value of 1,234 in a field formatted to include commas.</span></span> <span data-ttu-id="0e9e9-133">Clique em <strong>não</strong> se você quiser digitar <strong>1234</strong> para pesquisar os dados nesse campo.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-133">Click <strong>No</strong> if you want to type <strong>1234</strong> to search for the data in this field.</span></span> <span data-ttu-id="0e9e9-134">Para pesquisar datas, clique em <strong>Sim</strong> para localizar uma data exatamente como ela está formatada, como 08 de julho de 2003.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-134">To search for dates, click <strong>Yes</strong> to find a date exactly as it is formatted, such as 08-July-2003.</span></span> <span data-ttu-id="0e9e9-135">Se você clicar em <strong>não</strong>, digite a data para o argumento <strong>Localizar</strong> no formato definido nas configurações regionais no painel de controle do Windows.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-135">If you click <strong>No</strong>, enter the date for the <strong>Find What</strong> argument in the format that is set in the regional settings in Windows Control Panel.</span></span> <span data-ttu-id="0e9e9-136">Esse formato é mostrado na caixa <strong>formato de data curta</strong> encontrada na guia <strong>Data</strong> nas configurações regionais.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-136">This format is shown in the <strong>Short date format</strong> box found on the <strong>Date</strong> tab in the regional settings.</span></span> <span data-ttu-id="0e9e9-137">Por exemplo, se a caixa de <strong>formato de data curta</strong> estiver definida como <strong>m/aa</strong>, você pode inserir 7/8/03 e Access irá localizar todas as entradas em um campo de data que correspondem à 8 de julho de 2003, independentemente de como esse campo é formatado.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-137">For example, if the <strong>Short date format</strong> box is set to <strong>M/d/yy</strong>, you can enter 7/8/03, and Access will find all entries in a Date field that correspond to July 8, 2003, regardless of how this field is formatted.</span></span></p>
<p><span data-ttu-id="0e9e9-138"><strong>Observação</strong>: O argumento <strong>Pesquisar como formatado</strong> entrará em vigor somente se o campo atual for um controle acoplado, o argumento <strong>Coincidir</strong> estiver definido como <strong>Campo inteiro</strong>, o argumento <strong>Somente campo atual</strong> será definido como <strong>Sim</strong>e a correspondência de <strong> Caso</strong> argumento estiver definido como <strong>não</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-138"><strong>NOTE</strong>: The <strong>Search As Formatted</strong> argument takes effect only if the current field is a bound control, the <strong>Match</strong> argument is set to <strong>Whole Field</strong>, the <strong>Only Current Field</strong> argument is set to <strong>Yes</strong>, and the <strong>Match Case</strong> argument is set to <strong>No</strong>.</span></span></p>
<p><span data-ttu-id="0e9e9-139">Se você definiu <strong>Diferenciar Maiúsc. de Minúsc.</strong> como <strong>Sim</strong>, ou <strong>Somente Campo Atual</strong> como <strong>Não</strong>, também precisará definir <strong>Pesquisar como Formatado</strong> como <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-139">If you set <strong>Match Case</strong> to <strong>Yes</strong> or <strong>Only Current Field</strong> to <strong>No</strong>, you must also set <strong>Search As Formatted</strong> to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e9e9-140"><strong>Somente Campo Atual</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-140"><strong>Only Current Field</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-p107">Especifica se a pesquisa está confinada no campo atual em cada registro ou se inclui todos os campos de cada registro. A pesquisa no campo atual é mais rápida. Clique em <strong>Sim</strong> (confinar a pesquisa no campo atual) ou <strong>Não</strong> (pesquisar em todos os campos de cada registro). O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p107">Specifies whether the search is confined to the current field in each record or includes all fields in each record. Searching in the current field is faster. Click <strong>Yes</strong> (confine the search to the current field) or <strong>No</strong> (search in all fields in each record). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e9e9-145"><strong>Localizar Primeiro</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-145"><strong>Find First</strong></span></span></p></td>
<td><p><span data-ttu-id="0e9e9-p108">Especifica se a pesquisa começa no primeiro registro ou no atual. Clique em <strong>Sim</strong> (começar no primeiro registro) ou <strong>Não</strong> (começar no registro atual). O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p108">Specifies whether the search starts at the first record or at the current record. Click <strong>Yes</strong> (start at the first record) or <strong>No</strong> (start at the current record). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e9e9-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e9e9-149">Remarks</span></span>

<span data-ttu-id="0e9e9-p109">Quando uma macro é executada na ação **EncontrarRegistro**, o Access pesquisa os dados especificados nos registros (a ordem da pesquisa é determinada pela configuração do argumento **Pesquisar** ). Quando o Access localiza os dados especificados, eles são selecionados no registro.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p109">When a macro runs the **FindRecord** action, Access searches for the specified data in the records (the order of the search is determined by the setting of the **Search** argument). When Access finds the specified data, the data is selected in the record.</span></span>

<span data-ttu-id="0e9e9-p110">A ação **EncontrarRegistro** equivale a clicar em **Localizar** na guia **Página Inicial**, e seus argumentos são os mesmos das opções na caixa de diálogo **Localizar e Substituir**. Se você definir os argumentos **EncontrarRegistro** no painel Construtor de Macros e executar a macro, verá as opções correspondentes selecionadas na caixa de diálogo **Localizar e Substituir** ao clicar em **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p110">The **FindRecord** action is equivalent to clicking **Find** on the **Home** tab, and its arguments are the same as the options in the **Find and Replace** dialog box. If you set the **FindRecord** arguments in the Macro Builder pane and then run the macro, you will see the corresponding options selected in the **Find and Replace** dialog box when you click **Find**.</span></span>

<span data-ttu-id="0e9e9-p111">O Access retém os argumentos **EncontrarRegistro** mais recentes durante uma sessão de banco de dados para que não seja necessário inserir os mesmos critérios várias vezes à medida que são executadas operações subsequentes com a ação **EncontrarRegistro**. Se você deixar um argumento em branco, o Access usará a configuração mais recente do argumento, conforme definida por uma ação **EncontrarRegistro** anterior ou na caixa de diálogo **Localizar e Substituir**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p111">Access retains the most recent **FindRecord** arguments during a database session so that you don't need to enter the same criteria repeatedly as you perform subsequent operations with the **FindRecord** action. If you leave an argument blank, Access uses the most recent setting for the argument, as set either by a previous **FindRecord** action or in the **Find and Replace** dialog box.</span></span>

<span data-ttu-id="0e9e9-156">Quando você deseja localizar um registro usando uma macro, use a ação **EncontrarRegistro**, e não a ação **ExecutarComandodeMenu** com o respectivo argumento definido para executar o comando **Localizar**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-156">When you want to find a record by using a macro, use the **FindRecord** action, not the **RunMenuCommand** action with its argument set to run the **Find** command.</span></span>

> [!NOTE]
> <span data-ttu-id="0e9e9-p112">[!OBSERVAçãO] Embora a ação **EncontrarRegistro** corresponda ao comando **Localizar** na guia **Página Inicial** para tabelas, consultas e formulários, ela não corresponde ao comando **Localizar** no menu **Editar** da janela Código. Não é possível usar a ação **EncontrarRegistro** para pesquisar texto em módulos.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p112">While the **FindRecord** action corresponds to the **Find** command on the **Home** tab for tables, queries, and forms, it doesn't correspond to the **Find** command on the **Edit** menu in the Code window. You can't use the **FindRecord** action to search for text in modules.</span></span>

<span data-ttu-id="0e9e9-p113">Se o texto selecionado no momento for o mesmo do texto de pesquisa quando a ação **EncontrarRegistro** for executada, a pesquisa começará imediatamente após a seleção, no mesmo campo da seleção e no mesmo registro. Caso contrário, começará no início do registro atual. Isso permite localizar várias instâncias dos mesmos critérios de pesquisa que podem aparecer em um único registro.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p113">If the currently selected text is the same as the search text at the time the **FindRecord** action is carried out, the search begins immediately following the selection in the same field as the selection, and in the same record. Otherwise, the search begins at the start of the current record. This enables you to find multiple instances of the same search criteria that might appear in a single record.</span></span>

<span data-ttu-id="0e9e9-p114">Entretanto, observe que, se você usar um botão de comando para executar uma macro que contém a ação **EncontrarRegistro**, a primeira instância dos critérios de pesquisa será localizada várias vezes. Esse comportamento ocorre porque clicar no botão de comando remove o foco do campo que contém o valor correspondente. A ação **EncontrarRegistro** começará a pesquisar partindo do início do registro. Para evitar esse problema, execute a macro usando uma técnica que não altera o foco, como um botão de barra de ferramentas personalizado ou uma combinação de teclas definida em uma macro AutoKeys. Ou então, defina o foco na macro para o campo que contém os critérios de pesquisa antes de executar a ação **EncontrarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p114">However, note that if you use a command button to run a macro containing the **FindRecord** action, the first instance of the search criteria will be found repeatedly. This behavior occurs because clicking the command button removes the focus from the field containing the matching value. The **FindRecord** action will then begin searching from the start of the record. To avoid this problem, run the macro by using a technique that doesn't change the focus, such as a custom toolbar button or a key combination defined in an AutoKeys macro, or set the focus in the macro to the field containing the search criteria before you carry out the **FindRecord** action.</span></span>

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Observação sobre segurança" alt="Security note" /><span data-ttu-id="0e9e9-167"><strong>Observação de segurança</strong></span><span class="sxs-lookup"><span data-stu-id="0e9e9-167"><strong>Security Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e9e9-p115">
      Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.
</span><span class="sxs-lookup"><span data-stu-id="0e9e9-p115">Avoid using the <strong>SendKeys</strong> statement or an AutoKeys macro with sensitive or confidential information. A malicious user could intercept the keystrokes and compromise the security of your computer and data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0e9e9-170">O mesmo comportamento também ocorre se você usa um botão de comando para executar uma macro que contém a ação **EncontrarPróximo**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-170">The same behavior also occurs if you use a command button to run a macro containing the **FindNext** action.</span></span>

<span data-ttu-id="0e9e9-171">Para executar a ação **EncontrarRegistro** em um módulo do VBA (Visual Basic for Applications), use o método **FindRecord** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-171">To run the **FindRecord** action in a Visual Basic for Applications (VBA) module, use the **FindRecord** method of the **DoCmd** object.</span></span>

<span data-ttu-id="0e9e9-172">Para pesquisas mais complexas, convém usar a ação de macro **ProcurarRegistro**.</span><span class="sxs-lookup"><span data-stu-id="0e9e9-172">For more complex searches, you may want to use the **SearchForRecord** macro action.</span></span>

