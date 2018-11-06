---
title: Ação da macro AbrirFunção
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a3a1ed5b08c9bf0b318baeebb7190868b90682f0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998858"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="9478a-102">Ação da macro AbrirFunção</span><span class="sxs-lookup"><span data-stu-id="9478a-102">OpenFunction macro action</span></span>

<span data-ttu-id="9478a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9478a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9478a-p101">Em um projeto do Access, você pode usar a ação **AbrirFunção** para abrir uma função definida pelo usuário no modo Folha de Dados, uma função in-line no modo Design, o modo Editor de Texto do SQL (para uma função definida pelo usuário escalar ou de tabela) ou Visualizar Impressão. Esta ação executa a função definida pelo usuário quando aberta em modo Folha de Dados. Você também pode selecionar o modo de entrada de dados para a função definida pelo usuário e restringir os registros exibidos pela função definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9478a-p101">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview. This action runs the user-defined function when opened in Datasheet view. You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="9478a-107">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="9478a-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="9478a-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="9478a-108">Setting</span></span>

<span data-ttu-id="9478a-109">A ação **AbrirFunção** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9478a-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9478a-110">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="9478a-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9478a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9478a-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9478a-112"><strong>Nome da função</strong></span><span class="sxs-lookup"><span data-stu-id="9478a-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9478a-113">O nome da função definida pelo usuário para abrir.</span><span class="sxs-lookup"><span data-stu-id="9478a-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="9478a-114">Caixa <strong>Nome da função</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todas as funções definidas pelo usuário no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="9478a-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="9478a-115">Esse é um argumento necessário. Se você executar uma macro que contém a ação <strong>função</strong> em um banco de dados biblioteca, o Microsoft Access procurará primeiro a função com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="9478a-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9478a-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="9478a-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="9478a-p103">O modo de exibição no qual a função definida pelo usuário será aberta. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</span><span class="sxs-lookup"><span data-stu-id="9478a-p103">The view in which the user-defined function will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9478a-120"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="9478a-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="9478a-p104">O modo de entrada de dados da função definida pelo usuário. Isso se aplica somente a funções definidas pelo usuário abertas no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode exibir ou editar os existentes), <strong>Editar</strong> (o usuário pode exibir ou editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="9478a-p104">The data entry mode for the user-defined function. This applies only to user-defined functions opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9478a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9478a-125">Remarks</span></span>

<span data-ttu-id="9478a-126">Esta ação é semelhante a clicar duas vezes em uma função definida pelo usuário do Painel de Navegação ou a clicar com o botão direito do mouse na função do Painel de Navegação e selecionar um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="9478a-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="9478a-p105">Alternar para o modo Design enquanto a função definida pelo usuário é aberta remove a configuração do argumento **Modo de Dados** da função definida pelo usuário. Essa configuração não entra em vigor, mesmo se o usuário retorna para o modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="9478a-p105">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function. This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="9478a-p106">Você pode selecionar uma função definida pelo usuário no Painel de Navegação e arrastá-la para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirFunção** que abre a função definida pelo usuário em modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="9478a-p106">You can select a user-defined function in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="9478a-131">Se você não desejar exibir as mensagens de sistema que normalmente aparecem quando uma função definida pelo usuário é executada (indicando que é uma função definida pelo usuário e mostrando quantos registros serão afetados), poderá usar a ação **DefinirAvisos** para suprimir a exibição dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="9478a-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="9478a-132">Para executar a ação **AbrirFunção** em um módulo do VBA (Visual Basic for Applications), use o método **OpenFunction** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="9478a-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

