---
title: Método Recordset2. getRows (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7b20e2f41074e9f12198477a6abf2f1f1f9f719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309412"
---
# <a name="recordset2getrows-method-dao"></a>Método Recordset2. getRows (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Recupera várias linhas de um objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . GetRows (***numrows***)

*expressão* Uma variável que representa um objeto **Recordset2** .

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NumRows</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>O número de linhas a serem recuperadas.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Variant

## <a name="remarks"></a>Comentários

Use o método **GetRows** para copiar registros de um **Recordset**. **GetRows** retorna uma matriz bidimensional. A primeira subscript identifica o campo e a segunda, o número de linhas. Por exemplo, `intField` representa o campo e `intRecord` identifica o número da linha:

`avarRecords(intField, intRecord)`

Para obter o primeiro valor do campo na segunda linha retornada, use o código como se segue:

`field1 = avarRecords(0,1)`

Para obter o segundo valor do campo na primeira linha, use o código como se segue:

`field2 = avarRecords(1,0)`

A variável avarRecords automaticamente se torna uma matriz bidimensional quando **GetRows** retorna dados.

Se você solicitar mais linhas do que aquelas disponíveis, **GetRows** retornará apenas o número de linhas disponíveis. Você pode usar a função **UBound** do Visual Basic for Applications para determinar quantas linhas **GetRows** realmente recuperou, porque a matriz deve ajustar-se ao número de linhas retornadas. Por exemplo, se você retornou os resultados em uma **Variant** chamada vara, poderá usar o código a seguir para determinar quantas linhas foram realmente retornadas:

`numReturned = UBound(varA,2) + 1`

Você precisa usar "+ 1" por que a primeira linha retornada está no elemento 0 da matriz. O número de linhas que você pode recuperar está restrito pela quantidade de memória disponível. Você não deve usar **GetRows** para recuperar uma tabela inteira em uma matriz, se ela for grande.

Como **GetRows** retorna todos os campos do **Recordset** na matriz, inclusive os campos Memo e Long Binary, é possível usar uma consulta que restrinja os campos retornados.

Depois de chamar **GetRows**, o registro atual é posicionado na próxima linha não lida. Ou seja, **GetRows** tem o mesmo efeito no registro atual como **move**numrows.

Se você estiver tentando recuperar todas as linhas utilizando várias chamadas de **GetRows**, use a propriedade **[EOF](recordset2-eof-property-dao.md)** para ter certeza de que está no final do **Recordset**. **GetRows** retorna menos que o número solicitado se ele estiver no final de **Recordset** ou se ele não puder recuperar uma linha no intervalo solicitado. Por exemplo, se você estiver tentando recuperar 10 registros, mas não conseguir recuperar o quinto registro, **GetRows** retornará quatro registros e tornará o quinto registro o registro atual. Isso não irá gerar nenhum erro de tempo de execução. Isso pode ocorrer se outro usuário excluir um registro em um **Recordset** tipo dynaset. Consulte o exemplo para obter uma demonstração de como tratar isso.

## <a name="example"></a>Exemplo

Este exemplo usa o método **GetRows** para recuperar um número especificado de linhas de um **Recordset** e para preencher uma matriz com os dados resultantes. O método **GetRows** retornará menos do que o número desejado de linhas em dois casos: se **EOF** tiver sido atingido ou se **GetRows** tiver tentado recuperar um registro excluído por outro usuário. A função só retornará **Falso** se o segundo caso ocorrer. A função GetRowsOK é necessária para a execução deste procedimento.

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
