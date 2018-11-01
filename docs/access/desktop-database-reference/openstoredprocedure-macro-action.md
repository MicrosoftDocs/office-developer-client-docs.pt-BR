---
title: Ação de macro AbrirProcedimentoArmazenado
TOCTitle: OpenStoredProcedure Macro Action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52d7d6c54913511ab593ee77d374ed55984ed40b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883250"
---
# <a name="openstoredprocedure-macro-action"></a><span data-ttu-id="30664-102">Ação de macro AbrirProcedimentoArmazenado</span><span class="sxs-lookup"><span data-stu-id="30664-102">OpenStoredProcedure Macro Action</span></span>


<span data-ttu-id="30664-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="30664-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30664-p101">Em um projeto do Access, você pode usar a ação **AbrirProcedimentoArmazenado** para abrir um procedimento armazenado em modo Folha de Dados, em modo Design de procedimento armazenado ou Visualizar Impressão. Esta ação executa o procedimento armazenado nomeado quando aberta em modo Folha de Dados. Você pode selecionar o modo de entrada de dados do procedimento armazenado e restringir os registros exibidos pelo procedimento armazenado.</span><span class="sxs-lookup"><span data-stu-id="30664-p101">In an Access project, you can use the **OpenStoredProcedure** action to open a stored procedure in Datasheet view, stored procedure Design view, or Print Preview. This action runs the named stored procedure when opened in Datasheet view. You can select the data entry mode for the stored procedure and restrict the records that the stored procedure displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="30664-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="30664-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="30664-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="30664-109">Setting</span></span>

<span data-ttu-id="30664-110">A ação **AbrirProcedimentoArmazenado** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="30664-110">The **OpenStoredProcedure** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30664-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="30664-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="30664-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="30664-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30664-113"><strong>Nome do Procedimento</strong></span><span class="sxs-lookup"><span data-stu-id="30664-113"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="30664-114">O nome do procedimento armazenado para abrir.</span><span class="sxs-lookup"><span data-stu-id="30664-114">The name of the stored procedure to open.</span></span> <span data-ttu-id="30664-115">A caixa <strong>Nome do procedimento</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os procedimentos armazenados no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="30664-115">The <strong>Procedure Name box</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all stored procedures in the current database.</span></span> <span data-ttu-id="30664-116">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="30664-116">This is a required argument.</span></span> <span data-ttu-id="30664-117">Se você executar uma macro que contém a ação <strong>AbrirProcedimentoArmazenado</strong> em um banco de dados biblioteca, o Microsoft Access procurará o procedimento armazenado com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="30664-117">If you run a macro containing the <strong>OpenStoredProcedure</strong> action in a library database, Microsoft Access first looks for the stored procedure with this name first in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30664-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="30664-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="30664-p104">O modo de exibição no qual o procedimento armazenado será aberto. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</span><span class="sxs-lookup"><span data-stu-id="30664-p104">The view in which the stored procedure will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30664-122"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="30664-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="30664-p105">O modo de entrada de dados do procedimento armazenado. Isso se aplica somente a procedimentos armazenados abertos no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="30664-p105">The data entry mode for the stored procedure. This applies only to stored procedures opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="30664-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="30664-127">Remarks</span></span>

<span data-ttu-id="30664-128">Esta ação é semelhante a clicar duas vezes no procedimento armazenado do Painel de Navegação ou a clicar com o botão direito do mouse no procedimento armazenado do Painel de Navegação e selecionar o comando desejado.</span><span class="sxs-lookup"><span data-stu-id="30664-128">This action is similar to double-clicking the stored procedure in the Navigation Pane, or right-clicking the stored procedure in the Navigation Pane and selecting the command you want.</span></span>

<span data-ttu-id="30664-p106">Alternar para o modo Design enquanto o procedimento armazenado é aberto remove a configuração do argumento **Modo de Dados** do procedimento armazenado. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="30664-p106">Switching to Design view while the stored procedure is open removes the **Data Mode** argument setting for the stored procedure. This setting is not in effect, even if the user returns to Datasheet view.</span></span>


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P><span data-ttu-id="30664-131">Você pode arrastar um procedimento armazenado no painel de navegação para uma linha de ação de macro.</span><span class="sxs-lookup"><span data-stu-id="30664-131">You can drag a stored procedure from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="30664-132">Isso cria automaticamente uma ação <STRONG>AbrirProcedimentoArmazenado</STRONG> que abre o procedimento armazenado no modo folha de dados.</span><span class="sxs-lookup"><span data-stu-id="30664-132">This automatically creates an <STRONG>OpenStoredProcedure</STRONG> action that opens the stored procedure in Datasheet view.</span></span></P>
> <LI>
> <P><span data-ttu-id="30664-133">
> 						Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um procedimento armazenado é executado (indicando que ele é um procedimento armazenado e mostrando quantos registros serão afetados), use a ação <STRONG>DefinirAviso</STRONG> para suprimir a exibição dessas mensagens.
</span><span class="sxs-lookup"><span data-stu-id="30664-133">If you do not want to display the system messages that normally appear when a stored procedure is run (indicating it is a stored procedure and showing how many records will be affected), you can use the <STRONG>SetWarning</STRONG> action to suppress the display of these messages.</span></span></P></LI></UL>
<P></P>



<span data-ttu-id="30664-134">Para executar a ação **AbrirProcedimentoArmazenado** em um módulo do VBA (Visual Basic for Applications), use o método **OpenStoredProcedure** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="30664-134">To run the **OpenStoredProcedure** action in a Visual Basic for Applications (VBA) module, use the **OpenStoredProcedure** method of the **DoCmd** object.</span></span>

