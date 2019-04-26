---
title: Evento de macro Após Atualização
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
localization_priority: Priority
ms.openlocfilehash: a96b46fcc78c4f93887e487f52091a77da6c0d2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297183"
---
# <a name="after-update-macro-event"></a>Evento de macro Após Atualização

**Aplica-se ao:** Access 2013, Office 2013

O evento **After Update** ocorre após a alteração de um registro.

> [!NOTE]
> O evento **After Update** só está disponível em Macros de Dados.

## <a name="remarks"></a>Comentários

Use o evento **After Update** para executar todas as ações que você deseja que ocorram quando um registro for alterado. Os usos comuns para **After Insert** incluem impor regras comerciais, atualização de um total agregado e envio de notificações.

Você pode usar a função **Updated("*Nome do Campo*")** para determinar se um campo foi alterado. O exemplo de código a seguir mostra como usar uma instrução **If** para determinar se o campo PaidInFull foi alterado.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Você pode usar o acesso ao valor anterior em um campo usando a sintaxe a seguir.

`[Old].[Field Name]`

Por exemplo, para acessar o valor anterior do campo QuantityIInStock, use a sintaxe a seguir.

`[Old].[QuantityInStock]`

Os valores anteriores serão permanentemente excluídos quando o evento **After Update** terminar.

A tabela a seguir lista comandos de macro que podem ser usados no evento **After Update**.

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


Para criar uma macro Data que captura o evento **After Update**, use estas etapas:

1.  Abra a tabela para a qual você deseja capturar o evento **After Update**.

2.  Na guia **Tabela**, no grupo **After Events**, clique em **After Update**.

Uma macro de dados vazia é exibida no designer de macros.

## <a name="example"></a>Exemplo

O exemplo de código a seguir usa o evento **After Update** para executar uma macro de dados nomeada que adiciona um registro à tabela Comentário sempre que o status de um problema for atualizado.

**Clique aqui para exibir uma cópia de macro que você pode colar no Designer de Macros.**

Para exibir este exemplo no designer de macros, use estas etapas:

1.  Abra a tabela para a qual você deseja capturar o evento **After Update**.

2.  Na guia **Tabela**, no grupo **After Events**, clique em **After Update**.

3.  Selecione o código no seguinte exemplo de código e então pressione CTRL+C para copiá-lo para a Área de Transferência.

4.  Ative a janela do designer de macros e pressione CTRL+V.

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

