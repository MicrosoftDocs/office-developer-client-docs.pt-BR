---
title: Evento de macro Após Exclusão
TOCTitle: After Delete Macro Event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b180acb99ab2ac406a7b60fdecf8aff5d63eb71f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869110"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="feeed-102">Evento de macro Após Exclusão</span><span class="sxs-lookup"><span data-stu-id="feeed-102">After Delete Macro Event</span></span>


<span data-ttu-id="feeed-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="feeed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="feeed-104">O evento **Após Exclusão** ocorre após a exclusão de cada evento.</span><span class="sxs-lookup"><span data-stu-id="feeed-104">The **After Delete** event occurs after a record is deleted.</span></span>


> [!NOTE]
> <span data-ttu-id="feeed-105">[!OBSERVAçãO] O evento **Após Exclusão** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="feeed-105">The **After Delete** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="feeed-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="feeed-106">Remarks</span></span>

<span data-ttu-id="feeed-p101">Use o evento **Após Exclusão** para executar qualquer ação que você deseja que ocorra após a exclusão de um registro. As utilizações mais comuns do **Após Exclusão** incluem a aplicação de regras de negócio, fluxos de trabalho, a atualização de um total agregado e o envio de notificações.</span><span class="sxs-lookup"><span data-stu-id="feeed-p101">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted. Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="feeed-109">Quando o evento **Após Exclusão** ocorre, os valores contidos no registro excluído ainda permanecem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="feeed-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="feeed-110">Convém usar um valor excluído para incrementar ou diminuir um total, criar uma trilha de auditoria ou comparar com um valor existente em um argumento *WhereCondition* .</span><span class="sxs-lookup"><span data-stu-id="feeed-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="feeed-p103">Você pode usar a função **Updated("*Nome do Campo*")** para determinar se um campo foi alterado. O código de exemplo a seguir mostra como usar uma instrução Se para determinar se o campo PaidInFull foi alterado.</span><span class="sxs-lookup"><span data-stu-id="feeed-p103">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="feeed-113">Você pode acessar um valor no registro excluído utilizando a sintaxe a seguir</span><span class="sxs-lookup"><span data-stu-id="feeed-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="feeed-114">Por exemplo, para acessar o valor do campo QuantityInStock no registro excluído, use a seguinte sintaxe.</span><span class="sxs-lookup"><span data-stu-id="feeed-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="feeed-115">Os valores contidos no registro excluído são excluídos permanentemente após a conclusão do evento **Após Exclusão**.</span><span class="sxs-lookup"><span data-stu-id="feeed-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="feeed-116">Os seguintes comandos de macro podem ser usados no evento **Após exclusão** .</span><span class="sxs-lookup"><span data-stu-id="feeed-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="feeed-117">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="feeed-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="feeed-118">Comando</span><span class="sxs-lookup"><span data-stu-id="feeed-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feeed-119">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="feeed-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="feeed-120"><a href="comment-macro-statement.md">Instrução de macro de comentário</a></span><span class="sxs-lookup"><span data-stu-id="feeed-120"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-121">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="feeed-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="feeed-122"><a href="group-macro-statement.md">Instrução de macro de grupo</a></span><span class="sxs-lookup"><span data-stu-id="feeed-122"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-123">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="feeed-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="feeed-124"><a href="if-then-else-macro-block.md">Bloco de macro If...Then...Else</a></span><span class="sxs-lookup"><span data-stu-id="feeed-124"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-125">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="feeed-126"><a href="createrecord-data-block.md">Ação de macro CreateRecord</a></span><span class="sxs-lookup"><span data-stu-id="feeed-126"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-127">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="feeed-128"><a href="editrecord-data-block.md">Ação de macro EditRecord</a></span><span class="sxs-lookup"><span data-stu-id="feeed-128"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-129">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="feeed-130"><a href="foreachrecord-data-block.md">Ação de macro ForEachRecord</a></span><span class="sxs-lookup"><span data-stu-id="feeed-130"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-131">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="feeed-132"><a href="lookuprecord-data-block.md">Bloco de dados LookupRecord</a></span><span class="sxs-lookup"><span data-stu-id="feeed-132"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-133">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-134"><a href="cancelrecordchange-macro-action.md">Ação de macro CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="feeed-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-135">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-136"><a href="clearmacroerror-macro-action.md">Ação de macro ClearMacroError</a></span><span class="sxs-lookup"><span data-stu-id="feeed-136"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-137">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-138"><a href="deleterecord-macro-action.md">Ação de macro DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="feeed-138"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-139">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-140"><a href="exitforeachrecord-macro-action.md">Ação de macro ExitForEachRecord</a></span><span class="sxs-lookup"><span data-stu-id="feeed-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-141">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-142"><a href="logevent-macro-action.md">Ação de macro LogEvent</a></span><span class="sxs-lookup"><span data-stu-id="feeed-142"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-143">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-144"><a href="onerror-macro-action.md">Ação de macro OnError</a></span><span class="sxs-lookup"><span data-stu-id="feeed-144"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-145">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-146"><a href="raiseerror-macro-action.md">Ação de macro RaiseError</a></span><span class="sxs-lookup"><span data-stu-id="feeed-146"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-147">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-148"><a href="rundatamacro-macro-action.md">Ação de macro RunDataMacro</a></span><span class="sxs-lookup"><span data-stu-id="feeed-148"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-149">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-150"><a href="sendemail-macro-action.md">Ação de macro SendEmail</a></span><span class="sxs-lookup"><span data-stu-id="feeed-150"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-151">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-152"><a href="setfield-macro-action.md">Ação de macro SetField</a></span><span class="sxs-lookup"><span data-stu-id="feeed-152"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-153">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-154"><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="feeed-154"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feeed-155">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-156"><a href="stopallmacros-macro-action.md">Ação de macro StopAllMacros</a></span><span class="sxs-lookup"><span data-stu-id="feeed-156"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feeed-157">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="feeed-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="feeed-158"><a href="stopmacro-macro-action.md">Ação de macro StopMacro</a></span><span class="sxs-lookup"><span data-stu-id="feeed-158"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="feeed-159">Para criar uma Macro de Dados que capture o evento **Após Exclusão**, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="feeed-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="feeed-160">Abra a tabela na qual deseja capturar o evento **Após Exclusão**.</span><span class="sxs-lookup"><span data-stu-id="feeed-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="feeed-161">Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Exclusão**.</span><span class="sxs-lookup"><span data-stu-id="feeed-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="feeed-162">Uma Macro de Dados vazia é exibida no designer de macros.</span><span class="sxs-lookup"><span data-stu-id="feeed-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="feeed-163">Exemplo</span><span class="sxs-lookup"><span data-stu-id="feeed-163">Example</span></span>

<span data-ttu-id="feeed-p104">O exemplo de código a seguir usa o evento **Após Exclusão** para executar alguns processos quando um registro é excluído da tabela Doações. Quando um registro é excluído, a quantidade de doações é subtraída do campo DoaçõesRecebidas em DoaçõesRecebidas e do campo TotaldaDoação na tabela Doadores.</span><span class="sxs-lookup"><span data-stu-id="feeed-p104">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table. When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="feeed-166">**Clique aqui para exibir uma cópia da macro que você pode colar no Designer de Macros.**</span><span class="sxs-lookup"><span data-stu-id="feeed-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="feeed-167">Para exibir este exemplo no designer de macros, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="feeed-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="feeed-168">Abra a tabela na qual deseja capturar o evento **Após Exclusão**.</span><span class="sxs-lookup"><span data-stu-id="feeed-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="feeed-169">Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Exclusão**.</span><span class="sxs-lookup"><span data-stu-id="feeed-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="feeed-170">Selecione o código listado abaixo e pressione CTRL+C para copiá-lo para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="feeed-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="feeed-171">Ative a janela do designer de macros e pressione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="feeed-171">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterDelete"> 
        <Statements> 
          <Comment>Initialize a variable and assign the old</Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Old].[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Old].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Collapsed="true" Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Old].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
```

<br/>

```vb
    SetLocalVar 
                    Name    varAmount 
              Expression   =[Old].[Amount] 
     
    If   Not(IsNull([Old].[CampaignID]]))   Then 
     
         For Each Record In     Campaigns 
            Where Condition     =[ID]=[Old].[CampaignID] 
                      Alias 
            EditRecord 
                      Alias 
                  SetField   ([DonationsReceived], [DonationsReceived] - [varAmount]) 
            End EditRecord 
     
    End If 
     
    If   Not(IsNull([Old].[DonorID]]))   Then 
     
         For Each Record In    Donors 
            Where Condition     =[ID]=[Old].[DonorID] 
                      Alias 
            EditRecord 
                      Alias 
     
              SetField 
                             Name   [TotalDonated] 
                            Value   =[TotalDonated]-[varAmount] 
            End EditRecord 
    End If
```
