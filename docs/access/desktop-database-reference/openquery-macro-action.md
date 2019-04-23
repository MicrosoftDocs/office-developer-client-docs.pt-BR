---
title: Ação da macro AbrirConsulta
TOCTitle: OpenQuery macro action
ms:assetid: 64bfce73-aeaf-9a78-895c-492e5da43ded
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195094(v=office.15)
ms:contentKeyID: 48545298
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89069
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3294efe5ea1ab0f82be19f5c64a51287cc4df9b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288340"
---
# <a name="openquery-macro-action"></a><span data-ttu-id="947f4-102">Ação da macro AbrirConsulta</span><span class="sxs-lookup"><span data-stu-id="947f4-102">OpenQuery macro action</span></span>

<span data-ttu-id="947f4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="947f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="947f4-p101">Você pode usar a ação **AbrirConsulta** para abrir uma consulta de seleção ou tabela de referência cruzada em modo Folha de Dados, modo Design ou Visualizar Impressão. Esta ação executa uma consulta de ação. Também é possível selecionar um modo de entrada de dados para a consulta.</span><span class="sxs-lookup"><span data-stu-id="947f4-p101">You can use the **OpenQuery** action to open a select or crosstab query in Datasheet view, Design view, or Print Preview. This action runs an action query. You can also select a data entry mode for the query.</span></span>

> [!NOTE]
> <span data-ttu-id="947f4-p102">[!OBSERVAçãO] Esta ação só está disponível no ambiente de banco de dados do Access (.mdb ou .accdb). Consulte as ações **AbrirModoDeExibição**, **AbrirProcedimentoArmazenado** ou **AbrirFunção** se estiver usando o ambiente de the projeto do Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="947f4-p102">This action is only available in the Access database environment (.mdb or .accdb). See the **OpenView**, **OpenStoredProcedure**, or **OpenFunction** actions if you are using the Access project environment (.adp).</span></span>

## <a name="setting"></a><span data-ttu-id="947f4-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="947f4-109">Setting</span></span>

<span data-ttu-id="947f4-110">A ação **AbrirConsulta** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="947f4-110">The **OpenQuery** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="947f4-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="947f4-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="947f4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="947f4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="947f4-113"><strong>Nome da Consulta</strong></span><span class="sxs-lookup"><span data-stu-id="947f4-113"><strong>Query Name</strong></span></span></p></td>
<td><p><span data-ttu-id="947f4-114">O nome da consulta que será aberta.</span><span class="sxs-lookup"><span data-stu-id="947f4-114">The name of the query to open.</span></span> <span data-ttu-id="947f4-115">A caixa <strong>nome da consulta</strong> na seção argumentos da <strong>ação</strong> do painel Construtor de macros mostra todas as consultas no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="947f4-115">The <strong>Query Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all queries in the current database.</span></span> <span data-ttu-id="947f4-116">Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirConsulta</strong> em um banco de dados biblioteca, o Microsoft Access procurará a consulta com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="947f4-116">This is a required argument.If you run a macro containing the <strong>OpenQuery</strong> action in a library database, Microsoft Access first looks for the query with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="947f4-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="947f4-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="947f4-p104">O modo de exibição no qual a consulta será aberta. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</span><span class="sxs-lookup"><span data-stu-id="947f4-p104">The view in which the query will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="947f4-121"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="947f4-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="947f4-p105">O modo de entrada de dados da consulta. Isso se aplica somente às consultas abertas em modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="947f4-p105">The data entry mode for the query. This applies only to queries opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="947f4-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="947f4-126">Remarks</span></span>

<span data-ttu-id="947f4-127">Se você usar **Folha de Dados** para o argumento **Modo de Exibição**, o Access exibirá o conjunto de resultados se a consulta for uma consulta de seleção, tabela de referência cruzada, união ou passagem cuja propriedade **RetornarRegistros** esteja definida como **Sim**; e executará a consulta se for uma consulta de ação, definição de dados ou passagem cuja propriedade **RetornarRegistros** esteja definida como **Não**.</span><span class="sxs-lookup"><span data-stu-id="947f4-127">If you use **Datasheet** for the **View** argument, Access displays the result set if the query is a select, crosstab, union, or pass-through query whose **ReturnsRecords** property is set to **Yes**; and it runs the query if it is an action, data-definition, or pass-through query whose **ReturnsRecords** property is set to **No**.</span></span>

<span data-ttu-id="947f4-p106">A ação **AbrirConsulta** é semelhante a clicar duas vezes na consulta do Painel de Navegação ou a clicar com o botão direito do mouse na consulta do Painel de Navegação e selecionar um modo de exibição. Com esta ação, é possível selecionar outras opções.</span><span class="sxs-lookup"><span data-stu-id="947f4-p106">The **OpenQuery** action is similar to double-clicking the query in the Navigation Pane, or right-clicking the query in the Navigation Pane and selecting a view. With this action you can select additional options.</span></span>

> [!TIP]
> - <span data-ttu-id="947f4-p107">Você pode arrastar uma consulta do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirConsulta** que abre a consulta em modo Folha de Dados. Alternar para o modo Design enquanto a consulta é aberta remove a configuração do argumento **Modo de Dados** da consulta. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="947f4-p107">You can drag a query from the Navigation Pane to a macro action row. This automatically creates an **OpenQuery** action that opens the query in Datasheet view. Switching to Design view while the query is open removes the **Data Mode** argument setting for the query. This setting isn't in effect even if the user returns to Datasheet view.</span></span>
> - <span data-ttu-id="947f4-134">Se você não desejar exibir as mensagens de sistema que normalmente aparecem quando uma consulta de ação é executada (indicando que é uma consulta de ação e mostrando quantos registros serão afetados), poderá usar a ação **DefinirAvisos** para suprimir a exibição dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="947f4-134">If you don't want to display the system messages that normally appear when an action query is run (indicating it is an action query and showing how many records will be affected), you can use the **SetWarnings** action to suppress the display of these messages.</span></span>

<span data-ttu-id="947f4-135">Para executar a ação **AbrirConsulta** em um módulo do VBA (Visual Basic for Applications), use o método **OpenQuery** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="947f4-135">To run the **OpenQuery** action in a Visual Basic for Applications (VBA) module, use the **OpenQuery** method of the **DoCmd** object.</span></span>

