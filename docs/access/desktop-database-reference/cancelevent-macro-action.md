---
title: Ação da macro CancelarEvento
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7999d2acd19fd1f6aa4d7dd9dccd88b7ffea88a7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925322"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="066a7-102">Ação da macro CancelarEvento</span><span class="sxs-lookup"><span data-stu-id="066a7-102">CancelEvent macro action</span></span>


<span data-ttu-id="066a7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="066a7-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="066a7-104">Você pode usar a ação **CancelarEvento** para cancelar o evento que ativou o acesso ao executar a macro que contém essa ação.</span><span class="sxs-lookup"><span data-stu-id="066a7-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="066a7-105">O nome da macro é a configuração de uma propriedade de evento como **AntesDeAtualizar**, **AoAbrir**, **OnUnload** ou **OnPrint**.</span><span class="sxs-lookup"><span data-stu-id="066a7-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="066a7-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="066a7-106">Setting</span></span>

<span data-ttu-id="066a7-107">A ação **CancelarEvento** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="066a7-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="066a7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="066a7-108">Remarks</span></span>

<span data-ttu-id="066a7-p102">Em um formulário, normalmente é usada a ação **CancelarEvento** em uma macro de validação com a propriedade de evento **AntesDeAtualizar**. Quando um usuário insere dados em um controle ou registro, o Access executa a macro antes de adicioná-los ao banco de dados. Se os dados falharem nas condições de validação da macro, a ação **CancelarEvento** cancelará o processo de atualização antes de ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="066a7-p102">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property. When a user enters data in a control or record, Access runs the macro before adding the data to the database. If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="066a7-112">Geralmente, você usa esta ação com a ação **CaixadeMensagem** para indicar que os dados falharam nas condições de validação e para fornecer informações úteis sobre o tipo de dados que deve ser inserido.</span><span class="sxs-lookup"><span data-stu-id="066a7-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="066a7-113">Os eventos a seguir podem ser cancelados pala ação **CancelarEvento**.</span><span class="sxs-lookup"><span data-stu-id="066a7-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="066a7-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a7-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066a7-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-121"><strong>Filtrar</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a7-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-124"><strong>Formato</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-125"><strong>Imprimir</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066a7-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="066a7-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a7-129"><strong>Delete</strong></span><span class="sxs-lookup"><span data-stu-id="066a7-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="066a7-130">[!OBSERVAçãO] Você pode usar a ação **CancelarEvento** com o evento **PressionarMouse** somente para cancelar o evento que ocorre ao clicar com o botão direito do mouse em um objeto.</span><span class="sxs-lookup"><span data-stu-id="066a7-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="066a7-131">Se a configuração da propriedade de evento **OnDblClick** de um controle especificar uma macro que contém a ação **CancelarEvento**, esta cancelará o evento **ClicarDuasVezes**.</span><span class="sxs-lookup"><span data-stu-id="066a7-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="066a7-p103">Para eventos que podem ser cancelados, o comportamento padrão do evento (ou seja, o que o Access normalmente faz na ocorrência do evento) ocorre após a execução da macro do evento. Isso permite cancelar o comportamento padrão. Por exemplo, quando você clica duas vezes em uma palavra sobre a qual está o ponto de inserção em uma caixa de texto, o Access normalmente seleciona a palavra. É possível cancelar esse comportamento padrão na macro do evento **ClicarDuasVezes** e executar alguma outra ação, como abrir um formulário que contém informações sobre os dados na caixa de texto. Para eventos que não podem ser cancelados, o comportamento padrão ocorre antes de a macro ser executada.</span><span class="sxs-lookup"><span data-stu-id="066a7-p103">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs. This enables you to cancel the default behavior. For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word. You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box. For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="066a7-p104">[!OBSERVAçãO] Se a propriedade de evento **OnUnload** de um formulário especificar uma macro que executa uma ação **CancelarEvento**, você não conseguirá fechar o formulário. Será necessário corrigir a condição que causou a execução da ação **CancelarEvento** ou abrir a macro e excluir a ação **CancelarEvento**. Se o formulário for restrito, você não conseguirá abrir a macro.</span><span class="sxs-lookup"><span data-stu-id="066a7-p104">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form. You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action. If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="066a7-140">Para executar a ação **CancelarEvento** em um módulo do VBA (Visual Basic for Applications), use o método **CancelEvent** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="066a7-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="066a7-141">Exemplo</span><span class="sxs-lookup"><span data-stu-id="066a7-141">Example</span></span>

<span data-ttu-id="066a7-142"> Validar dados usando uma macro</span><span class="sxs-lookup"><span data-stu-id="066a7-142">Validate data by using a macro</span></span>

<span data-ttu-id="066a7-p105">A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato certo para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro. Ela retornará o controle de Código Postal, em que será possível corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.</span><span class="sxs-lookup"><span data-stu-id="066a7-p105">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the Postal Code control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="066a7-149">Condição</span><span class="sxs-lookup"><span data-stu-id="066a7-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="066a7-150">Ação</span><span class="sxs-lookup"><span data-stu-id="066a7-150">Action</span></span></p></th>
<th><p><span data-ttu-id="066a7-151">Argumentos: Configuração</span><span class="sxs-lookup"><span data-stu-id="066a7-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="066a7-152">Comentário</span><span class="sxs-lookup"><span data-stu-id="066a7-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="066a7-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="066a7-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="066a7-154">PararMacro</span><span class="sxs-lookup"><span data-stu-id="066a7-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="066a7-155">Se PaísRegião for <strong>Nulo</strong>, o código postal não poderá ser validado.</span><span class="sxs-lookup"><span data-stu-id="066a7-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a7-156">[Paísregião] No (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e Compr ([CEP]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="066a7-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="066a7-157">CaixaDeMensagem</span><span class="sxs-lookup"><span data-stu-id="066a7-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="066a7-158">Mensagem: O código postal precisa ter 5 caracteres. 

</span><span class="sxs-lookup"><span data-stu-id="066a7-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="066a7-159">Alarme sonoro: <strong>Sim</strong> tipo: <strong>informação</strong> título: erro de CEP</span><span class="sxs-lookup"><span data-stu-id="066a7-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="066a7-160">Se o código postal não tiver 5 caracteres, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="066a7-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066a7-161">...</span><span class="sxs-lookup"><span data-stu-id="066a7-161"></span></span></p></td>
<td><p><span data-ttu-id="066a7-162">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="066a7-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="066a7-163">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="066a7-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="066a7-164">IrParaControle</span><span class="sxs-lookup"><span data-stu-id="066a7-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="066a7-165">Nome do Controle: CEP</span><span class="sxs-lookup"><span data-stu-id="066a7-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066a7-166">[Paísregião] No (&quot;Austrália&quot;,&quot;Cingapura&quot;) e Compr ([CEP]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="066a7-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="066a7-167">CaixaDeMensagem</span><span class="sxs-lookup"><span data-stu-id="066a7-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="066a7-168">Mensagem: O código postal precisa ter 4 caracteres. 

</span><span class="sxs-lookup"><span data-stu-id="066a7-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="066a7-169">Alarme sonoro: <strong>Sim</strong> tipo: <strong>informação</strong> título: erro de CEP</span><span class="sxs-lookup"><span data-stu-id="066a7-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="066a7-170">Se o código postal não tiver 4 caracteres, exiba uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="066a7-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a7-171">...</span><span class="sxs-lookup"><span data-stu-id="066a7-171"></span></span></p></td>
<td><p><span data-ttu-id="066a7-172">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="066a7-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="066a7-173">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="066a7-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="066a7-174">IrParaControle</span><span class="sxs-lookup"><span data-stu-id="066a7-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="066a7-175">Nome do Controle: CEP</span><span class="sxs-lookup"><span data-stu-id="066a7-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="066a7-176">([Paísregião] = &quot;Canadá&quot;) E ([CEP] não igual a&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="066a7-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="066a7-177">CaixaDeMensagem</span><span class="sxs-lookup"><span data-stu-id="066a7-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="066a7-178">Mensagem: O código postal não é válido.</span><span class="sxs-lookup"><span data-stu-id="066a7-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="066a7-179">Exemplo de código canadense: H1J 1C3 alarme sonoro: <strong>Sim</strong> tipo: <strong>informação</strong> título: erro de código Postal</span><span class="sxs-lookup"><span data-stu-id="066a7-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="066a7-p109">Se o código postal não estiver correto para Canadá, exiba uma mensagem. (Exemplo de código de Canadá: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="066a7-p109">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="066a7-182">...</span><span class="sxs-lookup"><span data-stu-id="066a7-182"></span></span></p></td>
<td><p><span data-ttu-id="066a7-183">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="066a7-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="066a7-184">Cancele o evento.</span><span class="sxs-lookup"><span data-stu-id="066a7-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

