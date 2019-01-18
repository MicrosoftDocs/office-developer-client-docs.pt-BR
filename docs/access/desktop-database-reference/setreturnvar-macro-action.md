---
title: Ação da macro DefinirVardeRetorno
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708155"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="7b822-102">Ação da macro DefinirVardeRetorno</span><span class="sxs-lookup"><span data-stu-id="7b822-102">SetReturnVar macro action</span></span>

<span data-ttu-id="7b822-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b822-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b822-104">A ação **SetReturnVar** cria uma variável de retorno e o configura para um valor específico.</span><span class="sxs-lookup"><span data-stu-id="7b822-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="7b822-105">A ação de **SetReturnVar** está disponível somente em Macros de dados.</span><span class="sxs-lookup"><span data-stu-id="7b822-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="7b822-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="7b822-106">Setting</span></span>

<span data-ttu-id="7b822-107">A ação **SetReturnVar** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7b822-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b822-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="7b822-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="7b822-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7b822-109">Required</span></span></p></th>
<th><p><span data-ttu-id="7b822-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b822-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b822-111">Name</span><span class="sxs-lookup"><span data-stu-id="7b822-111">Name</span></span></p></td>
<td><p><span data-ttu-id="7b822-112">Sim</span><span class="sxs-lookup"><span data-stu-id="7b822-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="7b822-113">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="7b822-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b822-114">Expressão</span><span class="sxs-lookup"><span data-stu-id="7b822-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="7b822-115">Sim</span><span class="sxs-lookup"><span data-stu-id="7b822-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="7b822-116">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="7b822-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="7b822-117">Não preceda a expressão com o sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="7b822-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="7b822-118">Você pode clicar no botão <strong>Construir</strong> para usar o <strong>Construtor de expressões</strong> para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="7b822-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7b822-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b822-119">Remarks</span></span>

<span data-ttu-id="7b822-120">A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é a variável que pode ser usado por macros que chamar uma macro de dados usando a ação **ExecutarMacrodeDados** .</span><span class="sxs-lookup"><span data-stu-id="7b822-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="7b822-121">Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro chamada pode ser usada em uma expressão.</span><span class="sxs-lookup"><span data-stu-id="7b822-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="7b822-122">Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, você poderia usar a variável usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="7b822-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="7b822-123">A ação **SetReturnVar** pode ser usada somente em macros de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="7b822-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="7b822-124">Ele não está disponível em macros de dados que estejam anexadas a um evento de macro de dados.</span><span class="sxs-lookup"><span data-stu-id="7b822-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="7b822-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7b822-125">Example</span></span>

<span data-ttu-id="7b822-126">O exemplo a seguir mostra como usar a ação de SetReturnVar para retornar um valor de uma macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="7b822-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="7b822-127">Um ReturnVar chamado **CurrentServiceRequest** é retornada para a macro ou o Visual Basic para a sub-rotina Applications (VBA) que chamou a macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="7b822-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="7b822-128">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="7b822-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
