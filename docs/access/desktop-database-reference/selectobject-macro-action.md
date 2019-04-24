---
title: Ação da macro SelecionarObjeto
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308726"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="4651a-102">Ação da macro SelecionarObjeto</span><span class="sxs-lookup"><span data-stu-id="4651a-102">SelectObject macro action</span></span>

<span data-ttu-id="4651a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4651a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4651a-104">Use a ação **SelecionarObjeto** para selecionar um objeto de banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="4651a-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="4651a-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="4651a-105">Setting</span></span>

<span data-ttu-id="4651a-106">A ação **SelecionarObjeto** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4651a-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4651a-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="4651a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4651a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4651a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4651a-109"><strong>Tipo de Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="4651a-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="4651a-p101">O tipo de objeto de banco de dados a ser selecionado. Clique em <strong>Tabela</strong>, <strong>Consulta</strong>, <strong>Formulário</strong>, <strong>Relatório</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de Acesso a Dados</strong>, <strong>Modo de Exibição do Servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimento Armazenado</strong> ou <strong>Função</strong> na caixa <strong>Tipo de Objeto</strong>, na seção <strong>Argumentos da Ação</strong> do Construtor de Macros. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4651a-p101">The type of database object to select. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4651a-113"><strong>Nome do Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="4651a-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4651a-p102">O nome do objeto a ser selecionado. A caixa <strong>Nome do Objeto</strong> mostra todos os objetos do banco de dados, do tipo selecionado pelo argumento <strong>Tipo de objeto</strong>. Este é um argumento obrigatório, a menos que, no Painel de Navegação, você defina o argumento como <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="4651a-p102">The name of the object to select. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p><p><span data-ttu-id="4651a-117"><strong>Observação</strong>: os nomes de objeto para o <STRONG>modo de exibição do servidor</STRONG>, <STRONG>diagrama</STRONG>ou <STRONG>procedimento armazenado</STRONG> não são exibidos na caixa <STRONG>nome do objeto</STRONG> de um projeto do Access (. adp).</span><span class="sxs-lookup"><span data-stu-id="4651a-117"><strong>NOTE</strong>: The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4651a-118"><strong>No Painel de Navegação</strong></span><span class="sxs-lookup"><span data-stu-id="4651a-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="4651a-p103">Especifica se o Microsoft Access seleciona o objeto no Painel de Navegação. Clique em <strong>Sim</strong> (para selecionar o objeto nesse painel) ou em <strong>Não</strong> (para não selecionar o objeto no Painel de Navegação). O padrão é <strong>Não</strong>.</span><span class="sxs-lookup"><span data-stu-id="4651a-p103">Specifies whether Microsoft Access selects the object in the Navigation Pane. Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane). The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4651a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4651a-122">Remarks</span></span>

<span data-ttu-id="4651a-p104">A ação **SelecionarObjeto** trabalha com qualquer objeto do Access que possa receber o foco. Essa ação aplica o foco no objeto especificado e, caso o objeto esteja oculto, mostra o objeto. Se o objeto for um formulário, a ação **SelecionarObjeto** definirá a propriedade **Visível** do objeto como **Sim** e retornará o formulário ao modo definido pelas respectivas propriedades do formulário (por exemplo, como um formulário modal ou pop-up).</span><span class="sxs-lookup"><span data-stu-id="4651a-p104">The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="4651a-p105">Se o objeto não for aberto em uma das outras janelas do Access, você poderá selecioná-lo no Painel de Navegação definindo o argumento **No Painel de Navegação** como **Sim**. Se você definir o argumento **No Painel de Navegação** como **Não**, uma mensagem de erro aparecerá quando você tentar selecionar um objeto não aberto.</span><span class="sxs-lookup"><span data-stu-id="4651a-p105">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="4651a-p106">Geralmente é possível usar essa ação para selecionar um objeto em que você deseja executar ações adicionais. Por exemplo, se tiver configurado o Access para usar janelas sobrepostas, em vez de documentos com guias, você poderá restaurar um objeto que tenha sido minimizado (usando a ação **RestaurarJanela** ) ou maximizar uma janela que contenha um objeto com o qual queira trabalhar (usando a ação **MaximizarJanela** ).</span><span class="sxs-lookup"><span data-stu-id="4651a-p106">Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="4651a-p107">Ao selecionar um formulário, use as ações **IrParaControle**, **IrParaRegistro** e **IrParaPágina** para ir para áreas específicas do formulário. A ação **IrParaRegistro** também funciona em folhas de dados.</span><span class="sxs-lookup"><span data-stu-id="4651a-p107">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="4651a-132">Para executar a ação **SelecionarObjeto** em um módulo do VBA (Visual Basic for Applications), use o método **SelectObject** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4651a-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

