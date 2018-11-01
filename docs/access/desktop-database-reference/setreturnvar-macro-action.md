---
title: Ação de Macro SetReturnVar
TOCTitle: SetReturnVar Macro Action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a0c4d47283b059a32fa4df3ba8e1278c1fdcd17a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873982"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="4f387-102">Ação de Macro SetReturnVar</span><span class="sxs-lookup"><span data-stu-id="4f387-102">SetReturnVar Macro Action</span></span>

<span data-ttu-id="4f387-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f387-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f387-104">A ação **SetReturnVar** cria uma variável de retorno e o configura para um valor específico.</span><span class="sxs-lookup"><span data-stu-id="4f387-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="4f387-105">A ação de **SetReturnVar** está disponível somente em Macros de dados.</span><span class="sxs-lookup"><span data-stu-id="4f387-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="4f387-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="4f387-106">Setting</span></span>

<span data-ttu-id="4f387-107">A ação **SetReturnVar** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4f387-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f387-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="4f387-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="4f387-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4f387-109">Required</span></span></p></th>
<th><p><span data-ttu-id="4f387-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f387-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f387-111">Name</span><span class="sxs-lookup"><span data-stu-id="4f387-111">Name</span></span></p></td>
<td><p><span data-ttu-id="4f387-112">Sim</span><span class="sxs-lookup"><span data-stu-id="4f387-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f387-113">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="4f387-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f387-114">Expressão</span><span class="sxs-lookup"><span data-stu-id="4f387-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="4f387-115">Sim</span><span class="sxs-lookup"><span data-stu-id="4f387-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="4f387-116">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="4f387-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="4f387-117">Não preceda a expressão com o sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="4f387-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="4f387-118">Você pode clicar no botão <strong>Construir</strong> para usar o <strong>Construtor de expressões</strong> para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="4f387-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4f387-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f387-119">Remarks</span></span>

<span data-ttu-id="4f387-120">A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é a variável que pode ser usado por macros que chamar uma macro de dados usando a ação **ExecutarMacrodeDados** .</span><span class="sxs-lookup"><span data-stu-id="4f387-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="4f387-121">Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro chamada pode ser usada em uma expressão.</span><span class="sxs-lookup"><span data-stu-id="4f387-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="4f387-122">Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, você poderia usar a variável usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="4f387-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="4f387-123">A ação **SetReturnVar** pode ser usada somente em macros de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="4f387-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="4f387-124">Ele não está disponível em macros de dados que estejam anexadas a um evento de macro de dados.</span><span class="sxs-lookup"><span data-stu-id="4f387-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="4f387-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4f387-125">Example</span></span>

<span data-ttu-id="4f387-126">O exemplo a seguir mostra como usar a ação de SetReturnVar para retornar um valor de uma macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="4f387-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="4f387-127">Um ReturnVar chamado **CurrentServiceRequest** é retornada para a macro ou o Visual Basic para a sub-rotina Applications (VBA) que chamou a macro de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="4f387-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="4f387-128">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4f387-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
