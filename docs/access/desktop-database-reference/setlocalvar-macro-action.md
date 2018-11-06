---
title: Ação da macro DefinirVarLocal
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b257473d2acd3d17f30a3fdd579d213dcd39487b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996899"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="d7952-102">Ação da macro DefinirVarLocal</span><span class="sxs-lookup"><span data-stu-id="d7952-102">SetLocalVar macro action</span></span>

<span data-ttu-id="d7952-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7952-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7952-104">Use a ação **DefinirVarLocal** para criar uma variável temporária e defini-la com um valor específico.</span><span class="sxs-lookup"><span data-stu-id="d7952-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="d7952-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="d7952-105">Setting</span></span>

<span data-ttu-id="d7952-106">A ação **DefinirVarLocal** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d7952-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7952-107">Argumento</span><span class="sxs-lookup"><span data-stu-id="d7952-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="d7952-108">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d7952-108">Required</span></span></p></th>
<th><p><span data-ttu-id="d7952-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7952-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7952-110"><strong>Nome</strong></span><span class="sxs-lookup"><span data-stu-id="d7952-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d7952-111">Sim</span><span class="sxs-lookup"><span data-stu-id="d7952-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="d7952-112">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="d7952-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7952-113"><strong>Expressão</strong>.</span><span class="sxs-lookup"><span data-stu-id="d7952-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="d7952-114">Sim</span><span class="sxs-lookup"><span data-stu-id="d7952-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="d7952-115">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="d7952-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="d7952-116">Não preceda a expressão com o sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="d7952-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="d7952-117">Você pode clicar no botão <strong>Construir</strong> para usar o <strong>Construtor de expressões</strong> para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="d7952-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="d7952-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7952-118">Remarks</span></span>

<span data-ttu-id="d7952-p102">As variáveis criadas pela ação **DefinirVarLocal** somente podem ser usadas na macro onde foram definidas. Use a ação **[DefinirVarLocal](settempvar-macro-action.md)** para definir uma variável que pode ser usada em outra macro, em um procedimento de evento ou em um formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="d7952-p102">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="d7952-p103">Após a criação de uma variável temporária, você poderá fazer referência a ela em uma expressão. Por exemplo, se criar uma variável temporária com o nome MinhaVar, você poderá usá-la como fonte de controle de uma caixa de texto, usando esta sintaxe.</span><span class="sxs-lookup"><span data-stu-id="d7952-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> <span data-ttu-id="d7952-123">[!OBSERVAçãO] Em uma Macro de Dados, não é necessário usar a coleção LocalVars para fazer referência a uma variável.</span><span class="sxs-lookup"><span data-stu-id="d7952-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="d7952-124">Por exemplo, se você criou uma variável temporária em uma Macro de dados denominado TotalAmount, você pode usar a variável como a fonte de controle para uma caixa de texto usando a seguinte sintaxe: `=[TotalAmount]`.</span><span class="sxs-lookup"><span data-stu-id="d7952-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax: `=[TotalAmount]`.</span></span>

