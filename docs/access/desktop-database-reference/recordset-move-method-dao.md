---
title: Método Recordset.Move (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1f10b5b779141189f114e420b3f7d4827e701161
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284796"
---
# <a name="recordsetmove-method-dao"></a>Método Recordset.Move (DAO)

**Aplica-se ao**: Access 2013, Office 2013

Move a posição do registro atual em um objeto **[Conjunto de registros](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* .Move (***Linhas***, ***StartBookmark***)

*expressão* Uma variável que representa um objeto **Conjunto de registros**.

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Linhas</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>O número de linhas que a posição vai mover. Se a quantidade de linhas for maior que 0, a posição será movida para a frente (em direção ao final do arquivo). Se a quantidade de linhas for menor que 0, a posição será movida para trás (em direção ao início do arquivo).</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um valor que identifica um marcador. Se você especificar startbookmark, a movimentação será iniciada em relação a este marcador. Caso contrário, Move começará a partir do registro atual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se você utilizar **Move** para posicionar o ponteiro do registro atual antes do primeiro registro, o ponteiro do registro atual será movido para o início do arquivo. Se o **Recordset** não contiver nenhum registro e sua propriedade **[BOF](recordset-bof-property-dao.md)** for **True**, utilizar esse método para mover para trás causará um erro.

Se você utilizar **Move** para posicionar o ponteiro do registro atual depois do último registro, a posição do ponteiro do registro atual será movida para o final do arquivo. Se o **Recordset** não contiver nenhum registro e sua propriedade **[EOF](recordset-eof-property-dao.md)** for **True**, utilizar esse método para mover para frente causará um erro.

Se a propriedade **BOF** ou **EOF** for **True** e você tentar usar o método **Move** sem um indicador válido, ocorrerá um erro de tempo de execução.

> [!NOTE]
> - Quando você usa **Move** em um objeto **Recordset** tipo somente encaminhamento, o argumento rows deve ser um inteiro positivo, e os indicadores não são permitidos. Isso significa que você só poderá mover para frente.
> - Para tornar o primeiro, o último, o anterior ou o próximo registro em um **Recordset** o registro atual, use o método **MoveFirst**, **MoveLast**, **MoveNext** ou **MovePrevious**.
> - Utilizar **Move** com linhas iguais a 0 é um modo fácil de recuperar dados de base para o registro atual. Isso é útil se você quiser confirmar se o registro atual tem os dados mais recentes a partir das tabelas base. Isso também poderá cancelar qualquer chamada **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)** pendente.


## <a name="example"></a>Exemplo

Este exemplo usa o método **Move** para posicionar o ponteiro do registro com base na entrada do usuário.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
