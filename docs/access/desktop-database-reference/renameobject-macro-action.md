---
title: Ação da macro RenomearObjeto
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306717"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="adc07-102">Ação da macro RenomearObjeto</span><span class="sxs-lookup"><span data-stu-id="adc07-102">RenameObject macro action</span></span>

<span data-ttu-id="adc07-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adc07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adc07-104">Você pode usar a ação **RenomearObjeto** para renomear um objeto de banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="adc07-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="adc07-105">Essa ação não será permitida se o banco de dados não for confiável.</span><span class="sxs-lookup"><span data-stu-id="adc07-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="adc07-106">Setting</span><span class="sxs-lookup"><span data-stu-id="adc07-106">Setting</span></span>

<span data-ttu-id="adc07-107">A ação **RenomearObjeto** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="adc07-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adc07-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="adc07-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="adc07-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="adc07-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adc07-110"><strong>Novo nome</strong></span><span class="sxs-lookup"><span data-stu-id="adc07-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="adc07-p101">Um novo nome para o objeto de banco de dados. Digite o nome do objeto na caixa <strong>Novo Nome</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="adc07-p101">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adc07-114"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="adc07-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="adc07-p102">O tipo de objeto a ser renomeado. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong>. Para renomear o objeto selecionado no Painel de Navegação, deixe esse argumento em branco.</span><span class="sxs-lookup"><span data-stu-id="adc07-p102">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adc07-118"><strong>Nome antigo</strong></span><span class="sxs-lookup"><span data-stu-id="adc07-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="adc07-119">O nome do objeto a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="adc07-119">The name of the object to be renamed.</span></span> <span data-ttu-id="adc07-120">A caixa <strong>Nome Antigo</strong> mostra todos os objetos de banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="adc07-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="adc07-121">Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, faça o mesmo com este argumento.</span><span class="sxs-lookup"><span data-stu-id="adc07-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="adc07-122"><strong>OBSERVAÇÃO:</strong>se você executar uma <STRONG></STRONG> macro que contém a ação Renomear em um banco de dados biblioteca, o Microsoft Access primeiro procura o objeto com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="adc07-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="adc07-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="adc07-123">Remarks</span></span>

<span data-ttu-id="adc07-124">O novo nome do objeto de banco de dados deve cumprir as convenções de nomeação padrão para objetos do Access.</span><span class="sxs-lookup"><span data-stu-id="adc07-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="adc07-125">Não é possível renomear um objeto aberto.</span><span class="sxs-lookup"><span data-stu-id="adc07-125">You can't rename an open object.</span></span>

<span data-ttu-id="adc07-p104">Se você deixar em branco os argumentos **Tipo de Objeto** e **Nome Antigo**, o Access renomeará o objeto selecionado no Painel de Navegação. Para selecionar um objeto nesse painel, você pode usar a ação **SelecionarObjeto** com o argumento **No Painel de Navegação** definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="adc07-p104">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="adc07-p105">Outra maneira de renomear um objeto é clicar com o botão direito do mouse no Painel de Navegação, clicar em **Renomear** e digitar um novo nome. Com a ação **RenomearObjeto**, você não precisa selecionar primeiro o objeto no Painel de Navegação nem interromper a macro para digitar o novo nome.</span><span class="sxs-lookup"><span data-stu-id="adc07-p105">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="adc07-130">Essa ação é diferente da ação **CopiarObjeto**, que cria uma cópia do objeto com um novo nome.</span><span class="sxs-lookup"><span data-stu-id="adc07-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="adc07-131">Para executar a ação **RenomearObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **Renomear** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="adc07-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

