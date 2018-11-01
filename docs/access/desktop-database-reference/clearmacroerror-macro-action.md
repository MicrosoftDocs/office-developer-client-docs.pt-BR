---
title: Ação de macro LimparErrodeMacro
TOCTitle: ClearMacroError Macro Action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e9b8232f24a837466529f8ce04f9f830af72e7a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870188"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="294db-102">Ação de macro LimparErrodeMacro</span><span class="sxs-lookup"><span data-stu-id="294db-102">ClearMacroError Macro Action</span></span>


<span data-ttu-id="294db-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="294db-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="294db-104">Você pode usar a ação **LimparErrodeMacro** para limpar as informações sobre um erro armazenado no objeto **MacroError**.</span><span class="sxs-lookup"><span data-stu-id="294db-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="294db-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="294db-105">Setting</span></span>

<span data-ttu-id="294db-106">A ação **LimparErrodeMacro** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="294db-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="294db-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="294db-107">Remarks</span></span>

  - <span data-ttu-id="294db-108">Quando ocorre um erro em uma macro, informações sobre o erro são armazenadas no objeto **MacroError**.</span><span class="sxs-lookup"><span data-stu-id="294db-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="294db-109">Se você não tiver usado a ação **[AoOcorrerErro](onerror-macro-action.md)** para suprimir as mensagens de erro, a macro é interrompida e as informações de erro será exibido em uma mensagem de erro padrão.</span><span class="sxs-lookup"><span data-stu-id="294db-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="294db-110">No entanto, se você tiver usado a ação **AoOcorrerErro** para suprimir as mensagens de erro, você talvez queira usar as informações armazenadas no objeto **MacroError** em uma condição ou em uma mensagem de erro personalizada.</span><span class="sxs-lookup"><span data-stu-id="294db-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
    <span data-ttu-id="294db-p102">Depois que um erro for manipulado, as informações do objeto **MacroError** estarão desatualizadas, portanto é uma ótima ideia limpar o objeto usando a ação **LimparErrodeMacro**. Esse procedimento redefinirá o número de erro no objeto **MacroError** como 0 e limpará todas as outras informações sobre o erro armazenado no objeto, como descrição do erro, nome da macro, nome da ação, condição e argumentos. Dessa maneira, você poderá inspecionar o objeto **MacroError** outra vez mais tarde para saber se ocorreu outro erro.</span><span class="sxs-lookup"><span data-stu-id="294db-p102">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action. Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments. This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

  - <span data-ttu-id="294db-114">O objeto **MacroError** é limpo automaticamente quando qualquer macro chega ao fim, por isso não é necessário usar a ação **LimparErrodeMacro** no fim de uma macro.</span><span class="sxs-lookup"><span data-stu-id="294db-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

  - <span data-ttu-id="294db-p103">O objeto **MacroError** contém informações somente sobre um erro de cada vez. Se ocorrer mais de um erro em uma macro, o objeto **MacroError** conterá informações somente sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="294db-p103">The **MacroError** object contains information about only one error at a time. If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

  - <span data-ttu-id="294db-117">Para executar a ação **LimparErrodeMacro** em um módulo do VBA, use o método **ClearMacroError** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="294db-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="294db-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="294db-118">Example</span></span>

<span data-ttu-id="294db-119">A macro a seguir usa a ação **AoOcorrerErro** com o argumento **Próximo** para suprimir mensagens de erro, além de usar a ação **AbrirFormulário** para abrir um formulário.</span><span class="sxs-lookup"><span data-stu-id="294db-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="294db-120">Para este exemplo, um erro é criado deliberadamente usando a ação **IrParaRegistro** para ir até o registro anterior.</span><span class="sxs-lookup"><span data-stu-id="294db-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="294db-121">A condição \*\* \[MacroError\].\[ Número\]\<\>0\*\* testa o objeto **MacroError** .</span><span class="sxs-lookup"><span data-stu-id="294db-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="294db-122">Se um erro tiver ocorrido, o número do erro será diferente de zero, e a ação **CaixadeMensagem** será executada.</span><span class="sxs-lookup"><span data-stu-id="294db-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="294db-123">A caixa de mensagem exibirá o nome da ação que causou o erro (nesse caso, a ação **IrParaRegistro** ) e o número do erro será exibido.</span><span class="sxs-lookup"><span data-stu-id="294db-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="294db-124">Por fim, a execução da ação **LimparErrodeMacro** limpa o objeto **ErrodeMacro**.</span><span class="sxs-lookup"><span data-stu-id="294db-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="294db-125">Condição</span><span class="sxs-lookup"><span data-stu-id="294db-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="294db-126">Ação</span><span class="sxs-lookup"><span data-stu-id="294db-126">Action</span></span></p></th>
<th><p><span data-ttu-id="294db-127">Argumentos</span><span class="sxs-lookup"><span data-stu-id="294db-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="294db-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="294db-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="294db-129"><strong>Ir para</strong>: <strong>Próximo</strong></span><span class="sxs-lookup"><span data-stu-id="294db-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="294db-130"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="294db-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="294db-131"><strong>Nome do formulário</strong>: Formuláriodacategoria<strong>modo de exibição</strong>: <strong>Modo FormWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="294db-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="294db-132"><strong>IrParaRegistro</strong></span><span class="sxs-lookup"><span data-stu-id="294db-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="294db-133"><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: Formuláriodacategoria<strong>registro</strong>: anterior</span><span class="sxs-lookup"><span data-stu-id="294db-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="294db-134">[Errodemacro]. [Número] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="294db-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="294db-135"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="294db-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="294db-136"><strong>Mensagem</strong>: =&quot;erro # &quot; &amp; [Errodemacro]. [Número] &amp; &quot; na &quot; &amp; [Errodemacro]. [NomeDaAção] &amp; &quot; ação. &quot; <strong>Alarme sonoro</strong>: <strong>YesType</strong>: informações</span><span class="sxs-lookup"><span data-stu-id="294db-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="294db-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="294db-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

