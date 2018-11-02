---
title: Ação da macro AbrirModoDeExibição
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 50346ce66d32d91a4f902adbb5600438d214e1fb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921324"
---
# <a name="openview-macro-action"></a><span data-ttu-id="cad72-102">Ação da macro AbrirModoDeExibição</span><span class="sxs-lookup"><span data-stu-id="cad72-102">OpenView macro action</span></span>


<span data-ttu-id="cad72-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cad72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cad72-p101">Em um projeto do Access, você pode usar a ação **AbrirModoDeExibição** para abrir um modo de exibição em modo Folha de Dados, modo Design ou Visualizar Impressão. Esta ação executa o modo de exibição nomeado quando aberta em modo Folha de Dados. É possível selecionar a entrada de dados do modo de exibição e restringir os registros exibidos pelo modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="cad72-p101">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview. This action runs the named view when opened in Datasheet view. You can select data entry for the view and restrict the records that the view displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cad72-p102">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="cad72-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="cad72-109">Configuração</span><span class="sxs-lookup"><span data-stu-id="cad72-109">Setting</span></span>

<span data-ttu-id="cad72-110">A ação **AbrirModoDeExibição** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cad72-110">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cad72-111">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="cad72-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cad72-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cad72-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cad72-113"><strong>Nome do Modo de Exibição</strong></span><span class="sxs-lookup"><span data-stu-id="cad72-113"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cad72-114">O nome da exibição a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="cad72-114">The name of the view to open.</span></span> <span data-ttu-id="cad72-115">A caixa de <strong>Nome de exibição</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os modos de exibição no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="cad72-115">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="cad72-116">Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cad72-116">This is a required argument.</span></span> <span data-ttu-id="cad72-117">Se você executar uma macro que contém a ação <strong>AbrirModoDeExibição</strong> em um banco de dados biblioteca, o Microsoft Access procurará o modo de exibição com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="cad72-117">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cad72-118"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="cad72-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="cad72-p104">O modo de exibição no qual o modo de exibição será aberto. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</span><span class="sxs-lookup"><span data-stu-id="cad72-p104">The view in which the view will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cad72-122"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="cad72-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="cad72-p105">O modo de entrada de dados do modo de exibição. Isso se aplica somente a modos de exibição abertos no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="cad72-p105">The data entry mode for the view. This applies only to views opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cad72-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="cad72-127">Remarks</span></span>

<span data-ttu-id="cad72-128">Esta ação é semelhante a clicar duas vezes em um modo de exibição do Painel de Navegação ou a clicar com o botão direito do mouse no modo de exibição do Painel de Navegação e clicar no comando desejado.</span><span class="sxs-lookup"><span data-stu-id="cad72-128">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

<span data-ttu-id="cad72-129">**Dicas**</span><span class="sxs-lookup"><span data-stu-id="cad72-129">**Tips**</span></span>

  - <span data-ttu-id="cad72-p106">Você pode arrastar um modo de exibição do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirModoDeExibição** que abre o modo de exibição em modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="cad72-p106">You can drag a view from the Navigation Pane to a macro action row. This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>

  - <span data-ttu-id="cad72-132">Se você não deseja exibir as mensagens do sistema que normalmente aparecem quando um modo de exibição é executado (indicando que é um modo de exibição ou mostrando quantos registros serão afetados), use a ação **DefinirAviso** para suprimir a exibição dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="cad72-132">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="cad72-133">Para executar a ação **AbrirModoDeExibição** em um módulo do VBA (Visual Basic for Applications), use o método **OpenView** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="cad72-133">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

