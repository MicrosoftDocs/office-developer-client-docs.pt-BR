---
title: Método Recordset2.move (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ed9eb021df9d4c82473f1924a539787680f76a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928800"
---
# <a name="recordset2move-method-dao"></a>Método Recordset2.move (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Move a posição do registro atual em um objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . Move (***linhas***, ***StartBookmark***)

*expressão* Uma variável que representa um objeto **Recordset2** .

### <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Linhas</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>O número de linhas que a posição será movida. Se rows for maior que 0, a posição será movida para frente (em direção ao final do arquivo). Se rows for menor que 0, a posição será movida para trás (em direção ao início do arquivo).</p></td>
</tr>
<tr class="even">
<td><p>StartBookmark</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um valor identificando um indicador. Se você especificar startbookmark, Move começará relativo a esse indicador. Caso contrário, Move começará a partir do registro atual.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se você usar **Move** para posicionar o ponteiro do registro atual antes do primeiro registro, o ponteiro do registro atual se moverá para o início do arquivo. Se o **Recordset** não contiver registros e sua propriedade **[BOF](recordset2-bof-property-dao.md)** for **True**, a utilização desse método para mover para trás causará um erro.

Se você usar **Move** para posicionar o ponteiro do registro atual depois do último registro, a posição do ponteiro do registro atual se moverá para o fim do arquivo. Se o **Recordset** não contiver registros e sua propriedade **[EOF](recordset2-eof-property-dao.md)** for **True**, a utilização desse método para mover para frente causará um erro.

Se a propriedade **BOF** ou **EOF** for **True** e você tentar usar o método **Move** sem um indicador válido, ocorrerá um erro em tempo de execução.


> [!NOTE]
> <UL>
> <LI>
> <P>Quando você usa <STRONG>Move</STRONG> em um objeto <STRONG>Recordset</STRONG> do tipo somente para encaminhamento, o argumento rows deve ser um inteiro positivo e não são permitidos indicadores. Isso significa que você pode mover apenas para a frente.</P>
> <LI>
> <P>Para definir o primeiro registro, o último, o próximo ou o anterior como o registro atual em um <STRONG>Recordset</STRONG>, use o método <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG> ou <STRONG>MovePrevious</STRONG>.</P>
> <LI>
> <P>Usar <STRONG>Move</STRONG> com rows igual a 0 é uma maneira fácil de recuperar os dados subjacentes do registro atual. Isso será útil se você desejar se certificar de que o registro atual tem os dados mais recentes das tabelas base. Também cancelará quaisquer chamadas pendentes de <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> ou <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG>.</P></LI></UL>



## <a name="example"></a>Exemplo

Este exemplo usa o método **Move** para posicionar o ponteiro do registro com base na entrada do usuário.

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
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
