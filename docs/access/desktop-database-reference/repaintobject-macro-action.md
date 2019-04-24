---
title: Ação da macro RedesenharObjeto
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2ef6c5f38064ae3253cd7e0e58732f63294ceb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306682"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="7318b-102">Ação da macro RedesenharObjeto</span><span class="sxs-lookup"><span data-stu-id="7318b-102">RepaintObject macro action</span></span>

<span data-ttu-id="7318b-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7318b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7318b-p101">Você pode usar a ação **RedesenharObjeto** para concluir todas as atualizações de tela pendentes para um objeto de bancos de dados especificado ou para o objeto de banco de dados ativo, caso não haja nenhum especificado. Essas atualizações incluem todos os recálculos pendentes de controles do objeto.</span><span class="sxs-lookup"><span data-stu-id="7318b-p101">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified. Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="7318b-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="7318b-106">Setting</span></span>

<span data-ttu-id="7318b-107">A ação **RedesenharObjeto** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7318b-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7318b-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="7318b-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7318b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7318b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7318b-110"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="7318b-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="7318b-p102">O tipo de objeto a ser redesenhado. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Deixe esse argumento em branco para selecionar o objeto ativo.</span><span class="sxs-lookup"><span data-stu-id="7318b-p102">The type of object to repaint. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7318b-114"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="7318b-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7318b-p103">O nome do objeto a ser redesenhado. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos de banco de dados do tipo selecionado pelo argumento <strong>Tipo de Objeto</strong>. Se você deixar o argumento <strong>Tipo de Objeto</strong> em branco, faça o mesmo com este argumento.</span><span class="sxs-lookup"><span data-stu-id="7318b-p103">The name of the object to repaint. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7318b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7318b-118">Remarks</span></span>

<span data-ttu-id="7318b-p104">Para concluir as atualizações de tela pendentes, o Microsoft Access aguarda a finalização de outras tarefas pendentes. Com esta ação, você pode forçar o redesenho imediato dos controles do objeto especificado. Você pode usar a ação:</span><span class="sxs-lookup"><span data-stu-id="7318b-p104">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks. With this action, you can force immediate repainting of the controls in the specified object. You can use this action:</span></span>

- <span data-ttu-id="7318b-p105">Quando utilizar a ação **DefinirValor** para alterar valores em vários controles. O Access talvez não mostre as alterações de imediato, principalmente se outros controles (por exemplo, controles calculados) dependerem dos valores dos controles alterados.</span><span class="sxs-lookup"><span data-stu-id="7318b-p105">When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

- <span data-ttu-id="7318b-p106">Quando quiser verificar se o formulário em exibição mostra os dados de todos os controles. Por exemplo, controles contendo objetos OLE não exibem os dados imediatamente após a abertura de um formulário.</span><span class="sxs-lookup"><span data-stu-id="7318b-p106">When you want to make sure that the form you are viewing displays data in all of its controls. For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>

> [!NOTE]
> - <span data-ttu-id="7318b-p107">Esta ação não ativa a repetição de consulta do banco de dados, portanto, não mostra registros novos e alterados nem remove registros excluídos da tabela ou da consulta subjacente do objeto. Use a ação **Repetir Consulta** para consultar outra vez a origem do objeto ou de um de seus controles. Use a ação **MostrarTodosRegistros** para exibir a maioria dos registros recentes e remover todos os filtros aplicados.</span><span class="sxs-lookup"><span data-stu-id="7318b-p107">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the **Requery** action to requery the source of the object or one of its controls. Use the **ShowAllRecords** action to display the most recent records and remove any applied filters.</span></span>
> - <span data-ttu-id="7318b-129">A ação **RedesenharObjeto** não tem o mesmo efeito de clicar em **Atualizar** no grupo **Registros** da guia **Página Inicial**, que mostra todas as alterações que você ou outros usuários tenham feito nos registros exibidos no momento, em formulários e folhas de dados.</span><span class="sxs-lookup"><span data-stu-id="7318b-129">The **RepaintObject** action doesn't have the same effect as clicking **Refresh** in the **Records** group on the **Home** tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span>

<span data-ttu-id="7318b-130">Para executar a ação **RedesenharObjeto** em um módulo do VBA, use o método **RepaintObject** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="7318b-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>

