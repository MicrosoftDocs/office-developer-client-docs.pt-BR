---
title: Propriedade Recordset2. AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4de869866e2aeb28032553be78bee7af16f60402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307508"
---
# <a name="recordset2absoluteposition-property-dao"></a><span data-ttu-id="45f08-102">Propriedade Recordset2. AbsolutePosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="45f08-102">Recordset2.AbsolutePosition property (DAO)</span></span>

<span data-ttu-id="45f08-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45f08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45f08-104">Define ou retorna o número de registros relativos de um registro atual do objeto **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="45f08-104">Sets or returns the relative record number of a **Recordset2** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45f08-105">Syntax</span></span>

<span data-ttu-id="45f08-106">*expressão* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="45f08-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="45f08-107">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="45f08-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="45f08-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="45f08-108">Remarks</span></span>

<span data-ttu-id="45f08-p101">Você pode usar a propriedade **AbsolutePosition** para posicionar o ponteiro do registro atual em um registro específico com base em sua posição ordinal em um objeto **Recordset2** do tipo dynaset ou instantâneo. Também será necessário determinar o número de registros atual pela verificação da definição da propriedade **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="45f08-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset2** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="45f08-p102">Como o valor da propriedade **AbsolutePosition** está baseado em zero (ou seja, uma definição de 0 refere-se ao primeiro registro do objeto **Recordset2**), não será possível definir um valor maior ou igual ao número de registros preenchidos, pois isso ocasionará um erro interceptável. Determine o número de registros preenchidos no objeto **Recordset2** por meio da verificação da definição da propriedade **RecordCount**. A definição máxima permitida da propriedade **AbsolutePosition** é o valor da propriedade **RecordCount** menos 1.</span><span class="sxs-lookup"><span data-stu-id="45f08-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset2** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset2** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="45f08-114">Se não houver nenhum registro atual, como quando não há registros no objeto **Recordset2** , **AbsolutePosition** retornará – 1.</span><span class="sxs-lookup"><span data-stu-id="45f08-114">If there is no current record, as when there are no records in the **Recordset2** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="45f08-115">Caso o registro atual seja excluído, o valor da propriedade **AbsolutePosition** não será definido e ocorrerá um erro interceptável se for mencionado.</span><span class="sxs-lookup"><span data-stu-id="45f08-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="45f08-116">Os novos registros serão adicionados ao final da sequência.</span><span class="sxs-lookup"><span data-stu-id="45f08-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="45f08-p104">Você não deverá usar essa propriedade como um número de registro substituto. Os indicadores ainda são a forma recomendada de retenção e de retorno de uma determinada posição e são a única forma de posicionamento do registro atual em todos os tipos de objetos **Recordset2**. Em especial, a posição de um registro será alterada quando um ou vários registros precedentes forem excluídos. Também não existirá nenhuma garantia de que um registro terá a mesma posição absoluta, se o objeto **Recordset2** recriado novamente devido à ordem dos registros individuais em um objeto **Recordset** não for garantido, a não ser que seja criada com uma instrução SQL por meio da cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="45f08-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset2** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset2** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="45f08-p105">A definição da propriedade **AbsolutePosition** como um valor maior que zero em um objeto **Recordset2** recentemente aberto, mas não preenchido, causará um erro interceptável. Preencha primeiro o objeto **Recordset2** com o método **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="45f08-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset2** object causes a trappable error. Populate the **Recordset2** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="45f08-123">A propriedade **AbsolutePosition** não está disponível em objetos **Recordset2** somente de encaminhamento – ou nos objetos **Recordset2** abertos a partir de consultas passagem em bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="45f08-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset2** objects, or on **Recordset2** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="45f08-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="45f08-124">Example</span></span>

<span data-ttu-id="45f08-125">Este exemplo usa a propriedade **AbsolutePosition** para rastrear o progresso de um loop que enumera todos os registros de um **Recordset2**.</span><span class="sxs-lookup"><span data-stu-id="45f08-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset2**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
