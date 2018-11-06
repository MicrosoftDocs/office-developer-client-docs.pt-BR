---
title: Método Recordset.GetRows (DAO)
TOCTitle: GetRows method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ec7947fd5d8d15eee92a033a47a8574f2933e73b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998382"
---
# <a name="recordsetgetrows-method-dao"></a><span data-ttu-id="3172a-102">Método Recordset.GetRows (DAO)</span><span class="sxs-lookup"><span data-stu-id="3172a-102">Recordset.GetRows method (DAO)</span></span>

<span data-ttu-id="3172a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="3172a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3172a-104">Recupera várias linhas de um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="3172a-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3172a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3172a-105">Syntax</span></span>

<span data-ttu-id="3172a-106">*expressão* . GetRows (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="3172a-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="3172a-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="3172a-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3172a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3172a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3172a-109">Nome</span><span class="sxs-lookup"><span data-stu-id="3172a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3172a-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="3172a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3172a-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3172a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="3172a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3172a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3172a-113"><em>NumRows</em></span><span class="sxs-lookup"><span data-stu-id="3172a-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="3172a-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="3172a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="3172a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3172a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3172a-116">O número de linhas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="3172a-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="3172a-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3172a-117">Return value</span></span>

<span data-ttu-id="3172a-118">Variant</span><span class="sxs-lookup"><span data-stu-id="3172a-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="3172a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3172a-119">Remarks</span></span>

<span data-ttu-id="3172a-120">Use o método **GetRows** para copiar registros de um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3172a-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="3172a-121">**GetRows** retorna uma matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="3172a-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="3172a-122">A primeira assinatura identifica o campo e a segunda identifica o número da linha.</span><span class="sxs-lookup"><span data-stu-id="3172a-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="3172a-123">Por exemplo, `intField` representa o campo, e `intRecord` identifica o número da linha:</span><span class="sxs-lookup"><span data-stu-id="3172a-123">For example, `intField` represents the field, and `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="3172a-124">Para obter o valor do primeiro campo na segunda linha retornada, use código como este:</span><span class="sxs-lookup"><span data-stu-id="3172a-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="3172a-125">Para obter o segundo valor do campo na primeira linha, use código como este:</span><span class="sxs-lookup"><span data-stu-id="3172a-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="3172a-126">A variável avarRecords automaticamente se torna uma matriz bidimensional quando **GetRows** retorna dados.</span><span class="sxs-lookup"><span data-stu-id="3172a-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="3172a-127">Se você solicitar mais linhas do que as disponíveis, então **GetRows** retornará somente o número de linhas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3172a-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="3172a-128">Você pode usar a função **UBound** do Visual Basic for Applications para determinar quantas linhas **GetRows** realmente recuperou, já que a matriz é dimensionada para ajustar o número de linhas retornadas.</span><span class="sxs-lookup"><span data-stu-id="3172a-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="3172a-129">Por exemplo, se você tiver retornado os resultados em uma **Variant** chamado varA, você pode usar o código a seguir para determinar quantas linhas foram realmente retornadas:</span><span class="sxs-lookup"><span data-stu-id="3172a-129">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="3172a-p103">Você precisa usar "+ 1" por que a primeira linha retornada está no elemento 0 da matriz. O número de linhas que você pode retornar é restringido pela quantidade de memória disponível. Você não deve usar **GetRows** para recuperar a tabela inteira para uma matriz caso ela seja grande.</span><span class="sxs-lookup"><span data-stu-id="3172a-p103">You need to use "+ 1" because the first row returned is in the 0 element of the array. The number of rows that you can retrieve is constrained by the amount of available memory. You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="3172a-133">Como **GetRows** retorna todos os campos do **Recordset** para a matriz, incluindo os campos Memorandos e Binário Longo, talvez queira usar uma consta que restrinja os campos retornados.</span><span class="sxs-lookup"><span data-stu-id="3172a-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="3172a-134">Depois de chamar **GetRows**, o registro atual é posicionado na próxima linha não lida.</span><span class="sxs-lookup"><span data-stu-id="3172a-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="3172a-135">Ou seja, **GetRows** tem o mesmo efeito no registro atual numrows **Mover** .</span><span class="sxs-lookup"><span data-stu-id="3172a-135">That is, **GetRows** has the same effect on the current record as **Move** numrows.</span></span>

<span data-ttu-id="3172a-p105">Se você estiver tentando recuperar todas as linhas usando várias chamadas a **GetRows**, use a propriedade **[EOF](recordset-eof-property-dao.md)** para garantir que você esteja no final do **Recordset**. **GetRows** retornará menos do que o número solicitado se estiver no final do **Recordset** ou se não puder recuperar uma linha no intervalo solicitado. Por exemplo, se você estiver tentando recuperar 10 registros mas não puder recuperar o quinto registro, **GetRows** retornará quatro registros e transformará o quinto registro no registro atual. Isso não gerará um erro de tempo de execução. Isso pode ocorrer caso um usuário exclua um registro em um **Recordset** do tipo dynaset. Veja o exemplo para obter uma demonstração de como lidar com isso.</span><span class="sxs-lookup"><span data-stu-id="3172a-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="3172a-142">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3172a-142">Example</span></span>

<span data-ttu-id="3172a-p106">Este exemplo usa o método **GetRows** para recuperar um número especificado de linhas de um **Recordset** e para preencher uma matriz com os dados resultantes. O método **GetRows** retornará menos do que o número desejado de linhas em dois casos: se **EOF** tiver sido atingido ou se **GetRows** tiver tentado recuperar um registro excluído por outro usuário. A função só retornará **Falso** se o segundo caso ocorrer. A função GetRowsOK é necessária para a execução deste procedimento.</span><span class="sxs-lookup"><span data-stu-id="3172a-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function GetRowsOK(rstTemp As Recordset, _ 
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
