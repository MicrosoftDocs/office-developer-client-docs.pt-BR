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
# <a name="before-change-macro-event"></a>Evento da macro Antes da Alteração

**Aplica-se ao:** Access 2013, Office 2013

O evento **Antes de Alterar** ocorre quando um registro é alterado, mas antes da alteração ser submetida.

> [!NOTE]
> O evento **Antes de Alterar** está disponível somente em Macros de Dados.

## <a name="remarks"></a>Comentários

Use o evento **Antes de Alterar** para executar qualquer ação que você deseja que ocorra antes da alteração de um registro. O **Antes de Alterar** é comumente usado para executar validação e criar mensagens de erro personalizadas.

Você pode usar a função **Updated("*Nome do Campo*")** para determinar se um campo foi alterado. O exemplo de código a seguir mostra como usar **uma instrução If** para determinar se o campo PaidInFull foi alterado.

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

Você pode usar o acesso ao valor anterior em um campo usando a sintaxe a seguir.

```vb
    [Old].[Field Name]
```

Por exemplo, para acessar o valor anterior do campo QuantityIInStock, use a sintaxe a seguir.

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
<td><p><a href="lookuprecord-data-block.md">Ação da macro LookupRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Ação de macro LimparErrodaMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="onerror-macro-action.md">Ação de macro AoOcorrerErro</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="raiseerror-macro-action.md">Ação de macro GerarErro</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="setfield-macro-action.md">Ação de macro DefinirCampo</a></p></td>
</tr>
<tr class="odd">
<td><p>Ação de Dados</p></td>
<td><p><a href="setlocalvar-macro-action.md">Ação de macro DefinirVarLocal</a></p></td>
</tr>
<tr class="even">
<td><p>Ação de Dados</p></td>
<td><p><a href="stopmacro-macro-action.md">Ação de macro PararMacro</a></p></td>
</tr>
</tbody>
</table>


Para criar uma Macro de Dados que capture o evento **Antes de Alterar**, siga estas etapas.

1.  Abra a tabela na qual deseja capturar o evento **Antes de Alterar**.

2.  Na guia **Tabela**, no grupo **Antes de eventos**, clique em **Antes de Alterar**.

Uma macro de dados vazia é exibida no designer de macros.

## <a name="example"></a>Exemplo

O exemplo de código a seguir usa o **evento Before Change** para validar os campos Status. Um erro será exibido se houver um valor incorreto no campo Resolução.

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

3.  Selecione o código no exemplo de código a seguir e pressione **CTRL+C** para copiá-lo para a área de transferência.

4.  Ative a janela do designer de macros e pressione **CTRL+V.**



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

O exemplo a seguir mostra como usar a ação RaiseError para cancelar o evento de macro de dados Antes de Alterar. Quando o campo AssignedTo é atualizado, um bloco de dados LookupRecord é usado para determinar se o técnico atribuído está atribuído no momento a uma solicitação de serviço aberta. Se isso for verdadeiro, o evento Antes de Alterar será cancelado e o registro não será atualizado.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
