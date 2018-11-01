---
title: Ação de macro FecharJanela
TOCTitle: CloseWindow Macro Action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab6b3a265b6e63680add41ec051ba61a262819bd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876838"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="6ec11-102">Ação de macro FecharJanela</span><span class="sxs-lookup"><span data-stu-id="6ec11-102">CloseWindow Macro Action</span></span>


<span data-ttu-id="6ec11-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ec11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ec11-104">Você pode usar a ação **fecharJanela** para fechar uma guia de documento especificada do Access ou a guia do documento ativo se nenhuma estiver especificada.</span><span class="sxs-lookup"><span data-stu-id="6ec11-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="6ec11-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="6ec11-105">Setting</span></span>

<span data-ttu-id="6ec11-106">A ação **FecharJanela** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="6ec11-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ec11-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="6ec11-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6ec11-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ec11-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ec11-109"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="6ec11-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="6ec11-p101">O tipo de objeto cuja guia de documento você deseja fechar. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para selecionar a guia de documento ativa, deixe este argumento em branco. 

</span><span class="sxs-lookup"><span data-stu-id="6ec11-p101">The type of object whose document tab you want to close. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="6ec11-113">Se você estiver fechando um módulo no Editor do Visual Basic, use **Módulo** no argumento **Tipo de Objeto**.</span><span class="sxs-lookup"><span data-stu-id="6ec11-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ec11-114"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="6ec11-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6ec11-p102">O nome do objeto que será fechado. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Clique no objeto que será fechado. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, deixe este argumento em branco também.</span><span class="sxs-lookup"><span data-stu-id="6ec11-p102">The name of the object to be closed. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. Click the object to close. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ec11-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="6ec11-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="6ec11-p103">Define se serão salvas as alterações no objeto quando ele estiver fechado. Clique em <strong>Sim</strong> (salvar o objeto), <strong>Não</strong> (fechar o objeto sem salvá-lo) ou <strong>Aviso</strong> (perguntar ao usuário se o objeto deverá ser salvo ou não). O padrão é <strong>Aviso</strong>.</span><span class="sxs-lookup"><span data-stu-id="6ec11-p103">Whether to save changes to the object when it is closed. Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object). The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6ec11-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ec11-123">Remarks</span></span>

<span data-ttu-id="6ec11-p104">A ação **FecharJanela** funciona em todos os objetos de banco de dados que o usuário pode abrir ou fechar explicitamente. Esta ação equivale a selecionar um objeto e fechá-lo clicando com o botão direito do mouse na guia de documento do objeto e clicando em **Fechar** no menu de atalho ou clicando no botão **Fechar** do objeto.</span><span class="sxs-lookup"><span data-stu-id="6ec11-p104">The **CloseWindow** action works on all database objects that the user can explicitly open or close. This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="6ec11-p105">Se o argumento **Salvar** for definido como **Aviso** e o objeto ainda não tiver sido salvo antes de a ação **FecharJanela** ser executada, uma caixa de diálogo solicitará ao usuário que salve o objeto antes de a macro fechá-lo. Se você tiver definido o argumento **Avisos Ativos** da ação **DefinirAvisos** como **Não**, a caixa de diálogo não será exibida e o objeto será salvo automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6ec11-p105">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it. If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="6ec11-128">Para executar a ação **FecharJanela** em um módulo do VBA (Visual Basic for Applications), use o método **FecharJanela** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="6ec11-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

