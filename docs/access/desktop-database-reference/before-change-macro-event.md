---
title: Evento de macro Antes de Alterar
TOCTitle: Before Change Macro Event
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
ms.openlocfilehash: f54a1e7619022fc08b96066e85ccf49a298bae88
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465158"
---
# <a name="before-change-macro-event"></a>Evento de macro Antes de Alterar

**Aplica-se a**: Access 2013 | Office 2013

O evento **Antes de Alterar** ocorre quando um registro é alterado, mas antes da alteração ser submetida.

> [!NOTE]
> [!OBSERVAçãO] O evento **Antes de Alterar** está disponível somente em Macros de Dados.

## <a name="remarks"></a>Comentários

Use o evento **Antes de Alterar** para executar qualquer ação que você deseja que ocorra antes da alteração de um registro. O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.

Você pode usar a função **atualizado ("*Nome do campo*")** para determinar se um campo foi alterada. O exemplo de código a seguir mostra como usar uma instrução **If** para determinar se o campo PaidInFull foi alterado.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Use a propriedade **Inserido** para determinar se o evento **Antes de Alterar** foi acionado por um novo registro que está sendo criado ou por uma alteração em um registro existente. A propriedade **Inserido** apresentará o valor **True** se o evento tiver sido acionado por um novo registro, e **False** se o evento tiver sido acionado por uma alteração em um registro existente.

O exemplo de código a seguir mostra a sintaxe para o uso da propriedade **Inserido**.

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

Você pode acessar um valor anterior em um campo utilizando a sintaxe a seguir.

```vb
    [Old].[Field Name]
```

Por exemplo, para acessar o valor anterior do campo QuantidadeEmEstoque, use a sintaxe a seguir.

```vb
    [Old].[QuantityInStock]
```

Os valores anteriores são excluídos permanentemente após a conclusão do evento **Antes de Alterar**.

Você pode cancelar o evento **Antes de Alterar** utilizando a ação **GerarErro**. Quando um erro é exibido, as alterações contidas no evento **Antes de Alterar** são descartadas.

A tabela a seguir lista comandos de macro que podem ser usadas no evento **Antes de Alterar**.

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
<td><p><a href="lookuprecord-data-block.md">Ação de Macro Pesquisarregistro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação de macro ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação de macro OnError</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação de macro RaiseError</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="setfield-macro-action.md">Ação de macro SetField</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação de macro SetLocalVar</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação de macro StopMacro</a></p></td>
</tr>
</tbody>
</table>


Para criar uma Macro de Dados que capture o evento **Antes de Alterar**, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Antes de Alterar**.

2.  Na guia **Tabela**, no grupo **Antes de eventos**, clique em **Antes de Alterar**.

Uma macra de dados vazia é exibida no designer de macros.

## <a name="example"></a>Exemplo

O exemplo de código a seguir usa o evento **Antes de alterar** para validar os campos de Status. Um erro será exibido se houver um valor incorreto no campo Resolução.

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

Para exibir este exemplo no designer de macros, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Antes de Alterar**.

2.  Na guia **Tabela**, no grupo **Antes de Eventos**, clique em **Antes de Alterar**.

3.  Selecione o código no exemplo de código a seguir e pressione **CTRL + C** para copiá-lo na área de transferência.

4.  Ative a janela do designer de macro e, em seguida, pressione **CTRL + V**.



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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

O exemplo a seguir mostra como usar a ação Gerarerro para cancelar o evento de macro de dados antes de alterar. Quando o campo AssignedTo é atualizado, um bloco de dados Pesquisarregistro é usado para determinar se o técnico atribuído atualmente atribuído a uma solicitação de serviço em aberto. Se isso for verdadeiro, então o evento antes de alterar for cancelado e o registro não será atualizado.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
