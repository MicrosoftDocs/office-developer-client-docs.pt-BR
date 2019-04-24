---
title: Ação da macro RepetirConsulta
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8b90af8d1cda073ffa37022bb5db5e8cf8e3b978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306703"
---
# <a name="requery-macro-action"></a><span data-ttu-id="27cf3-102">Ação da macro RepetirConsulta</span><span class="sxs-lookup"><span data-stu-id="27cf3-102">Requery macro action</span></span>

<span data-ttu-id="27cf3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27cf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27cf3-p101">Você pode usar a ação **RepetirConsulta** para atualizar os dados de um controle especificado no objeto ativo, repetindo a consulta da origem do controle. Se nenhum controle estiver especificado, a ação consultará outra vez a origem do próprio objeto. Use essa ação para verificar se o objeto ativo ou um de seus controles exibe a maioria dos dados atuais.</span><span class="sxs-lookup"><span data-stu-id="27cf3-p101">You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.</span></span>

## <a name="setting"></a><span data-ttu-id="27cf3-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="27cf3-107">Setting</span></span>

<span data-ttu-id="27cf3-108">A ação **RepetirConsulta** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="27cf3-108">The **Requery** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27cf3-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="27cf3-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="27cf3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="27cf3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27cf3-111"><strong>Nome do controle</strong></span><span class="sxs-lookup"><span data-stu-id="27cf3-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="27cf3-p102">O nome do controle a ser atualizado. Insira o nome do controle na caixa <strong>Nome do Controle</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Use somente o nome do controle, e não o identificador totalmente qualificado (como <strong>Formulários</strong>!<em>nomeform</em>!<em>nomedocontrole</em>). Deixe esse argumento em branco para repetir a consulta da origem do objeto ativo. Se o objeto ativo for uma folha de dados ou um conjunto de resultados de consulta, deixe esse argumento em branco.</span><span class="sxs-lookup"><span data-stu-id="27cf3-p102">The name of the control you want to update. Enter the control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You should use only the name of the control, not the fully qualified identifier (such as <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>). Leave this argument blank to requery the source of the active object. If the active object is a datasheet or a query result set, you must leave this argument blank.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="27cf3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="27cf3-117">Remarks</span></span>

<span data-ttu-id="27cf3-118">A ação **RepetirConsulta** executa um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="27cf3-118">The **Requery** action does one of the following:</span></span>

- <span data-ttu-id="27cf3-119">Refaz a consulta na qual o controle ou objeto se baseia.</span><span class="sxs-lookup"><span data-stu-id="27cf3-119">Reruns the query on which the control or object is based.</span></span>

- <span data-ttu-id="27cf3-120">Exibe quaisquer registros novos ou alterados e remove quaisquer registros excluídos da tabela na qual o objeto ou o controle se baseia.</span><span class="sxs-lookup"><span data-stu-id="27cf3-120">Displays any new or changed records, and removes any deleted records from the table on which the control or object is based.</span></span>

> [!NOTE]
> <span data-ttu-id="27cf3-121">[!OBSERVAçãO] A ação **RepetirConsulta** não afeta a posição do ponteiro de registro.</span><span class="sxs-lookup"><span data-stu-id="27cf3-121">The **Requery** action does not affect the position of the record pointer.</span></span>

<span data-ttu-id="27cf3-122">Os controles baseados em uma consulta ou tabela incluem:</span><span class="sxs-lookup"><span data-stu-id="27cf3-122">Controls based on a query or table include:</span></span>

- <span data-ttu-id="27cf3-123">Caixas de listagem e Caixas de combinação.</span><span class="sxs-lookup"><span data-stu-id="27cf3-123">List boxes and combo boxes.</span></span>

- <span data-ttu-id="27cf3-124">Controles de subformulário.</span><span class="sxs-lookup"><span data-stu-id="27cf3-124">Subform controls.</span></span>

- <span data-ttu-id="27cf3-125">Objetos OLE, tais como gráficos.</span><span class="sxs-lookup"><span data-stu-id="27cf3-125">OLE objects, such as charts.</span></span>

- <span data-ttu-id="27cf3-126">Controles contendo funções de agregação de domínios; por exemplo, **DSoma**.</span><span class="sxs-lookup"><span data-stu-id="27cf3-126">Controls containing domain aggregate functions, such as **DSum**.</span></span>

<span data-ttu-id="27cf3-127">Se o controle especificado não se basear em uma consulta ou tabela, essa ação forçará o recálculo do controle.</span><span class="sxs-lookup"><span data-stu-id="27cf3-127">If the specified control isn't based on a query or table, this action forces a recalculation of the control.</span></span>

<span data-ttu-id="27cf3-p103">Se você deixar em branco o argumento **Nome do Controle**, a ação **RepetirConsulta** terá o mesmo efeito das teclas SHIFT+F9 quando o objeto tiver o foco. Se um controle de subformulário tiver o foco, essa ação repetirá a consulta somente da origem do subformulário (assim como as teclas SHIFT+F9 fazem).</span><span class="sxs-lookup"><span data-stu-id="27cf3-p103">If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).</span></span>

> [!NOTE]
> <span data-ttu-id="27cf3-p104">[!OBSERVAçãO] A ação **RepetirConsulta** refaz a consulta da origem do controle ou do objeto. Por outro lado, a ação **RedesenharObjeto** redesenha os controles do objeto especificado, mas não repete a consulta do banco de dados nem exibe novos registros. A ação **MostrarTodosRegistros** não só repete a consulta do objeto ativo, mas também remove todos os filtros aplicados, o que a ação **RepetirConsulta** não faz.</span><span class="sxs-lookup"><span data-stu-id="27cf3-p104">The **Requery** action requeries the source of the control or object. In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records. The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.</span></span>

<span data-ttu-id="27cf3-133">Se você quiser repetir a consulta de um controle que não esteja no objeto ativo, use o método **Requery** em um módulo do VBA (Visual Basic for Applications), e não a ação **Requery** ou seu respectivo método **Requery** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="27cf3-133">If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object.</span></span> <span data-ttu-id="27cf3-134">O método **Requery** do VBA é mais rápido do que a ação **Requery** ou o método **DoCmd.Requery**.</span><span class="sxs-lookup"><span data-stu-id="27cf3-134">The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method.</span></span> <span data-ttu-id="27cf3-135">Além disso, quando você usa a ação **Requery** ou o método **DoCmd.Requery** o Microsoft Access fecha a consulta e a recarrega do banco de dados, mas quando você usa o método **Requery**, o Access reexecuta a consulta, mas sem fechá-la e recarregá-la.</span><span class="sxs-lookup"><span data-stu-id="27cf3-135">In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it.</span></span> <span data-ttu-id="27cf3-136">Observe que o método reQuery do ADO \*\*\*\* (objeto de dados ActiveX) funciona da mesma maneira que o método Requery do Access. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="27cf3-136">Note that the ActiveX Data object (ADO) **Requery** method works the same way as the Access **Requery** method.</span></span>

