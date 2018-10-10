---
title: Ação de macro ExcluirObjeto
TOCTitle: DeleteObject Macro Action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 85e9fc888e06a69be6f458ed03ad92b8253b30a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463465"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="9348f-102">Ação de macro ExcluirObjeto</span><span class="sxs-lookup"><span data-stu-id="9348f-102">DeleteObject Macro Action</span></span>


<span data-ttu-id="9348f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9348f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9348f-104">Você pode usar a ação **ExcluirObjeto** para excluir um objeto de banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="9348f-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9348f-p101">[!OBSERVAçãO] This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span><span class="sxs-lookup"><span data-stu-id="9348f-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="9348f-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="9348f-107">Setting</span></span>

<span data-ttu-id="9348f-108">A ação **ExcluirObjeto** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9348f-108">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9348f-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="9348f-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9348f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9348f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9348f-111"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="9348f-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="9348f-p102">O tipo de objeto que será excluído. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para excluir o objeto selecionado no Painel de Navegação, deixe este argumento em branco.</span><span class="sxs-lookup"><span data-stu-id="9348f-p102">The type of object to delete. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9348f-115"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="9348f-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9348f-116">O nome do objeto a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9348f-116">The name of the object to delete.</span></span> <span data-ttu-id="9348f-117">A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="9348f-117">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="9348f-118">Se você deixar a caixa <strong>Tipo de objeto</strong> , deixe esta caixa em branco também.</span><span class="sxs-lookup"><span data-stu-id="9348f-118">If you leave the <strong>Object Type</strong> box blank, leave this box blank also.</span></span> <span data-ttu-id="9348f-119">Se você executar uma macro que contém a ação <strong>ExcluirObjeto</strong> em um banco de dados biblioteca, o Microsoft Office Access 2007 primeiro procurará o objeto com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="9348f-119">If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>



> [!WARNING]
> <P><span data-ttu-id="9348f-120">[!CUIDADO] Se você deixar as caixas <STRONG>Tipo de Objeto</STRONG> e <STRONG>Nome do Objeto</STRONG> em branco, o Access excluirá o objeto selecionado no Painel de Navegação sem exibir uma mensagem de aviso ao encontrar a ação <STRONG>ExcluirObjeto</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="9348f-120">If you leave the <STRONG>Object Type</STRONG> and <STRONG>Object Name</STRONG> boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the <STRONG>DeleteObject</STRONG> action.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="9348f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9348f-121">Remarks</span></span>

<span data-ttu-id="9348f-p104">Você pode usar a ação **ExcluirObjeto** para excluir objetos temporários criados ao executar a macro. Por exemplo, é possível usar a ação **AbrirConsulta** para executar uma consulta criar tabela que cria uma tabela temporária. Quando tiver concluído o uso da tabela temporária, você poderá usar a ação **ExcluirObjeto** para excluí-la.</span><span class="sxs-lookup"><span data-stu-id="9348f-p104">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro. For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table. When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="9348f-125">Esta ação equivale a selecionar um objeto no Painel de Navegação e pressionar a tecla DELETE ou clicar com o botão direito do mouse no objeto no Painel de Navegação e clicar em **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="9348f-125">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="9348f-126">Para executar a ação **ExcluirObjeto** em um módulo do Visual Basic for Applications, use o método **DeleteObject** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="9348f-126">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>

