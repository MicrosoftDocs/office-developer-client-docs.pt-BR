---
title: Evento da macro Após Atualização
TOCTitle: After Update macro event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 237b3633ab70bcdbe84ce52f7d25b2203091cb1e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919133"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="2fea6-102">Evento da macro Após Atualização</span><span class="sxs-lookup"><span data-stu-id="2fea6-102">After Update macro event</span></span>


<span data-ttu-id="2fea6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fea6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fea6-104">O evento **After Update** ocorre após a alteração de um registro.</span><span class="sxs-lookup"><span data-stu-id="2fea6-104">The **After Update** event occurs after a record is changed.</span></span>


> [!NOTE]
> <span data-ttu-id="2fea6-105">[!OBSERVAçãO] O evento **After Update** só está disponível em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="2fea6-105">The **After Update** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="2fea6-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fea6-106">Remarks</span></span>

<span data-ttu-id="2fea6-p101">Use o evento **After Update** para executar todas as ações que você deseja que ocorram quando um registro for alterado. Os usos comuns para **After Insert** incluem impor regras comerciais, atualização de um total agregado e envio de notificações.</span><span class="sxs-lookup"><span data-stu-id="2fea6-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="2fea6-p102">Você pode usar a função **Updated("*Field Name*")** para determinar se um campo foi alterado. O exemplo de código a seguir mostra como usar uma instrução **If** para determinar se o campo PaidInFull foi alterado.</span><span class="sxs-lookup"><span data-stu-id="2fea6-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="2fea6-111">Você pode acessar um valor anterior em um campo utilizando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="2fea6-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="2fea6-112">Por exemplo, para acessar o valor anterior do campo QuantityIInStock, use a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="2fea6-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="2fea6-113">Os valores anteriores serão permanentemente excluídos quando o evento **After Update** terminar.</span><span class="sxs-lookup"><span data-stu-id="2fea6-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="2fea6-114">A tabela a seguir lista comandos de macro que podem ser usados no evento **After Update**.</span><span class="sxs-lookup"><span data-stu-id="2fea6-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fea6-115">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="2fea6-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="2fea6-116">Comando</span><span class="sxs-lookup"><span data-stu-id="2fea6-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-117">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="2fea6-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2fea6-118"><a href="comment-macro-statement.md">Instrução de macro comentário</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-119">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="2fea6-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2fea6-120"><a href="group-macro-statement.md">Instrução de macro grupo</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-121">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="2fea6-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2fea6-122"><a href="if-then-else-macro-block.md">Se... Então... Bloco de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-123">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2fea6-124"><a href="createrecord-data-block.md">Ação de macro CriarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-124"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-125">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2fea6-126"><a href="editrecord-data-block.md">Ação de macro EditarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-126"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-127">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2fea6-128"><a href="foreachrecord-data-block.md">Ação de macro ParaCadaRegistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-128"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-129">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2fea6-130"><a href="lookuprecord-data-block.md">Bloco de dados Pesquisarregistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-130"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-131">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-132"><a href="cancelrecordchange-macro-action.md">Ação de macro Cancelaralteraçãoderegistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-133">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-134"><a href="clearmacroerror-macro-action.md">Ação de macro Limparerrodemacro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-135">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-136"><a href="deleterecord-macro-action.md">Ação de macro ExcluirRegistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-137">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-138"><a href="exitforeachrecord-macro-action.md">Ação de macro SairParaCadaRegistro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-139">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-140"><a href="logevent-macro-action.md">Ação de macro RegistrarEvento</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-141">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-142"><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-143">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-144"><a href="raiseerror-macro-action.md">Ação de macro Gerarerro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-145">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-146"><a href="rundatamacro-macro-action.md">Ação de macro ExecutarMacrodeDados</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-147">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-148"><a href="sendemail-macro-action.md">Ação de macro EnviarEmail</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-149">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-150"><a href="setfield-macro-action.md">Ação de macro Definircampo</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-151">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-152"><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2fea6-153">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-154"><a href="stopallmacros-macro-action.md">Ação de macro PararTodasMacros</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fea6-155">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="2fea6-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2fea6-156"><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></span><span class="sxs-lookup"><span data-stu-id="2fea6-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2fea6-157">Para criar uma macro Data que captura o evento **After Update**, use estas etapas:</span><span class="sxs-lookup"><span data-stu-id="2fea6-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="2fea6-158">Abra a tabela para a qual você deseja capturar o evento **After Update**.</span><span class="sxs-lookup"><span data-stu-id="2fea6-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="2fea6-159">Na guia **Tabela**, no grupo **After Events**, clique em **After Update**.</span><span class="sxs-lookup"><span data-stu-id="2fea6-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="2fea6-160">Uma macro de dados vazia é exibida no designer de macros.</span><span class="sxs-lookup"><span data-stu-id="2fea6-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="2fea6-161">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2fea6-161">Example</span></span>

<span data-ttu-id="2fea6-162">O exemplo de código a seguir usa o evento **After Update** para executar uma macro de dados nomeada que adiciona um registro à tabela Comentário sempre que o status de um problema for atualizado.</span><span class="sxs-lookup"><span data-stu-id="2fea6-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="2fea6-163">**Clique aqui para exibir uma cópia da macro que você pode colar no Designer de Macros.**</span><span class="sxs-lookup"><span data-stu-id="2fea6-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="2fea6-164">Para exibir este exemplo no designer de macros, use estas etapas:</span><span class="sxs-lookup"><span data-stu-id="2fea6-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="2fea6-165">Abra a tabela para a qual você deseja capturar o evento **After Update**.</span><span class="sxs-lookup"><span data-stu-id="2fea6-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="2fea6-166">Na guia **Tabela**, no grupo **After Events**, clique em **After Update**.</span><span class="sxs-lookup"><span data-stu-id="2fea6-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="2fea6-167">Selecione o código no seguinte exemplo de código e então pressione CTRL+C para copiá-lo para a Área de Transferência.</span><span class="sxs-lookup"><span data-stu-id="2fea6-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="2fea6-168">Ative a janela do designer de macros e pressione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="2fea6-168">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterUpdate"> 
        <Statements> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Status")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Status changed to &quot; &amp; [Status]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Resolution")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Issue resolved as &quot; &amp; [Resolution]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
``` 

<br/>

```vb
If  Updated("Status")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
         prmComment   ="--Status Changes to "&[Status] 
          prmUserID   =[ChangedByUserID] 
End If 
 
If   Updated("Resolution")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
          prmUserID   =[ChangedByUserID] 
         prmComment   ="--Issue Resolved as "&[Status] 
End If 
```

