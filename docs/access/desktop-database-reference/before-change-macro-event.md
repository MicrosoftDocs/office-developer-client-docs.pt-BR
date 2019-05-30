---
title: Evento da macro Antes da Alteração
TOCTitle: Before Change macro event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a180068e805ae11883822ebf26f924e10d34bac5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538113"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="d8756-102">Evento da macro Antes da Alteração</span><span class="sxs-lookup"><span data-stu-id="d8756-102">Before Change macro event</span></span>

<span data-ttu-id="d8756-103">**Aplica-se a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8756-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8756-104">O evento **Antes de Alterar** ocorre quando um registro é alterado, mas antes da alteração ser submetida.</span><span class="sxs-lookup"><span data-stu-id="d8756-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="d8756-105">O evento **Antes de Alterar** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="d8756-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8756-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8756-106">Remarks</span></span>

<span data-ttu-id="d8756-p101">Use o evento **Antes de Alterar** para executar qualquer ação que você deseja que ocorra antes da alteração de um registro. O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d8756-p101">Use the **Before Change** event to perform any actions that you want to occur before a record is changed. The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="d8756-109">Você pode usar a função **Updated("*Nome do Campo*")** para determinar se um campo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d8756-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="d8756-110">O exemplo de código a seguir mostra como usar uma instrução **If** para determinar se o campo PaidInFull foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d8756-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="d8756-p103">Use a propriedade **Inserido** para determinar se o evento **Antes de Alterar** foi acionado por um novo registro que está sendo criado ou por uma alteração em um registro existente. A propriedade **Inserido** apresentará o valor **True** se o evento tiver sido acionado por um novo registro, e **False** se o evento tiver sido acionado por uma alteração em um registro existente.</span><span class="sxs-lookup"><span data-stu-id="d8756-p103">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record. They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="d8756-113">O exemplo de código a seguir mostra a sintaxe para o uso da propriedade **Inserido**.</span><span class="sxs-lookup"><span data-stu-id="d8756-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="d8756-114">Você pode usar o acesso ao valor anterior em um campo usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8756-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="d8756-115">Por exemplo, para acessar o valor anterior do campo QuantityIInStock, use a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8756-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="d8756-116">Os valores anteriores são excluídos permanentemente após a conclusão do evento **Antes de Alterar**.</span><span class="sxs-lookup"><span data-stu-id="d8756-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="d8756-p104">Você pode cancelar o evento **Antes de Alterar** utilizando a ação **GerarErro**. Quando um erro é exibido, as alterações contidas no evento **Antes de Alterar** são descartadas.</span><span class="sxs-lookup"><span data-stu-id="d8756-p104">You can cancel the **Before Change** event by using the **RaiseError** action. When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="d8756-119">A tabela a seguir lista comandos de macro que podem ser usadas no evento **Antes de Alterar**.</span><span class="sxs-lookup"><span data-stu-id="d8756-119">The following table lists macro commands that can be used in the**Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8756-120">Tipo de Comando</span><span class="sxs-lookup"><span data-stu-id="d8756-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="d8756-121">Comando</span><span class="sxs-lookup"><span data-stu-id="d8756-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8756-122">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="d8756-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="d8756-123"><a href="comment-macro-statement.md">Instrução de macro Comentário</a></span><span class="sxs-lookup"><span data-stu-id="d8756-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8756-124">Fluxo do Programa</span><span class="sxs-lookup"><span data-stu-id="d8756-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="d8756-125"><a href="group-macro-statement.md">Instrução de macro Grupo</a></span><span class="sxs-lookup"><span data-stu-id="d8756-125"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8756-126">Fluxo do Programa</span><span class="sxs-lookup"><span data-stu-id="d8756-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="d8756-127"><a href="if-then-else-macro-block.md">Bloco de macro Se... Então... Senão</a></span><span class="sxs-lookup"><span data-stu-id="d8756-127"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8756-128">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="d8756-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="d8756-129"><a href="lookuprecord-data-block.md">Ação de macro Pesquisarregistro</a></span><span class="sxs-lookup"><span data-stu-id="d8756-129"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8756-130">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="d8756-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d8756-131"><a href="clearmacroerror-macro-action.md">Ação de macro LimparErrodaMacro</a></span><span class="sxs-lookup"><span data-stu-id="d8756-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8756-132">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="d8756-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d8756-133"><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></span><span class="sxs-lookup"><span data-stu-id="d8756-133"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8756-134">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="d8756-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d8756-135"><a href="raiseerror-macro-action.md">Ação de macro GerarErro</a></span><span class="sxs-lookup"><span data-stu-id="d8756-135"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8756-136">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="d8756-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d8756-137"><a href="setfield-macro-action.md">Ação de macro DefinirCampo</a></span><span class="sxs-lookup"><span data-stu-id="d8756-137"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d8756-138">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="d8756-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d8756-139"><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></span><span class="sxs-lookup"><span data-stu-id="d8756-139"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8756-140">Ação de Dados</span><span class="sxs-lookup"><span data-stu-id="d8756-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="d8756-141"><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></span><span class="sxs-lookup"><span data-stu-id="d8756-141"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d8756-142">Para criar uma Macro de Dados que capture o evento **Antes de Alterar**, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="d8756-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="d8756-143">Abra a tabela na qual deseja capturar o evento **Antes de Alterar**.</span><span class="sxs-lookup"><span data-stu-id="d8756-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="d8756-144">Na guia **Tabela**, no grupo **Antes de eventos**, clique em **Antes de Alterar**.</span><span class="sxs-lookup"><span data-stu-id="d8756-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="d8756-145">Uma macro de dados vazia é exibida no designer de macros.</span><span class="sxs-lookup"><span data-stu-id="d8756-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="d8756-146">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d8756-146">Example</span></span>

<span data-ttu-id="d8756-147">O exemplo de código a seguir usa o evento **antes de alterar** para validar os campos de status.</span><span class="sxs-lookup"><span data-stu-id="d8756-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="d8756-148">Um erro será exibido se houver um valor incorreto no campo Resolução.</span><span class="sxs-lookup"><span data-stu-id="d8756-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

<span data-ttu-id="d8756-149">Para exibir este exemplo no designer de macros, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="d8756-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="d8756-150">Abra a tabela na qual deseja capturar o evento **Antes de Alterar**.</span><span class="sxs-lookup"><span data-stu-id="d8756-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="d8756-151">Na guia **Tabela**, no grupo **Antes de Eventos**, clique em **Antes de Alterar**.</span><span class="sxs-lookup"><span data-stu-id="d8756-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="d8756-152">Selecione o código no exemplo de código a seguir e pressione **Ctrl + C** para copiá-lo para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="d8756-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="d8756-153">Ative a janela do designer de macros e pressione **Ctrl + V**.</span><span class="sxs-lookup"><span data-stu-id="d8756-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



```xml
<DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

<span data-ttu-id="d8756-154">O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento antes de alterar a macro de dados.</span><span class="sxs-lookup"><span data-stu-id="d8756-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="d8756-155">Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído está atualmente atribuído a uma solicitação de serviço aberta.</span><span class="sxs-lookup"><span data-stu-id="d8756-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="d8756-156">Se isso for verdadeiro, o evento antes de alterar será cancelado e o registro não será atualizado.</span><span class="sxs-lookup"><span data-stu-id="d8756-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="d8756-157">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d8756-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
