---
title: Ação da macro AbrirMódulodoVisualBasic
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701694"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="e7815-102">Ação da macro AbrirMódulodoVisualBasic</span><span class="sxs-lookup"><span data-stu-id="e7815-102">OpenVisualBasicModule macro action</span></span>

<span data-ttu-id="e7815-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7815-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7815-p101">Você pode usar a ação **AbrirMódulodoVisualBasic** para abrir um módulo do VBA (Visual Basic for Applications) especificado em um procedimento especificado. Este pode ser um procedimento Sub, um procedimento Function ou um procedimento de evento.</span><span class="sxs-lookup"><span data-stu-id="e7815-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="e7815-106">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="e7815-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="e7815-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="e7815-107">Setting</span></span>

<span data-ttu-id="e7815-108">A ação **AbrirMódulodoVisualBasic** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e7815-108">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7815-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="e7815-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e7815-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7815-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7815-111"><strong>Nome do Módulo</strong></span><span class="sxs-lookup"><span data-stu-id="e7815-111"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e7815-112">O nome do módulo que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="e7815-112">The name of the module you want to open.</span></span> <span data-ttu-id="e7815-113">Você pode deixar este argumento em branco se desejar pesquisar todos os módulos padrão no banco de dados para obter um procedimento e abrir o módulo apropriado nesse procedimento.</span><span class="sxs-lookup"><span data-stu-id="e7815-113">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="e7815-114">Se você executar uma macro que contém a ação <strong>AbrirMódulodoVisualBasic</strong> em um banco de dados biblioteca, o Microsoft Access procurará o módulo com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="e7815-114">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7815-115"><strong>Nome do Procedimento</strong></span><span class="sxs-lookup"><span data-stu-id="e7815-115"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="e7815-p103">O nome do procedimento para o qual você deseja abrir o módulo. Se você deixar este argumento em branco, o módulo será aberto na seção Declarações.</span><span class="sxs-lookup"><span data-stu-id="e7815-p103">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e7815-118">[!OBSERVAçãO] Você precisa digitar um nome válido no argumento **Nome do Módulo** ou **Nome do Procedimento**.</span><span class="sxs-lookup"><span data-stu-id="e7815-118">You must enter a valid name in either the **Module Name** or **Procedure Name** argument.</span></span>


## <a name="remarks"></a><span data-ttu-id="e7815-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7815-119">Remarks</span></span>

<span data-ttu-id="e7815-120">Você pode usar esta ação para abrir um procedimento de evento especificando o argumento **Nome do Módulo** e o argumento **Nome do Procedimento**.</span><span class="sxs-lookup"><span data-stu-id="e7815-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="e7815-121">Por exemplo, para abrir o procedimento de evento **Click** do botão ImprimirFatura do formulário Pedidos, defina o argumento **Nome do módulo** **Orders** e defina o argumento **Nome do procedimento** como **ImprimirFatura\_clique**.</span><span class="sxs-lookup"><span data-stu-id="e7815-121">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="e7815-122">Para exibir o procedimento de evento de um formulário ou relatório, este precisa estar aberto.</span><span class="sxs-lookup"><span data-stu-id="e7815-122">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="e7815-123">Da mesma maneira, para abrir um procedimento em um módulo de classe, especifique o nome do módulo, embora não seja necessário abrir o módulo de classe.</span><span class="sxs-lookup"><span data-stu-id="e7815-123">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="e7815-124">Para abrir um procedimento particular, o módulo que o contém precisa estar aberto.</span><span class="sxs-lookup"><span data-stu-id="e7815-124">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="e7815-p105">Esta ação equivale a clicar com o botão direito do mouse em um módulo do Painel de Navegação e clicar em **Modo Design**. Ela também permite especificar um nome de procedimento e pesquisar nos módulos padrão de um banco de dados se há procedimentos.</span><span class="sxs-lookup"><span data-stu-id="e7815-p105">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>

> [!TIP]
> <span data-ttu-id="e7815-p106">[!DICA] Você pode selecionar um módulo do Painel de Navegação e arrastá-lo para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirMódulodoVisualBasic** que abre o módulo na seção Declarações.</span><span class="sxs-lookup"><span data-stu-id="e7815-p106">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span></span>

<span data-ttu-id="e7815-129">Para executar a ação **AbrirMódulodoVisualBasic** em um módulo do VBA, use o método **AbrirMódulo** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e7815-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>

