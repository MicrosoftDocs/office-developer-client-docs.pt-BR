---
title: Evento de macro Após Inserir
TOCTitle: After Insert Macro Event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a343c9bb0ea498c3388eb5ce67c3e0692808824c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463208"
---
# <a name="after-insert-macro-event"></a>Evento de macro Após Inserir


**Aplica-se a**: Access 2013 | Office 2013

O evento **Após Inserir** ocorre após a adição de um registro.


> [!NOTE]
> [!OBSERVAçãO] O evento **Após Inserir** está disponível somente em Macros de Dados.



## <a name="remarks"></a>Comentários

Use o evento **Após Inserir** para executar qualquer ação que você deseja que ocorra após a adição de um registro a uma tabela. As utilizações mais comuns do **Após Inserir** incluem a aplicação de regras de negócio, fluxos de trabalho, a atualização de um total agregado e o envio de notificações.

Você pode usar a função **Updated("*Field Name*")** para determinar se um campo foi alterado. O exemplo de código a seguir mostra como usar uma instrução **If** para determinar se o campo PaidInFull foi alterado.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

A tabela a seguir lista comandos de macro que podem ser usadas no evento **Após Inserir**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de comando</p></th>
<th><p>Comando</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="comment-macro-statement.md">Instrução de macro de comentário</a></p></td>
</tr>
<tr class="even">
<td><p>Fluxo do programa</p></td>
<td><p><a href="group-macro-statement.md">Instrução de macro de grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="if-then-else-macro-block.md">Bloco de macro If...Then...Else</a></p></td>
</tr>
<tr class="even">
<td><p>Bloco de dados</p></td>
<td><p><a href="createrecord-data-block.md">Ação de macro CreateRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloco de dados</p></td>
<td><p><a href="editrecord-data-block.md">Ação de macro EditRecord</a></p></td>
</tr>
<tr class="even">
<td><p>Bloco de dados</p></td>
<td><p><a href="foreachrecord-data-block.md">Ação de macro ForEachRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloco de dados</p></td>
<td><p><a href="lookuprecord-data-block.md">Bloco de dados LookupRecord</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Ação de macro CancelRecordChange</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação de macro ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="deleterecord-macro-action.md">Ação de macro DeleteRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Ação de macro ExitForEachRecord</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="logevent-macro-action.md">Ação de macro LogEvent</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação de macro OnError</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação de macro RaiseError</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="rundatamacro-macro-action.md">Ação de macro RunDataMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="sendemail-macro-action.md">Ação de macro SendEmail</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="setfield-macro-action.md">Ação de macro SetField</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="stopallmacros-macro-action.md">Ação de macro StopAllMacros</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação de macro StopMacro</a></p></td>
</tr>
</tbody>
</table>


Para criar uma Macro de Dados que capture o evento **Após Inserir**, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Após Inserir**.

2.  Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Inserir**.

Uma macro de dados vazia é exibida no designer de macros.

## <a name="example"></a>Exemplo

O exemplo de código a seguir usa o evento **Após Inserir** para executar alguns processos quando um registro é adicionado à tabela Doações. Quando um registro é adicionado, a quantidade de doações é adicionada ao campo DoaçõesRecebidas em Campanhas e ao campo TotaldaDoação na tabela Doa

**Clique aqui para exibir uma cópia da macro que você pode colar no Designer de Macros.**

Para exibir este exemplo no designer de macros, siga estas etapas:

1.  Abra a tabela na qual deseja capturar o evento **Após Inserir**.

2.  Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Inserir**.

3.  Selecione o código no exemplo de código a seguir e pressione CTRL+C para copiá-lo para a Área de Transfer

4.  Ative a janela do designer de macros e pressione CTRL+V.

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
