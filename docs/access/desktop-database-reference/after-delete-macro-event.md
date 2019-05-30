---
title: Evento da macro Após Exclusão
TOCTitle: After Delete macro event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5b3b2da44d817885eb6190a8cbbfc73bf99e9e0a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538232"
---
# <a name="after-delete-macro-event"></a>Evento da macro Após Exclusão

**Aplica-se a:** Access 2013, Office 2013

O evento **Após Exclusão** ocorre após a exclusão de cada evento.

> [!NOTE]
> O evento **Após Exclusão** está disponível somente em Macros de Dados.

## <a name="remarks"></a>Comentários

Use o evento **Após Exclusão** para executar qualquer ação que você deseja que ocorra após a exclusão de um registro. As utilizações mais comuns do **Após Exclusão** incluem a aplicação de regras de negócio, fluxos de trabalho, a atualização de um total agregado e o envio de notificações.

Quando o evento **Após Exclusão** ocorre, os valores contidos no registro excluído ainda permanecem disponíveis. Você pode querer usar um valor excluído para incrementar ou decrementar um total, criar uma trilha de auditoria ou comparar com um valor existente em um argumento *WhereCondition* .

Você pode usar a função **Updated("*Nome do Campo*")** para determinar se um campo foi alterado. O código de exemplo a seguir mostra como usar uma instrução Se para determinar se o campo PaidInFull foi alterado.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Você pode acessar um valor no registro excluído utilizando a sintaxe a seguir

`[Old].[Field Name]`

Por exemplo, para acessar o valor do campo QuantityInStock no registro excluído, use a seguinte sintaxe.

`[Old].[QuantityInStock]`

Os valores contidos no registro excluído são excluídos permanentemente após a conclusão do evento **Após Exclusão**.

Os comandos de macro a seguir podem ser usados no evento **After Delete** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de Comando</p></th>
<th><p>Comando</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fluxo do programa</p></td>
<td><p><a href="comment-macro-statement.md">Instrução de macro Comentário</a></p></td>
</tr>
<tr class="even">
<td><p>Fluxo do Programa</p></td>
<td><p><a href="group-macro-statement.md">Instrução de macro Grupo</a></p></td>
</tr>
<tr class="odd">
<td><p>Fluxo do Programa</p></td>
<td><p><a href="if-then-else-macro-block.md">Bloco de macro Se... Então... Senão</a></p></td>
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
<td><p><a href="lookuprecord-data-block.md">Bloco de dados PesquisarRegistro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Ação de macro CancelarAlteraçãodeRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação de macro LimparErrodaMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="deleterecord-macro-action.md">Ação de macro ExcluirRegistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Ação de macro SairparaCadaRegistro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="logevent-macro-action.md">Ação de macro RegistrarEvento</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação de macro GerarErro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="rundatamacro-macro-action.md">Ação de macro ExecutarMacrodeDados</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="sendemail-macro-action.md">Ação de macro EnviarEmail</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="setfield-macro-action.md">Ação de macro DefinirCampo</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="stopallmacros-macro-action.md">Ação de macro PararTodasMacros</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></p></td>
</tr>
</tbody>
</table>


Para criar uma Macro de Dados que capture o evento **Após Exclusão**, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Após Exclusão**.

2.  Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Exclusão**.

Uma Macro de Dados vazia é exibida no designer de macros.

## <a name="example"></a>Exemplo

O exemplo de código a seguir usa o evento **Após Exclusão** para executar alguns processos quando um registro é excluído da tabela Doações. Quando um registro é excluído, a quantidade de doações é subtraída do campo DoaçõesRecebidas em DoaçõesRecebidas e do campo TotaldaDoação na tabela Doadores.

**Clique aqui para exibir uma cópia de macro que você pode colar no Designer de Macros.**

Para exibir este exemplo no designer de macros, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Após Exclusão**.

2.  Na guia **Tabela**, no grupo **Após Eventos**, clique em **Após Exclusão**.

3.  Selecione o código listado abaixo e pressione CTRL+C para copiá-lo para a área de transferência.

4.  Ative a janela do designer de macros e pressione CTRL+V.

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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
