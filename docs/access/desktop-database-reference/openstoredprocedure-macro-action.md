---
title: Ação da macro AbrirProcedimentoArmazenado
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b972174e4fe7f3c0384b7483e17eb5ceb9e8bc15
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698768"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="b0af9-102">Ação da macro AbrirProcedimentoArmazenado</span><span class="sxs-lookup"><span data-stu-id="b0af9-102">OpenStoredProcedure macro action</span></span>

<span data-ttu-id="b0af9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0af9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0af9-p101">Em um projeto do Access, você pode usar a ação **AbrirProcedimentoArmazenado** para abrir um procedimento armazenado em modo Folha de Dados, em modo Design de procedimento armazenado ou Visualizar Impressão. Esta ação executa o procedimento armazenado nomeado quando aberta em modo Folha de Dados. Você pode selecionar o modo de entrada de dados do procedimento armazenado e restringir os registros exibidos pelo procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="b0af9-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>

> [!NOTE]
> <span data-ttu-id="b0af9-107">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="b0af9-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b0af9-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="b0af9-108">Setting</span></span>

<span data-ttu-id="b0af9-109">A ação **AbrirProcedimentoArmazenado** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b0af9-109">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0af9-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="b0af9-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b0af9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0af9-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0af9-112"><strong>Nome do Procedimento</strong></span><span class="sxs-lookup"><span data-stu-id="b0af9-112"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b0af9-113">O nome do procedimento armazenado para abrir.</span><span class="sxs-lookup"><span data-stu-id="b0af9-113">The name of the stored procedure to open.</span></span> <span data-ttu-id="b0af9-114">A caixa <strong>Nome do procedimento</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os procedimentos armazenados no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="b0af9-114">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="b0af9-115">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="b0af9-115">This is a required argument.</span></span> <span data-ttu-id="b0af9-116">Se você executar uma macro que contém a ação <strong>AbrirProcedimentoArmazenado</strong> em um banco de dados biblioteca, o Microsoft Access procurará o procedimento armazenado com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="b0af9-116">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0af9-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="b0af9-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="b0af9-p103">O modo de exibição no qual o procedimento armazenado será aberto. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0af9-p103">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0af9-121"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="b0af9-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b0af9-p104">O modo de entrada de dados do procedimento armazenado. Isso se aplica somente a procedimentos armazenados abertos no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0af9-p104">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="b0af9-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0af9-126">Remarks</span></span>

<span data-ttu-id="b0af9-127">Esta ação é semelhante a clicar duas vezes no procedimento armazenado do Painel de Navegação ou a clicar com o botão direito do mouse no procedimento armazenado do Painel de Navegação e selecionar o comando desejado.</span><span class="sxs-lookup"><span data-stu-id="b0af9-127">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="b0af9-p105">Alternar para o modo Design enquanto o procedimento armazenado é aberto remove a configuração do argumento **Modo de Dados** do procedimento armazenado. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="b0af9-p105">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="b0af9-130">Você pode arrastar um procedimento armazenado no painel de navegação para uma linha de ação de macro.</span><span class="sxs-lookup"><span data-stu-id="b0af9-130">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="b0af9-131">Isso cria automaticamente uma ação **AbrirProcedimentoArmazenado** que abre o procedimento armazenado no modo folha de dados.</span><span class="sxs-lookup"><span data-stu-id="b0af9-131">This automatically creates an **OpenStoredProcedure** action that opens the stored procedure in Datasheet view.</span></span>
> - <span data-ttu-id="b0af9-132">
						Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um procedimento armazenado é executado (indicando que ele é um procedimento armazenado e mostrando quantos registros serão afetados), use a ação \*\*DefinirAviso\*\* para suprimir a exibição dessas mensagens.
</span><span class="sxs-lookup"><span data-stu-id="b0af9-132">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="b0af9-133">Para executar a ação **AbrirProcedimentoArmazenado** em um módulo do VBA (Visual Basic for Applications), use o método **OpenStoredProcedure** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="b0af9-133">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

