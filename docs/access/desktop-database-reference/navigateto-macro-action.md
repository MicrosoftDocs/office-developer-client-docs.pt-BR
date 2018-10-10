---
title: Ação de macro NavegarPara
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9a6a59b6c84e9814aeb9b4709d27955f29fd9e1e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463630"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="28758-102">Ação de macro NavegarPara</span><span class="sxs-lookup"><span data-stu-id="28758-102">NavigateTo Macro Action</span></span>


<span data-ttu-id="28758-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="28758-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="28758-p101">Você pode usar a ação **NavegarPara** para controlar a exibição de objetos de banco de dados no Painel de Navegação. Por exemplo, é possível alterar a maneira como os objetos de banco de dados são categorizados, além de filtrá-los para que somente alguns sejam exibidos.</span><span class="sxs-lookup"><span data-stu-id="28758-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="28758-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="28758-106">Setting</span></span>

<span data-ttu-id="28758-107">A ação **NavegarPara** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="28758-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28758-108">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="28758-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="28758-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="28758-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28758-110"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="28758-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="28758-p102">Obrigatório. A categoria pela qual você deseja que o Painel de Navegação exiba os objetos. Clique em <strong>Tipo de Objeto</strong>, <strong>Tabelas e Exibições</strong>, <strong>Data de Modificação</strong>, <strong>Data de Criação</strong> ou <strong>Personalizado</strong> na caixa <strong>Categoria</strong>.</span><span class="sxs-lookup"><span data-stu-id="28758-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28758-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="28758-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="28758-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="28758-115">Optional.</span></span> <span data-ttu-id="28758-116">Os limites de argumento do <strong>grupo</strong> que objetos na categoria aparecem no painel de navegação.</span><span class="sxs-lookup"><span data-stu-id="28758-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="28758-117">Se você deixar vazio o argumento de <strong>grupo</strong> , o painel de navegação exibe todos os objetos de banco de dados, classificados por critérios especificados no argumento <strong>categoria</strong> .</span><span class="sxs-lookup"><span data-stu-id="28758-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="28758-118">Exemplos de argumentos  <strong>Grupo</strong> válidos para os vários argumentos <strong>Categoria</strong> são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="28758-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="28758-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="28758-119">Remarks</span></span>

  - <span data-ttu-id="28758-120">Esta ação é semelhante à seleção de categorias e grupos na barra de título do Painel de Navegação.</span><span class="sxs-lookup"><span data-stu-id="28758-120">This action is similar to selecting categories and groups from the title bar of the Navigation Pane.</span></span>

  - <span data-ttu-id="28758-p104">Os argumentos **Grupo** válidos dependem do argumento **Categoria** usado. Se você digitar um argumento **Grupo** inválido, será exibida uma mensagem de erro.A tabela a seguir contém exemplos de argumentos **Grupo** válidos para cada argumento **Categoria**.</span><span class="sxs-lookup"><span data-stu-id="28758-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="28758-123">Argumento Categoria</span><span class="sxs-lookup"><span data-stu-id="28758-123">Category argument</span></span></p></th>
    <th><p><span data-ttu-id="28758-124">Argumentos Grupo de exemplo</span><span class="sxs-lookup"><span data-stu-id="28758-124">Example Group arguments</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="28758-125">Tipo de Objeto</span><span class="sxs-lookup"><span data-stu-id="28758-125">Object Type</span></span></p></td>
    <td><p><span data-ttu-id="28758-126">Tabelas; Formulários; Consultas; Páginas; Macros; Módulos</span><span class="sxs-lookup"><span data-stu-id="28758-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="28758-127">Tabelas e Exibições</span><span class="sxs-lookup"><span data-stu-id="28758-127">Tables and Views</span></span></p></td>
    <td><p><span data-ttu-id="28758-128">Nomes de tabelas específicas do banco de dados</span><span class="sxs-lookup"><span data-stu-id="28758-128">Names of specific tables in your database</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="28758-129">Data de Modificação</span><span class="sxs-lookup"><span data-stu-id="28758-129">Modified Date</span></span></p></td>
    <td><p><span data-ttu-id="28758-130">Hoje; Ontem; Mês Passado; Mais Antiga</span><span class="sxs-lookup"><span data-stu-id="28758-130">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="28758-131">Data de Criação</span><span class="sxs-lookup"><span data-stu-id="28758-131">Created Date</span></span></p></td>
    <td><p><span data-ttu-id="28758-132">Hoje; Ontem; Mês Passado; Mais Antiga</span><span class="sxs-lookup"><span data-stu-id="28758-132">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="28758-133">Categoria Personalizado</span><span class="sxs-lookup"><span data-stu-id="28758-133">Custom category</span></span></p></td>
    <td><p><span data-ttu-id="28758-134">Nomes de grupos que você criou para a categoria personalizada especificada</span><span class="sxs-lookup"><span data-stu-id="28758-134">Names of groups you have created for the specified custom category</span></span></p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="28758-135">Para executar a ação **NavegarPara** em um módulo do VBA, use o método **NavigateTo** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="28758-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="28758-p105">[!OBSERVAçãO] Para navegar até o nível superior de uma categoria (por exemplo, <STRONG>Todas as Tabelas</STRONG>, <STRONG>Todos os Objetos do Access</STRONG> ou <STRONG>Todas as Datas</STRONG>), é necessário deixar o argumento Grupo em branco. Por exemplo, quando o argumento <STRONG>Categoria</STRONG> é <STRONG>Tipo de Objeto</STRONG>, a inserção de <STRONG>Todos os Objetos do Access</STRONG> como um argumento <STRONG>Grupo</STRONG> resulta em erro.</span><span class="sxs-lookup"><span data-stu-id="28758-p105">To navigate to the top level of a category (for example, <STRONG>All Tables</STRONG>, <STRONG>All Access Objects</STRONG>, or <STRONG>All Dates</STRONG>), you must leave the Group argument blank. For example, when the <STRONG>Category</STRONG> argument is <STRONG>Object Type</STRONG>, entering <STRONG>All Access Objects</STRONG> as a <STRONG>Group</STRONG> argument results in an error.</span></span></P>


