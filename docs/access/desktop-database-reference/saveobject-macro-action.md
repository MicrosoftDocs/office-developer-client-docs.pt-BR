---
title: Ação da macro SalvarObjeto
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 33180aa296fc40c05a3fc50da697aadbf6ada77e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997158"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="26a67-102">Ação da macro SalvarObjeto</span><span class="sxs-lookup"><span data-stu-id="26a67-102">SaveObject macro action</span></span>

<span data-ttu-id="26a67-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="26a67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26a67-p101">Você pode usar a ação **SalvarObjeto** para salvar um objeto do Access especificado ou, se nenhum estiver especificado, o objeto ativo. Em alguns casos, pode também salvar o objeto ativo com um novo nome (tem o mesmo efeito do comando **Salvar como** na **Barra de Ferramentas de Acesso Rápido**).</span><span class="sxs-lookup"><span data-stu-id="26a67-p101">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="26a67-106">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="26a67-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="26a67-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="26a67-107">Setting</span></span>

<span data-ttu-id="26a67-108">A ação **SalvarObjeto** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="26a67-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26a67-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="26a67-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="26a67-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="26a67-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26a67-111"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-p102">O tipo de objeto que você deseja salvar. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Para selecionar o objeto ativo, deixe este argumento em branco. Se você selecionar um tipo de objeto no argumento, selecione um nome de objeto existente no argumento <strong>Nome do Objeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="26a67-p102">The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26a67-116"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-117">O nome do objeto a ser salvo.</span><span class="sxs-lookup"><span data-stu-id="26a67-117">The name of the object to be saved.</span></span> <span data-ttu-id="26a67-118">A caixa <strong>Nome do Objeto</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="26a67-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="26a67-119">Se você deixar vazio o argumento de <strong>Tipo de objeto</strong> , você pode deixar este argumento em branco para salvar o objeto ativo ou, em alguns casos, insira um novo nome neste argumento para salvar o objeto ativo com esse nome.</span><span class="sxs-lookup"><span data-stu-id="26a67-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="26a67-120">Se digitar um novo nome, você deverá cumprir as convenções de nomeação padrão para objetos do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="26a67-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="26a67-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="26a67-121">Remarks</span></span>

<span data-ttu-id="26a67-p104">A ação **SalvarObjeto** funciona em todos os objetos de banco de dados que o usuário possa explicitamente abrir e salvar. O objeto especificado deve estar aberto para que a ação **SalvarObjeto** tenha qualquer efeito no objeto. Essa ação é semelhante à ação de selecionar um objeto e salvá-lo clicando em **Salvar** na **Barra de Ferramentas de Acesso Rápido**. Deixar em branco o argumento **Tipo de Objeto** e inserir um novo nome no argumento **Nome do Objeto** tem o mesmo efeito de clicar em **Salvar Como** na **Barra de Ferramentas de Acesso Rápido** e digitar um novo nome para o objeto ativo. O uso da ação **SalvarObjeto** permite que você especifique um objeto a ser salvo e execute um comando **Salvar Como** em uma macro.</span><span class="sxs-lookup"><span data-stu-id="26a67-p104">The **SaveObject** action works on all database objects that the user can explicitly open and save. The specified object must be open for the **SaveObject** action to have any effect on the object. This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**. Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object. Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="26a67-127">[!OBSERVAçãO] A ação **SalvarObjeto** não pode ser utilizada para salvar nenhum dos seguintes itens com um novo nome:</span><span class="sxs-lookup"><span data-stu-id="26a67-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="26a67-128">Um formulário no modo formulário ou modo de folha de dados</span><span class="sxs-lookup"><span data-stu-id="26a67-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="26a67-129">Um relatório no modo Visualizar impressão</span><span class="sxs-lookup"><span data-stu-id="26a67-129">A report in Print Preview</span></span>
> - <span data-ttu-id="26a67-130">Um módulo</span><span class="sxs-lookup"><span data-stu-id="26a67-130">A module</span></span>
> - <span data-ttu-id="26a67-131">Um modo de exibição do servidor no modo de folha de dados ou no modo Visualizar impressão</span><span class="sxs-lookup"><span data-stu-id="26a67-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="26a67-132">Página no modo de exibição de página de acesso a um dado</span><span class="sxs-lookup"><span data-stu-id="26a67-132">A data access page in Page view</span></span>
> - <span data-ttu-id="26a67-133">Uma tabela no modo folha de dados ou no modo Visualizar impressão</span><span class="sxs-lookup"><span data-stu-id="26a67-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="26a67-134">Uma consulta no modo folha de dados ou visualizar impressão</span><span class="sxs-lookup"><span data-stu-id="26a67-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="26a67-135">Um procedimento armazenado no modo folha de dados ou no modo Visualizar impressão</span><span class="sxs-lookup"><span data-stu-id="26a67-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="26a67-136">A ação **SalvarObjeto**, esteja ela carregada em uma macro em execução no banco de dados atual ou em um banco de dados biblioteca, sempre salva o objeto especificado ou o objeto ativo do banco de dados em que o objeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="26a67-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="26a67-p105">Se você salvar o objeto com um novo nome, mas o nome for o mesmo de um objeto existente desse tipo, uma caixa de diálogo perguntará se você deseja substituir o objeto existente. Se tiver definido o argumento **Avisos ativos** da ação **DefinirAvisos** como **Não**, a caixa de diálogo não será exibida e o objeto antigo será automaticamente substituído.</span><span class="sxs-lookup"><span data-stu-id="26a67-p105">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="26a67-139">Para executar a ação **SalvarObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **Salvar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="26a67-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

