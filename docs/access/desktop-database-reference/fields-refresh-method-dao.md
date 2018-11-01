---
title: Método Fields.Refresh (DAO)
TOCTitle: Refresh Method
ms:assetid: d08597d8-bad6-523b-a083-d824f85b64bc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834723(v=office.15)
ms:contentKeyID: 48547844
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1804585f3c3bc4a796da00dfede5a482d65a82a1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889613"
---
# <a name="fieldsrefresh-method-dao"></a><span data-ttu-id="a9412-102">Método Fields.Refresh (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9412-102">Fields.Refresh Method (DAO)</span></span>


<span data-ttu-id="a9412-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9412-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a9412-104">Atualiza os objetos na coleção especificada para refletir o esquema atual do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a9412-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9412-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9412-105">Syntax</span></span>

<span data-ttu-id="a9412-106">*expressão* . Atualizar</span><span class="sxs-lookup"><span data-stu-id="a9412-106">*expression* .Refresh</span></span>

<span data-ttu-id="a9412-107">*expressão* Uma variável que representa um objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="a9412-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9412-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9412-108">Remarks</span></span>

<span data-ttu-id="a9412-p101">Para determinar a posição que o mecanismo de banco de dados do Microsoft Access usa para os objetos **Field** na coleção **Fields** de um objeto **QueryDef**, **Recordset** ou **TableDef**, utilize a propriedade **OrdinalPosition** de cada objeto **Field**. Alterar a propriedade **OrdinalPosition** de um objeto **Field** pode não alterar a ordem dos objetos **Field** na coleção até que você use o método **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="a9412-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="a9412-p102">Use o método **Refresh** em um ambiente de vários usuários no qual outros usuários podem alterar o banco de dados. Você também pode precisar utilizá-lo em coleções que são indiretamente afetas pelas alterações no banco de dados. Por exemplo, se você alterar uma coleção **Users**, poderá precisar atualizar uma coleção **Groups** antes de utilizar a coleção **Groups**.</span><span class="sxs-lookup"><span data-stu-id="a9412-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="a9412-p103">Uma coleção é preenchida com objetos quando ela se refere, pela primeira vez, a e não reflete automaticamente as alterações subsequentes feitas por outros usuários. Se provavelmente outro usuário alterou uma coleção, use o método Refresh na coleção imediatamente antes de executar qualquer tarefa no aplicativo que considera a presença ou a ausência de um objeto particular na coleção. Isso garante que a coleção seja atualizada assim que possível. Por outro lado, utilizar Refresh pode desnecessariamente reduzir o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a9412-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

## <a name="example"></a><span data-ttu-id="a9412-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a9412-118">Example</span></span>

<span data-ttu-id="a9412-p104">Este exemplo usa o método **Refresh** para atualizar a coleção **Fields** da tabela Categories com base nas alterações nos dados de **OrdinalPosition**. A ordem de **Fields** na coleção muda somente depois de o método **Refresh** ser usado.</span><span class="sxs-lookup"><span data-stu-id="a9412-p104">This example uses the **Refresh** method to update the **Fields** collection of the Categories table based on changes to the **OrdinalPosition** data. The order of the **Fields** in the collection changes only after the **Refresh** method is used.</span></span>

```vb
    Sub RefreshX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Categories") 
     
     With tdfEmployees 
     ' Display original OrdinalPosition data and store it 
     ' in an array. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldLoop In .Fields 
     fldLoop.OrdinalPosition = _ 
     100 - fldLoop.OrdinalPosition 
     Next fldLoop 
     Set fldLoop = Nothing 
     
     ' Print new data. 
     Debug.Print "New OrdinalPosition data before Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     .Fields.Refresh 
     
     ' Print new data, showing how the field order has been 
     ' changed. 
     Debug.Print "New OrdinalPosition data after Refresh." 
     For Each fldLoop In .Fields 
     Debug.Print , fldLoop.OrdinalPosition, fldLoop.Name 
     Next fldLoop 
     
     ' Restore original OrdinalPosition data. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
