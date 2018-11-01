---
title: Ação da macro ExecutarCódigo
TOCTitle: RunCode Macro Action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e06d3ebb014cc38b19e37098b217bd072af4434a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870958"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="6fbaf-102">Ação da macro ExecutarCódigo</span><span class="sxs-lookup"><span data-stu-id="6fbaf-102">RunCode Macro Action</span></span>


<span data-ttu-id="6fbaf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6fbaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6fbaf-104">Use a ação **ExecutarCódigo** para chamar um procedimento Function do VBA(Visual Basic for Applications).</span><span class="sxs-lookup"><span data-stu-id="6fbaf-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="6fbaf-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="6fbaf-105">Setting</span></span>

<span data-ttu-id="6fbaf-106">A ação **ExecutarCódigo** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6fbaf-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="6fbaf-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6fbaf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fbaf-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fbaf-109"><strong>Nome da função</strong></span><span class="sxs-lookup"><span data-stu-id="6fbaf-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6fbaf-p101">O nome do procedimento Function do VBA a ser chamado. Coloque entre parênteses todos os argumentos da função. Digite o nome da função na caixa <strong>Nome da Função</strong>, na seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. Este é um argumento obrigatório.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-p101">The name of the VBA Function procedure to call. Enclose any function arguments in parentheses. Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="6fbaf-p102">Em um banco de dados do Access (.mdb ou .accdb), clique no botão <STRONG>Compilar</STRONG> para usar o Construtor de Expressões para selecionar uma função para esse argumento. Na lista do Construtor de Expressões, clique na função desejada.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-p102">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to select a function for this argument. Click the desired function in the list in the Expression Builder.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6fbaf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fbaf-116">Remarks</span></span>

<span data-ttu-id="6fbaf-117">Os procedimentos Function definidos pelo usuário são armazenados nos módulos do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="6fbaf-118">Você deve incluí-los entre parênteses, mesmo que o procedimento Function não tenha nenhum argumento. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6fbaf-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="6fbaf-119">Ao contrário de nomes de função definida pelo usuário usados para configurações de propriedade de evento, o nome da função no argumento **Nome da função** não começa com um sinal de igualdade (**=**).</span><span class="sxs-lookup"><span data-stu-id="6fbaf-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="6fbaf-120">O Access ignora o valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-120">Access ignores the return value of the function.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6fbaf-121">[!OBSERVAçãO] Não será possível chamar um procedimento Function em uma macro se o nome da função for igual ao nome do módulo.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="6fbaf-p103">[!DICA] Para executar um procedimento Sub ou um procedimento de evento escrito em Visual Basic, crie um procedimento Function que possa chamar o procedimento Sub ou o procedimento de evento. Use a ação <STRONG>ExecutarCódigo</STRONG> para executar o procedimento Function.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-p103">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure. Then use the <STRONG>RunCode</STRONG> action to run the Function procedure.</span></span></P>



<span data-ttu-id="6fbaf-p104">Se você usar a ação **ExecutarCódigo** para chamar uma função, o Access pesquisará a função com o nome especificado pelo argumento **Nome da Função** nos módulos padrão do banco de dados. Entretanto, quando essa ação for executada em resposta ao acionamento de um comando de menu em um formulário ou relatório, ou em resposta a um evento em um formulário ou relatório, o Access primeiro pesquisará a função no módulo de classe do formulário ou do relatório e depois nos módulos padrão. O Access não pesquisa os módulos de classe mostrados na área **Módulos** do Painel de Navegação para localizar a função especificada pelo argumento **Nome da Função**.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-p104">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database. However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules. Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="6fbaf-p105">Esta ação não está disponível em um módulo do VBA. Em vez disso, execute o procedimento Function desejado diretamente no VBA.</span><span class="sxs-lookup"><span data-stu-id="6fbaf-p105">This action isn't available in a VBA module. Instead, run the desired Function procedure directly in VBA.</span></span>

