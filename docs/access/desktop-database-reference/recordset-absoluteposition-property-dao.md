---
title: Propriedade Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702497"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="d96bb-102">Propriedade Recordset.AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="d96bb-102">Recordset.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="d96bb-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d96bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d96bb-104">Define ou retorna o número de registro relativo do registro atual de um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d96bb-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d96bb-105">Syntax</span></span>

<span data-ttu-id="d96bb-106">*expressão* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="d96bb-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="d96bb-107">*expressão* Uma variável que representa um objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d96bb-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d96bb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d96bb-108">Remarks</span></span>

<span data-ttu-id="d96bb-p101">Você pode usar a propriedade **AbsolutePosition** para posicionar o ponteiro do registro atual para um registro específico baseado na sua posição ordinal, em um objeto **Recordset** tipo dynaset ou instantâneo. Você também pode determinar o número atual do registro, verificando a configuração da propriedade **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="d96bb-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="d96bb-p102">Como o valor da propriedade **AbsolutePosition** é zero (isto é, uma configuração de 0 se refere aos primeiro registro no objeto **Recordset**), você não pode defini-lo como um valor maior ou igual ao número de registros preenchidos; fazer isso pode causar um erro interceptável. Você pode determinar o número de registros preenchidos no objeto **Recordset**, verificando a configuração da propriedade **RecordCount**. A configuração máxima permitida para a propriedade **AbsolutePosition** é o valor da propriedade **RecordCount** menos 1.</span><span class="sxs-lookup"><span data-stu-id="d96bb-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="d96bb-114">Se não houver nenhum registro atual, como quando não há nenhum registro no objeto **Recordset** , **AbsolutePosition** retorna – 1.</span><span class="sxs-lookup"><span data-stu-id="d96bb-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="d96bb-115">Se o registro atual for excluído, o valor da propriedade **AbsolutePosition** não será definido, e ocorrerá um erro interceptável se ele for referenciado.</span><span class="sxs-lookup"><span data-stu-id="d96bb-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="d96bb-116">Novos registros são adicionados ao final da sequência.</span><span class="sxs-lookup"><span data-stu-id="d96bb-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="d96bb-p104">Você não deve usar essa propriedade como um número de registro substituto. Os indicadores ainda são a forma recomendada de reter e retornar a uma determinada posição e são a única maneira de posicionar o registro atual em todos os tipos de objetos **Recordset**. Em particular, a posição de um registro é alterada quando um ou mais registros anteriores a ele são excluídos. Também não há nenhuma garantia de que um registro terá a mesma posição absoluta se o objeto **Recordset** for recriado, pois a ordem de registros individuais dentro de um objeto **Recordset** não é garantida, a menos que ela seja criada com uma instrução SQL, utilizando uma cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="d96bb-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="d96bb-p105">Definir a propriedade **AbsolutePosition** para um valor maior que zero em um objeto **Recordset** recém-aberto, mas não preenchido, causa um erro interceptável. Preencha o objeto **Recordset** primeiro com o método **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="d96bb-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error. Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="d96bb-123">A propriedade **AbsolutePosition** não está disponível nos objetos **Recordset** do tipo somente encaminhamento ou nos objetos **Recordset** abertos a partir de consultas passagem nos Microsoft Access banco de dados conectados ao mecanismo bancos de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="d96bb-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="d96bb-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d96bb-124">Example</span></span>

<span data-ttu-id="d96bb-125">Este exemplo usa a propriedade **AbsolutePosition** para controlar o progresso de um loop que enumera todos os registros de um **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d96bb-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
