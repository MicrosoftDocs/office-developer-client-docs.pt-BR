---
title: Ação da macro ExcluirObjeto
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dae5718e7b4cb609cb50bd65ee6e2486f4ebaab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294026"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="8a076-102">Ação da macro ExcluirObjeto</span><span class="sxs-lookup"><span data-stu-id="8a076-102">DeleteObject macro action</span></span>

<span data-ttu-id="8a076-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a076-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8a076-104">Você pode usar a ação **ExcluirObjeto** para excluir um objeto de banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="8a076-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="8a076-105">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="8a076-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="8a076-106">Setting</span><span class="sxs-lookup"><span data-stu-id="8a076-106">Setting</span></span>

<span data-ttu-id="8a076-107">A ação **ExcluirObjeto** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8a076-107">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a076-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="8a076-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8a076-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a076-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a076-110"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="8a076-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="8a076-p101">O tipo de objeto que será excluído. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para excluir o objeto selecionado no Painel de Navegação, deixe este argumento em branco.</span><span class="sxs-lookup"><span data-stu-id="8a076-p101">The type of object to delete. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a076-114"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="8a076-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8a076-115">O nome do objeto que será excluído.</span><span class="sxs-lookup"><span data-stu-id="8a076-115">The name of the object to delete.</span></span> <span data-ttu-id="8a076-116">A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a076-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="8a076-117">Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, deixe este argumento em branco também.</span><span class="sxs-lookup"><span data-stu-id="8a076-117">If you leave the <strong>Object Type</strong> box blank, leave this box blank also.</span></span> <span data-ttu-id="8a076-118">Se você executar uma macro que contém a ação <strong>ExcluirObjeto</strong> em um banco de dados biblioteca, o Microsoft Office Access 2007 primeiro procurará o objeto com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="8a076-118">If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> <span data-ttu-id="8a076-119">[!CUIDADO] Se você deixar as caixas **Tipo de Objeto** e **Nome do Objeto** em branco, o Access excluirá o objeto selecionado no Painel de Navegação sem exibir uma mensagem de aviso ao encontrar a ação **ExcluirObjeto**.</span><span class="sxs-lookup"><span data-stu-id="8a076-119">If you leave the **Object Type** and **Object Name** boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the **DeleteObject** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a076-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a076-120">Remarks</span></span>

<span data-ttu-id="8a076-p103">Você pode usar a ação **ExcluirObjeto** para excluir objetos temporários criados ao executar a macro. Por exemplo, é possível usar a ação **AbrirConsulta** para executar uma consulta criar tabela que cria uma tabela temporária. Quando tiver concluído o uso da tabela temporária, você poderá usar a ação **ExcluirObjeto** para excluí-la.</span><span class="sxs-lookup"><span data-stu-id="8a076-p103">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro. For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table. When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="8a076-124">Esta ação equivale a selecionar um objeto no Painel de Navegação e pressionar a tecla DELETE ou clicar com o botão direito do mouse no objeto no Painel de Navegação e clicar em **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="8a076-124">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="8a076-125">Para executar a ação **ExcluirObjeto** em um módulo do Visual Basic for Applications, use o método **DeleteObject** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="8a076-125">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>

