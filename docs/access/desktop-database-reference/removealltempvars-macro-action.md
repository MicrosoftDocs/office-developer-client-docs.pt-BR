---
title: Ação da macro RemoverTodasVariáveisTemporárias
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306794"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="0ccb9-102">Ação da macro RemoverTodasVariáveisTemporárias</span><span class="sxs-lookup"><span data-stu-id="0ccb9-102">RemoveAllTempVars macro action</span></span>


<span data-ttu-id="0ccb9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ccb9-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0ccb9-104">Você pode usar a ação **RemoverTodasVariáveisTemporárias** para remover todas as variáveis temporárias criadas usando a ação **DefinirVariávelTemporária**.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="0ccb9-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="0ccb9-105">Setting</span></span>

<span data-ttu-id="0ccb9-106">A ação **RemoverTodasVariáveisTemporárias** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ccb9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ccb9-107">Remarks</span></span>

  - <span data-ttu-id="0ccb9-p101">É possível ter até 255 variáveis temporárias definidas de cada vez. Se você não remover uma variável temporária, ela permanecerá na memória até o banco de dados ou projeto ser fechado. É recomendável remover as variáveis temporárias quando acabar de usá-las.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database or project. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="0ccb9-111">O Access remove automaticamente todas as variáveis temporárias ao fechar o banco de dados ou projeto.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="0ccb9-112">Para remover uma única variável temporária, use a ação **RemoverVariávelTemporária** e defina seu argumento com o nome da variável temporária que deseja remover.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="0ccb9-113">Para executar a ação **RemoverTodasVariáveisTemporárias** em um módulo do VBA, use o método **RemoveAll** do objeto **TempVars**.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="0ccb9-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0ccb9-114">Example</span></span>

<span data-ttu-id="0ccb9-115">A macro a seguir demonstra como criar uma variável temporária, usá-la em uma condição e uma caixa de mensagens e removê-la usando a ação **RemoverTodasVariáveisTemporárias**.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ccb9-116">Condição</span><span class="sxs-lookup"><span data-stu-id="0ccb9-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="0ccb9-117">Ação</span><span class="sxs-lookup"><span data-stu-id="0ccb9-117">Action</span></span></p></th>
<th><p><span data-ttu-id="0ccb9-118">Argumentos</span><span class="sxs-lookup"><span data-stu-id="0ccb9-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0ccb9-119"><strong>DefinirVariávelTemporária</strong></span><span class="sxs-lookup"><span data-stu-id="0ccb9-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccb9-120"><strong>Name</strong>: minhavar<strong>expressão</strong>: InputBox (&quot;Insira um número diferente de zero)&quot;.</span><span class="sxs-lookup"><span data-stu-id="0ccb9-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ccb9-121">[TempVars]! Minhavar &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="0ccb9-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="0ccb9-122"><strong>CaixaDeMensagem</strong></span><span class="sxs-lookup"><span data-stu-id="0ccb9-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="0ccb9-123"><strong>Mensagem</strong>: =&quot;você inseriu &quot; &amp; [TempVars]! Minhavar &amp; &quot;. &quot; <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>informações</strong></span><span class="sxs-lookup"><span data-stu-id="0ccb9-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0ccb9-124"><strong>RemoverTodasVariáveisTemporárias</strong></span><span class="sxs-lookup"><span data-stu-id="0ccb9-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

