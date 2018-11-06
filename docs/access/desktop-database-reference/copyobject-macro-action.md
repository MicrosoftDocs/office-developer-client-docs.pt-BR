---
title: Ação da macro CopiarObjeto
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 79f4e59309a4f224498421f2407df187d3b9e728
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998060"
---
# <a name="copyobject-macro-action"></a><span data-ttu-id="930f7-102">Ação da macro CopiarObjeto</span><span class="sxs-lookup"><span data-stu-id="930f7-102">CopyObject macro action</span></span>

<span data-ttu-id="930f7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="930f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="930f7-p101">Você pode usar a ação **CopiarObjeto** para copiar o objeto de banco de dados especificado para um banco de dados do Access diferente ou para o mesmo banco de dados ou o projeto do Access com um novo nome. Por exemplo, é possível executar cópia ou backup de um objeto existente em outro banco de dados ou rapidamente criar um objeto semelhante com algumas alterações.</span><span class="sxs-lookup"><span data-stu-id="930f7-p101">You can use the **CopyObject** action to copy the specified database object to a different Access database or to the same database or Access project under a new name. For example, you can copy or back up an existing object in another database or quickly create a similar object with a few changes.</span></span>

> [!NOTE]
> <span data-ttu-id="930f7-106">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="930f7-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="930f7-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="930f7-107">Setting</span></span>

<span data-ttu-id="930f7-108">A ação **CopiarObjeto** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="930f7-108">The **CopyObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="930f7-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="930f7-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="930f7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="930f7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="930f7-111"><strong>Banco de Dados de Destino</strong></span><span class="sxs-lookup"><span data-stu-id="930f7-111"><strong>Destination Database</strong></span></span></p></td>
<td><p><span data-ttu-id="930f7-p102">Um caminho e nome de arquivo válidos para o banco de dados de destino. Insira o caminho e nome de arquivo na caixa <strong>Banco de Dados de Destino</strong> na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Deixe este argumento em branco se desejar selecionar o banco de dados atual. 

</span><span class="sxs-lookup"><span data-stu-id="930f7-p102">A valid path and file name for the destination database. Enter the path and file name in the <strong>Destination Database</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank if you want to select the current database.</span></span></p><p><span data-ttu-id="930f7-115"><strong>Observação</strong>: este argumento só está disponível no ambiente de banco de dados do Access.</span><span class="sxs-lookup"><span data-stu-id="930f7-115"><strong>NOTE</strong>: This argument is only available in the Access database environment.</span></span> <span data-ttu-id="930f7-116">Ao usar essa ação em um ambiente de projeto do Access (. adp), o argumento de banco de dados de destino deve estar em branco.</span><span class="sxs-lookup"><span data-stu-id="930f7-116">When using this action in an Access project environment (.adp), the Destination Database argument must be blank.</span></span></p>
<p><span data-ttu-id="930f7-117">Se você executar uma macro que contém a ação <strong>CopiarObjeto</strong> em um banco de dados biblioteca e deixar este argumento em branco, o Microsoft Office Access 2007 copiará o objeto para o banco de dados biblioteca.</span><span class="sxs-lookup"><span data-stu-id="930f7-117">If you run a macro containing the <strong>CopyObject</strong> action in a library database and leave this argument blank, Microsoft Office Access 2007 will copy the object into the library database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="930f7-118"><strong>Novo Nome</strong></span><span class="sxs-lookup"><span data-stu-id="930f7-118"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="930f7-p104">Um novo nome para o objeto. Ao copiar para um banco de dados diferente, deixe este argumento em branco para manter o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="930f7-p104">A new name for the object. When copying to a different database, leave this argument blank to keep the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="930f7-121"><strong>Tipo do Objeto de Origem</strong></span><span class="sxs-lookup"><span data-stu-id="930f7-121"><strong>Source Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="930f7-p105">O tipo de objeto que deseja copiar. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong>. Para copiar o objeto selecionado no Painel de Navegação, deixe este argumento em branco.</span><span class="sxs-lookup"><span data-stu-id="930f7-p105">The object type you want to copy. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To copy the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="930f7-125"><strong>Nome do Objeto de Origem</strong></span><span class="sxs-lookup"><span data-stu-id="930f7-125"><strong>Source Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="930f7-126">O nome do objeto a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="930f7-126">The name of the object to be copied.</span></span> <span data-ttu-id="930f7-127">Na caixa <strong>Nome do objeto de origem</strong> mostra todos os objetos no banco de dados do tipo selecionado pelo argumento <strong>Tipo de objeto de origem</strong> .</span><span class="sxs-lookup"><span data-stu-id="930f7-127">The <strong>Source Object Name</strong> box shows all objects in the database of the type selected by the <strong>Source Object Type</strong> argument.</span></span> <span data-ttu-id="930f7-128">Na caixa <strong>Nome do objeto de origem</strong> , clique no objeto a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="930f7-128">In the <strong>Source Object Name</strong> box, click the object to copy.</span></span> <span data-ttu-id="930f7-129">Se você deixar vazio o argumento de <strong>Tipo de objeto de origem</strong> , deixe este argumento também em branco.</span><span class="sxs-lookup"><span data-stu-id="930f7-129">If you leave the <strong>Source Object Type</strong> argument blank, leave this argument blank also.</span></span> <span data-ttu-id="930f7-130">Se você executar uma macro que contém a ação <strong>CopiarObjeto</strong> em um banco de dados biblioteca, o Access procurará o objeto com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="930f7-130">If you run a macro containing the <strong>CopyObject</strong> action in a library database, Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="930f7-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="930f7-131">Remarks</span></span>

<span data-ttu-id="930f7-132">Você precisa digitar um valor para um dos argumentos **Banco de Dados de Destino** e **Novo Nome** para esta ação, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="930f7-132">You must enter a value for either one or both of the **Destination Database** and **New Name** arguments for this action.</span></span>

<span data-ttu-id="930f7-p107">Se você deixar os argumentos **Tipo do Objeto de Origem** e **Nome do Objeto de Origem** em branco, o Access copiará o objeto selecionado no Painel de Navegação. Para selecionar um objeto no Painel de Navegação, use a ação **SelecionarObjeto** com o argumento No Painel de Navegação definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="930f7-p107">If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.</span></span>

<span data-ttu-id="930f7-135">A ação **CopiarObjeto** equivale a seguir estas etapas manualmente:</span><span class="sxs-lookup"><span data-stu-id="930f7-135">The **CopyObject** action is similar to performing the following steps manually:</span></span>

1. <span data-ttu-id="930f7-136">Selecione um objeto no Painel de Navegação.</span><span class="sxs-lookup"><span data-stu-id="930f7-136">Select an object in the Navigation Pane.</span></span>

2. <span data-ttu-id="930f7-137">On the Home tab, in the Clipboard group, click Copy.</span><span class="sxs-lookup"><span data-stu-id="930f7-137">On the Home tab, in the Clipboard group, click Copy.</span></span>

3. <span data-ttu-id="930f7-p108">Na mesma guia, clique em **Colar**.A caixa de diálogo **Colar como** é exibida para você poder dar um novo nome ao objeto. A ação **CopiarObjeto** executa todas essas etapas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="930f7-p108">On the same tab, click **Paste**.The **Paste As** dialog box appears so that you can give the object a new name. The **CopyObject** action performs all of these steps automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="930f7-140">[!OBSERVAçãO] Ao copiar páginas de acesso a dados, a ação **CopiarObjeto** copia somente o link para o arquivo .htm associado, e não o arquivo em si.</span><span class="sxs-lookup"><span data-stu-id="930f7-140">When copying data access pages, the **CopyObject** action copies only the link to the associated .htm file, not the file itself.</span></span>

<span data-ttu-id="930f7-p109">O caminho e nome de arquivo do banco de dados de destino precisam existir antes de a macro executar a ação **CopiarObjeto**. Se não existirem, o Access exibirá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="930f7-p109">The path and file name of the destination database must exist before the macro runs the **CopyObject** action. If they don't exist, Access displays an error message.</span></span>

<span data-ttu-id="930f7-143">Para executar a ação **CopiarObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **CopyObject** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="930f7-143">To run the **CopyObject** action in a Visual Basic for Applications (VBA) module, use the **CopyObject** method of the **DoCmd** object.</span></span>

<span data-ttu-id="930f7-p110">Você também pode copiar manualmente um objeto selecionado no Painel de Navegação, ou um objeto que está aberto no momento, clicando na guia **Arquivo** e clicando em **Salvar como**. Esse comando fará uma cópia do objeto somente no banco de dados atual. Na caixa de diálogo **Salvar como**, digite o nome da cópia e escolha o tipo de objeto no qual ela será salva. Se o objeto original já tiver sido salvo e você salvá-lo no banco de dados atual com o novo nome, a versão original ainda existirá com o antigo nome.</span><span class="sxs-lookup"><span data-stu-id="930f7-p110">You can also manually copy an object selected in the Navigation Pane, or an object that is currently open, by clicking the **File** tab and then clicking **Save As**. This command will make a copy of the object in the current database only. In the **Save As** dialog box, enter the name for the copy, and choose what type of object you want to save it as. If the original object has already been saved and you save it in the current database with a new name, the original version still exists with its old name.</span></span>

<span data-ttu-id="930f7-148">Para copiar manualmente um objeto para um banco de dados diferente do Access:</span><span class="sxs-lookup"><span data-stu-id="930f7-148">To manually copy an object to a different Access database:</span></span>

1. <span data-ttu-id="930f7-149">Na guia **Dados Externos**, no grupo **Exportar**, clique em **Mais** e clique em **Banco de Dados do Access**.</span><span class="sxs-lookup"><span data-stu-id="930f7-149">On the **External Data** tab, in the **Export** group, click **More** and then click **Access Database**.</span></span>

2. <span data-ttu-id="930f7-150">Na caixa de diálogo **Exportar - Banco de Dados do Access**, digite o nome de arquivo do banco de dados de destino.-ou-Clique em **Procurar** para exibir a caixa de diálogo **Salvar Arquivo**, localize o banco de dados de destino e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="930f7-150">In the **Export - Access Database** dialog box, enter the file name of the destination database.-or-Click **Browse** to display the **File Save** dialog box, locate the destination database, and then click **Save**.</span></span>

3. <span data-ttu-id="930f7-p111">Na caixa de diálogo **Exportar - Banco de Dados do Access**, clique em **OK**. A caixa de diálogo **Exportar** será exibida.</span><span class="sxs-lookup"><span data-stu-id="930f7-p111">In the **Export - Access Database** dialog box, click **OK**. The **Export** dialog box appears.</span></span>

4. <span data-ttu-id="930f7-p112">Na caixa de diálogo **Exportar**, digite um nome para o objeto no banco de dados de destino. Escolha qualquer opção aplicável, como **Definição e Dados** ou **Somente Definição** para tabelas. Quando tiver concluído, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="930f7-p112">In the **Export** dialog box, enter a name for the object in the destination database. Choose any applicable options, such as **Export Definition and Data** or **Definition Only** for tables. When you are finished, click **OK**.</span></span>

