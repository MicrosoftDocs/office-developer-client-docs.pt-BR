---
title: Ação da macro GerarErro
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726033"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="82061-102">Ação da macro GerarErro</span><span class="sxs-lookup"><span data-stu-id="82061-102">RaiseError macro action</span></span>

<span data-ttu-id="82061-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="82061-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="82061-104">A ação **GerarErro** cria uma exceção que pode ser lidada pela ação de macro **[AoOcorrerErro](onerror-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="82061-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="82061-105">[!OBSERVAçãO] A ação **GerarErro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="82061-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="82061-106">Configuração</span><span class="sxs-lookup"><span data-stu-id="82061-106">Setting</span></span>

<span data-ttu-id="82061-107">A ação **GerarErro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="82061-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82061-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="82061-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="82061-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82061-109">Required</span></span></p></th>
<th><p><span data-ttu-id="82061-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="82061-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82061-111">Número do erro</span><span class="sxs-lookup"><span data-stu-id="82061-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="82061-112">Sim</span><span class="sxs-lookup"><span data-stu-id="82061-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="82061-113">Um número ou uma expressão que resolve para o tipo de dados Long.</span><span class="sxs-lookup"><span data-stu-id="82061-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82061-114">Descrição do erro</span><span class="sxs-lookup"><span data-stu-id="82061-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="82061-115">Não</span><span class="sxs-lookup"><span data-stu-id="82061-115">No</span></span></p></td>
<td><p><span data-ttu-id="82061-116">Uma expressão de cadeia de caracteres que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="82061-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="82061-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="82061-117">Remarks</span></span>

<span data-ttu-id="82061-118">Se a ação **GerarErro** for chamada em um evento de macro **[Antes de Alterar](before-change-macro-event.md)** ou **[Antes de Excluir](before-delete-macro-event.md)**, o evento será cancelado.</span><span class="sxs-lookup"><span data-stu-id="82061-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="82061-p101">Se não houver uma instrução **AoOcorrerErro** ativa lidando com erros, o erro gerado pela ação **GerarErro** será adicionado à tabela de sistema **USysApplicationLog**. Quando a ação **GerarErro** for gravada na tabela **USysApplicationLog**, a coluna **Categoria** será automaticamente definida como **Execução**.</span><span class="sxs-lookup"><span data-stu-id="82061-p101">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="82061-121">Para ver a tabela **USysApplicationLog**, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="82061-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="82061-122">Clique no menu **arquivo** e, em seguida, clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="82061-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="82061-123">Na caixa de diálogo **Opções do Access**, clique na guia **Banco de Dados Atual**.</span><span class="sxs-lookup"><span data-stu-id="82061-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="82061-124">Na seção **Navegação**, clique em **Opções de Navegação**.</span><span class="sxs-lookup"><span data-stu-id="82061-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="82061-125">Na caixa de diálogo **Opções de Navegação**, clique em **Mostrar Objetos do Sistema** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="82061-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="82061-126">Clique em **OK** para fechar a caixa de diálogo **Opções do Access**.</span><span class="sxs-lookup"><span data-stu-id="82061-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="82061-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="82061-127">Example</span></span>

<span data-ttu-id="82061-128">O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento de macro de dados antes de alterar.</span><span class="sxs-lookup"><span data-stu-id="82061-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="82061-129">Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído atualmente atribuído a uma solicitação de serviço em aberto.</span><span class="sxs-lookup"><span data-stu-id="82061-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="82061-130">Se isso for verdadeiro, então o evento antes de alterar for cancelado e o registro não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="82061-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="82061-131">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="82061-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
