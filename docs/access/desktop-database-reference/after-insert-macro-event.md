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
localization_priority: Priority
ms.openlocfilehash: c84a737d08b791bfe560bfe6af6bcc59a14d2678
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716135"
---
# <a name="after-insert-macro-event"></a>Evento da macro Após Inserção

**Aplica-se a**: Access 2013, o Office 2013

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
<td><p><a href="comment-macro-statement.md">Instrução de macro comentário</a></p></td>
</tr>
<tr class="even">
<td><p>Fluxo do programa</p></td>
<td><p><a href="group-macro-statement.md">Instrução de macro grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="if-then-else-macro-block.md">Se... Então... Bloco de macro Else</a></p></td>
</tr>
<tr class="even">
<td><p>Bloco de dados</p></td>
<td><p><a href="createrecord-data-block.md">Ação de macro CriarRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloco de dados</p></td>
<td><p><a href="editrecord-data-block.md">Ação de macro EditarRegistro</a></p></td>
</tr>
<tr class="even">
<td><p>Bloco de dados</p></td>
<td><p><a href="foreachrecord-data-block.md">Ação de macro ParaCadaRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Bloco de dados</p></td>
<td><p><a href="lookuprecord-data-block.md">Bloco de dados Pesquisarregistro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Ação de macro Cancelaralteraçãoderegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação de macro Limparerrodemacro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="deleterecord-macro-action.md">Ação de macro ExcluirRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Ação de macro SairParaCadaRegistro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="logevent-macro-action.md">Ação de macro RegistrarEvento</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação de macro Gerarerro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="rundatamacro-macro-action.md">Ação de macro ExecutarMacrodeDados</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="sendemail-macro-action.md">Ação de macro EnviarEmail</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="setfield-macro-action.md">Ação de macro Definircampo</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="stopallmacros-macro-action.md">Ação de macro PararTodasMacros</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></p></td>
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
