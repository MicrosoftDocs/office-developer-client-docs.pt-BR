---
title: Ação da macro AbrirTabela
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288291"
---
# <a name="opentable-macro-action"></a><span data-ttu-id="574c4-102">Ação da macro AbrirTabela</span><span class="sxs-lookup"><span data-stu-id="574c4-102">OpenTable macro action</span></span>

<span data-ttu-id="574c4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="574c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="574c4-p101">Você pode usar a ação **AbrirTabela** para abrir uma tabela em modo Folha de Dados, modo Design ou Visualizar Impressão. Também pode selecionar um modo de entrada de dados para a tabela.</span><span class="sxs-lookup"><span data-stu-id="574c4-p101">You can use the **OpenTable** action to open a table in Datasheet view, Design view, or Print Preview. You can also select a data entry mode for the table.</span></span>

## <a name="setting"></a><span data-ttu-id="574c4-106">Setting</span><span class="sxs-lookup"><span data-stu-id="574c4-106">Setting</span></span>

<span data-ttu-id="574c4-107">A ação **AbrirTabela** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="574c4-107">The **OpenTable** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="574c4-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="574c4-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="574c4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="574c4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="574c4-110"><strong>Nome da Tabela</strong></span><span class="sxs-lookup"><span data-stu-id="574c4-110"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="574c4-111">O nome da tabela que será aberta.</span><span class="sxs-lookup"><span data-stu-id="574c4-111">The name of the table to open.</span></span> <span data-ttu-id="574c4-112">A caixa <strong>Nome da Tabela</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros mostra todas as tabelas do banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="574c4-112">The <strong>Table Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all tables in the current database.</span></span> <span data-ttu-id="574c4-113">Esse é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="574c4-113">This is a required argument.</span></span> <span data-ttu-id="574c4-114">Se você executar uma macro que contém a ação <strong>AbrirTabela</strong> em um banco de dados biblioteca, o Microsoft Access procurará a tabela com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="574c4-114">If you run a macro containing the <strong>OpenTable</strong> action in a library database, Microsoft Microsoft Access looks for the table with this name first in the library database, then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="574c4-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="574c4-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="574c4-p103">O modo de exibição no qual a tabela será aberta. Clique em <strong>Folha de Dados</strong>, <strong>Design</strong>, <strong>Visualizar Impressão</strong>, <strong>Tabela Dinâmica</strong> ou <strong>Gráfico Dinâmico</strong> na caixa <strong>Modo de Exibição</strong>. O padrão é <strong>Folha de Dados</strong>.</span><span class="sxs-lookup"><span data-stu-id="574c4-p103">The view in which the table will open. Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="574c4-119"><strong>Modo de Dados</strong></span><span class="sxs-lookup"><span data-stu-id="574c4-119"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="574c4-p104">O modo de entrada de dados da tabela. Isso se aplica somente às tabelas abertas em modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>.</span><span class="sxs-lookup"><span data-stu-id="574c4-p104">The data entry mode for the table. This applies only to tables opened in Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="574c4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="574c4-124">Remarks</span></span>

<span data-ttu-id="574c4-125">Esta ação é semelhante a clicar duas vezes em uma tabela do Painel de Navegação ou a clicar com o botão direito do mouse na tabela do Painel de Navegação e selecionar um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="574c4-125">This action is similar to double-clicking the table in the Navigation Pane, or right-clicking the table in the Navigation Pane and selecting a view.</span></span>

> [!TIP]
> <span data-ttu-id="574c4-p105">[!DICA] Você pode arrastar uma tabela do Painel de Navegação para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirTabela** que abre a tabela em modo Folha de Dados.</span><span class="sxs-lookup"><span data-stu-id="574c4-p105">You can drag a table from the Navigation Pane to a macro action row. This automatically creates an **OpenTable** action that opens the table in Datasheet view.</span></span>

<span data-ttu-id="574c4-128">Para executar a ação **AbrirTabela** em um módulo do VBA (Visual Basic for Applications), use o método **OpenTable** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="574c4-128">To run the **OpenTable** action in a Visual Basic for Applications (VBA) module, use the **OpenTable** method of the **DoCmd** object.</span></span>

