---
title: Ação de macro RemoverVariávelTemporária
TOCTitle: RemoveTempVar Macro Action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 61d03f23e0fbe04cae49670366f76c02e81d694a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464167"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="be52a-102">Ação de macro RemoverVariávelTemporária</span><span class="sxs-lookup"><span data-stu-id="be52a-102">RemoveTempVar Macro Action</span></span>


<span data-ttu-id="be52a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be52a-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="be52a-104">Você pode usar a ação **RemoverVariávelTemporária** para remover uma única variável temporária criada usando a ação **DefinirVariávelTemporária**.</span><span class="sxs-lookup"><span data-stu-id="be52a-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="be52a-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="be52a-105">Setting</span></span>

<span data-ttu-id="be52a-106">A ação **RemoverVariávelTemporária** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="be52a-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be52a-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="be52a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="be52a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="be52a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be52a-109"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="be52a-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="be52a-110">Insira o nome da variável temporária que deseja remover.</span><span class="sxs-lookup"><span data-stu-id="be52a-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="be52a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="be52a-111">Remarks</span></span>

  - <span data-ttu-id="be52a-p101">É possível ter até 255 variáveis temporárias definidas de cada vez. Se você não remover uma variável temporária, ela permanecerá na memória até o banco de dados ser fechado. É recomendável remover as variáveis temporárias quando acabar de usá-las.</span><span class="sxs-lookup"><span data-stu-id="be52a-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="be52a-115">O Access remove automaticamente todas as variáveis temporárias ao fechar o banco de dados ou projeto.</span><span class="sxs-lookup"><span data-stu-id="be52a-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="be52a-p102">Se você errar na grafia do nome da variável a ser removida, o Access não exibirá um erro. A variável que deveria ser removida permanecerá na memória até o banco de dados ser fechado.</span><span class="sxs-lookup"><span data-stu-id="be52a-p102">If you misspell the name of the variable to be removed, Access does not display an error. The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="be52a-118">Se você criou mais de uma variável temporária e deseja remover todas de uma só vez, use a ação **RemoverTodasVariáveisTemporárias**.</span><span class="sxs-lookup"><span data-stu-id="be52a-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="be52a-119">Para executar a ação **RemoverVariávelTemporária** em um módulo do VBA, use o método **Remove** do objeto **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="be52a-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="be52a-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="be52a-120">Example</span></span>

<span data-ttu-id="be52a-121">A macro a seguir demonstra como criar uma variável temporária, usá-la em uma condição e uma caixa de mensagens e removê-la usando a ação **RemoverVariávelTemporária**.</span><span class="sxs-lookup"><span data-stu-id="be52a-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be52a-122">Condição</span><span class="sxs-lookup"><span data-stu-id="be52a-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="be52a-123">Ação</span><span class="sxs-lookup"><span data-stu-id="be52a-123">Action</span></span></p></th>
<th><p><span data-ttu-id="be52a-124">Argumentos</span><span class="sxs-lookup"><span data-stu-id="be52a-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="be52a-125"><strong>Definirvariáveltemporária</strong></span><span class="sxs-lookup"><span data-stu-id="be52a-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="be52a-126"><strong>Nome</strong>: MINHAVARIÁVEL<strong>expressão</strong>: CaixaDeEntrada (&quot;Insira um número diferente de zero.&quot;)</span><span class="sxs-lookup"><span data-stu-id="be52a-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be52a-127">[Varstemp]! [MINHAVARIÁVEL] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="be52a-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="be52a-128"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="be52a-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="be52a-129"><strong>Mensagem</strong>: =&quot;você digitou &quot; &amp; [Varstemp]! [MINHAVARIÁVEL] &amp; &quot;. &quot; <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>informações</strong></span><span class="sxs-lookup"><span data-stu-id="be52a-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="be52a-130"><strong>Removervariáveltemporária</strong></span><span class="sxs-lookup"><span data-stu-id="be52a-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="be52a-131"><strong>Nome</strong>: MinhaVar</span><span class="sxs-lookup"><span data-stu-id="be52a-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

