---
title: Evento da macro Após Inserção
TOCTitle: After Insert macro event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: af6bc99374c67560e9cd78a9f26bc9dd601c70d8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026145"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="03143-102">Evento da macro Após Inserção</span><span class="sxs-lookup"><span data-stu-id="03143-102">After Insert macro event</span></span>

<span data-ttu-id="03143-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="03143-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03143-104">O evento **Após Inserir** ocorre após a adição de um registro.</span><span class="sxs-lookup"><span data-stu-id="03143-104">The **After Insert** event occurs after a record is added.</span></span>

> [!NOTE]
> <span data-ttu-id="03143-105">[!OBSERVAçãO] O evento **Após Inserir** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="03143-105">The **After Insert** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="03143-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="03143-106">Remarks</span></span>

<span data-ttu-id="03143-p101">Use o evento **Após Inserir** para executar qualquer ação que você deseja que ocorra após a adição de um registro a uma tabela. As utilizações mais comuns do **Após Inserir** incluem a aplicação de regras de negócio, fluxos de trabalho, a atualização de um total agregado e o envio de notificações.</span><span class="sxs-lookup"><span data-stu-id="03143-p101">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table. Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="03143-p102">Você pode usar a função **Updated("*Field Name*")** para determinar se um campo foi alterado. O exemplo de código a seguir mostra como usar uma instrução **If** para determinar se o campo PaidInFull foi alterado.</span><span class="sxs-lookup"><span data-stu-id="03143-p102">You can use the **Updated("*Field Name*")** function to determine whether a field has changed. The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="03143-111">A tabela a seguir lista comandos de macro que podem ser usadas no evento **Após Inserir**.</span><span class="sxs-lookup"><span data-stu-id="03143-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03143-112">Tipo de comando</span><span class="sxs-lookup"><span data-stu-id="03143-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="03143-113">Comando</span><span class="sxs-lookup"><span data-stu-id="03143-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03143-114">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="03143-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="03143-115"><a href="comment-macro-statement.md">Instrução de macro comentário</a></span><span class="sxs-lookup"><span data-stu-id="03143-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-116">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="03143-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="03143-117"><a href="group-macro-statement.md">Instrução de macro grupo</a></span><span class="sxs-lookup"><span data-stu-id="03143-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-118">Fluxo do programa</span><span class="sxs-lookup"><span data-stu-id="03143-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="03143-119"><a href="if-then-else-macro-block.md">Se... Então... Bloco de macro Else</a></span><span class="sxs-lookup"><span data-stu-id="03143-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-120">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="03143-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="03143-121"><a href="createrecord-data-block.md">Ação de macro CriarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-121"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-122">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="03143-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="03143-123"><a href="editrecord-data-block.md">Ação de macro EditarRegistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-123"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-124">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="03143-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="03143-125"><a href="foreachrecord-data-block.md">Ação de macro ParaCadaRegistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-125"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-126">Bloco de dados</span><span class="sxs-lookup"><span data-stu-id="03143-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="03143-127"><a href="lookuprecord-data-block.md">Bloco de dados Pesquisarregistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-127"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-128">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-129"><a href="cancelrecordchange-macro-action.md">Ação de macro Cancelaralteraçãoderegistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-130">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-131"><a href="clearmacroerror-macro-action.md">Ação de macro Limparerrodemacro</a></span><span class="sxs-lookup"><span data-stu-id="03143-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-132">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-133"><a href="deleterecord-macro-action.md">Ação de macro ExcluirRegistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-134">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-135"><a href="exitforeachrecord-macro-action.md">Ação de macro SairParaCadaRegistro</a></span><span class="sxs-lookup"><span data-stu-id="03143-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-136">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-137"><a href="logevent-macro-action.md">Ação de macro RegistrarEvento</a></span><span class="sxs-lookup"><span data-stu-id="03143-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-138">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-139"><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></span><span class="sxs-lookup"><span data-stu-id="03143-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-140">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-141"><a href="raiseerror-macro-action.md">Ação de macro Gerarerro</a></span><span class="sxs-lookup"><span data-stu-id="03143-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-142">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-143"><a href="rundatamacro-macro-action.md">Ação de macro ExecutarMacrodeDados</a></span><span class="sxs-lookup"><span data-stu-id="03143-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-144">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-145"><a href="sendemail-macro-action.md">Ação de macro EnviarEmail</a></span><span class="sxs-lookup"><span data-stu-id="03143-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-146">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-147"><a href="setfield-macro-action.md">Ação de macro Definircampo</a></span><span class="sxs-lookup"><span data-stu-id="03143-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-148">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-149"><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></span><span class="sxs-lookup"><span data-stu-id="03143-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03143-150">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-151"><a href="stopallmacros-macro-action.md">Ação de macro PararTodasMacros</a></span><span class="sxs-lookup"><span data-stu-id="03143-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03143-152">Ação de dados</span><span class="sxs-lookup"><span data-stu-id="03143-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="03143-153"><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></span><span class="sxs-lookup"><span data-stu-id="03143-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03143-154">Para criar uma Macro de Dados que capture o evento **Após Inserir**, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="03143-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="03143-155">Abra a tabela na qual deseja capturar o evento **Após Inserir**.</span><span class="sxs-lookup"><span data-stu-id="03143-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="03143-156">Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Inserir**.</span><span class="sxs-lookup"><span data-stu-id="03143-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="03143-157">Uma macro de dados vazia é exibida no designer de macros.</span><span class="sxs-lookup"><span data-stu-id="03143-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="03143-158">Exemplo</span><span class="sxs-lookup"><span data-stu-id="03143-158">Example</span></span>

<span data-ttu-id="03143-p103">O exemplo de código a seguir usa o evento **Após Inserir** para executar alguns processos quando um registro é adicionado à tabela Doações. Quando um registro é adicionado, a quantidade de doações é adicionada ao campo DoaçõesRecebidas em Campanhas e ao campo TotaldaDoação na tabela Doa</span><span class="sxs-lookup"><span data-stu-id="03143-p103">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="03143-161">**Clique aqui para exibir uma cópia da macro que você pode colar no Designer de Macros.**</span><span class="sxs-lookup"><span data-stu-id="03143-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="03143-162">Para exibir este exemplo no designer de macros, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="03143-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="03143-163">Abra a tabela na qual deseja capturar o evento **Após Inserir**.</span><span class="sxs-lookup"><span data-stu-id="03143-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="03143-164">Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Inserir**.</span><span class="sxs-lookup"><span data-stu-id="03143-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="03143-165">Selecione o código no exemplo de código a seguir e pressione CTRL+C para copiá-lo para a Área de Transfer</span><span class="sxs-lookup"><span data-stu-id="03143-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="03143-166">Ative a janela do designer de macros e pressione CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="03143-166">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros> 
      <DataMacro Event="AfterInsert"> 
        <Statements> 
          <Comment>This data macro increments the DonationsReceived field in Campaigns and theAmountCollected field in Pledges </Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Donations].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]+[varAmount]</Argument> 
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
              <Condition>Not (IsNull([DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Donations].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]+[varAmount]</Argument> 
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
                  Name   varAmount 
            Expression   =[Amount] 
     
    If   Not (IsNull([CampaignID]))   Then 
     
         For Each Record In   Campaigns 
            Where Condition   =[ID]=[Donations].[CampaignID] 
                      Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [DonationsReceived] 
                                Value   =[DonationsReceived]+[varAmount] 
                End EditRecord 
    End If 
     
    If   Not (IsNull([DonorID]))   Then 
     
         For Each Record In  Donors 
            WhereCondition   =[ID]=[Donations].[DonorID] 
                     Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [TotalDonated] 
                                Value   =[TotalDonated]+[varAmount] 
                 End EditRecord 
    End If
```
