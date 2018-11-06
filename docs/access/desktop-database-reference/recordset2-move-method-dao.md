---
title: Método Recordset2.move (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2231e94703b49fd14fb89d7642c0144c1dda532
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998592"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="54b9d-102">Método Recordset2.move (DAO)</span><span class="sxs-lookup"><span data-stu-id="54b9d-102">Recordset2.Move method (DAO)</span></span>

<span data-ttu-id="54b9d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="54b9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54b9d-104">Move a posição do registro atual em um objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="54b9d-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b9d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54b9d-105">Syntax</span></span>

<span data-ttu-id="54b9d-106">*expressão* . Move (***linhas***, ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="54b9d-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="54b9d-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="54b9d-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="54b9d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54b9d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="54b9d-109">Nome</span><span class="sxs-lookup"><span data-stu-id="54b9d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="54b9d-110">Obrigatório/opcional</span><span class="sxs-lookup"><span data-stu-id="54b9d-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="54b9d-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="54b9d-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="54b9d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="54b9d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="54b9d-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="54b9d-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="54b9d-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="54b9d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="54b9d-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="54b9d-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="54b9d-p101">O número de linhas que a posição será movida. Se rows for maior que 0, a posição será movida para frente (em direção ao final do arquivo). Se rows for menor que 0, a posição será movida para trás (em direção ao início do arquivo).</span><span class="sxs-lookup"><span data-stu-id="54b9d-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="54b9d-119"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="54b9d-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="54b9d-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="54b9d-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="54b9d-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="54b9d-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="54b9d-p102">Um valor identificando um indicador. Se você especificar startbookmark, Move começará relativo a esse indicador. Caso contrário, Move começará a partir do registro atual.</span><span class="sxs-lookup"><span data-stu-id="54b9d-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="54b9d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="54b9d-125">Remarks</span></span>

<span data-ttu-id="54b9d-p103">Se você usar **Move** para posicionar o ponteiro do registro atual antes do primeiro registro, o ponteiro do registro atual se moverá para o início do arquivo. Se o **Recordset** não contiver registros e sua propriedade **[BOF](recordset2-bof-property-dao.md)** for **True**, a utilização desse método para mover para trás causará um erro.</span><span class="sxs-lookup"><span data-stu-id="54b9d-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="54b9d-p104">Se você usar **Move** para posicionar o ponteiro do registro atual depois do último registro, a posição do ponteiro do registro atual se moverá para o fim do arquivo. Se o **Recordset** não contiver registros e sua propriedade **[EOF](recordset2-eof-property-dao.md)** for **True**, a utilização desse método para mover para frente causará um erro.</span><span class="sxs-lookup"><span data-stu-id="54b9d-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="54b9d-130">Se a propriedade **BOF** ou **EOF** for **True** e você tentar usar o método **Move** sem um indicador válido, ocorrerá um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="54b9d-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="54b9d-p105">Quando você usa **Move** em um objeto **Recordset** do tipo somente para encaminhamento, o argumento rows deve ser um inteiro positivo e não são permitidos indicadores. Isso significa que você pode mover apenas para a frente.</span><span class="sxs-lookup"><span data-stu-id="54b9d-p105">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span>
> - <span data-ttu-id="54b9d-133">Para definir o primeiro registro, o último, o próximo ou o anterior como o registro atual em um **Recordset**, use o método **MoveFirst**, **MoveLast**, **MoveNext** ou **MovePrevious**.</span><span class="sxs-lookup"><span data-stu-id="54b9d-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="54b9d-p106">Usar **Move** com rows igual a 0 é uma maneira fácil de recuperar os dados subjacentes do registro atual. Isso será útil se você desejar se certificar de que o registro atual tem os dados mais recentes das tabelas base. Também cancelará quaisquer chamadas pendentes de **[Edit](recordset2-edit-method-dao.md)** ou **[AddNew](recordset-addnew-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="54b9d-p106">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="54b9d-137">Exemplo</span><span class="sxs-lookup"><span data-stu-id="54b9d-137">Example</span></span>

<span data-ttu-id="54b9d-138">Este exemplo usa o método **Move** para posicionar o ponteiro do registro com base na entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="54b9d-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

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
