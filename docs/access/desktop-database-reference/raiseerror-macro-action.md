---
title: Ação da macro GerarErro
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300921"
---
# <a name="raiseerror-macro-action"></a>Ação da macro GerarErro

**Aplica-se ao:** Access 2013, Office 2013 

A ação **GerarErro** cria uma exceção que pode ser lidada pela ação de macro **[AoOcorrerErro](onerror-macro-action.md)**.

> [!NOTE]
> [!OBSERVAçãO] A ação **GerarErro** está disponível somente em Macros de Dados.

## <a name="setting"></a>Setting

A ação **GerarErro** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Número do erro</p></td>
<td><p>Sim</p></td>
<td><p>Um número ou uma expressão que resolve para o tipo de dados Long.</p></td>
</tr>
<tr class="even">
<td><p>Descrição do erro</p></td>
<td><p>Não</p></td>
<td><p>Uma expressão de cadeia de caracteres que descreve o erro.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se a ação **GerarErro** for chamada em um evento de macro **[Antes de Alterar](before-change-macro-event.md)** ou **[Antes de Excluir](before-delete-macro-event.md)**, o evento será cancelado.

Se não houver uma instrução **AoOcorrerErro** ativa lidando com erros, o erro gerado pela ação **GerarErro** será adicionado à tabela de sistema **USysApplicationLog**. Quando a ação **GerarErro** for gravada na tabela **USysApplicationLog**, a coluna **Categoria** será automaticamente definida como **Execução**.

Para ver a tabela **USysApplicationLog**, siga estas etapas:

1.  Clique no menu **Arquivo** e em **Opções.**

2.  Na caixa de diálogo **Opções do Access**, clique na guia **Bancos de Dados Atual**.

3.  Na seção **Navegação**, clique em **Opções de Navegação**.

4.  Na caixa de diálogo **Opções de Navegação**, clique em **Mostrar Objetos do Sistema** e clique em **OK**.

5.  Clique em **OK** para fechar a caixa de diálogo **Opções do Access**.

## <a name="example"></a>Exemplo

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
