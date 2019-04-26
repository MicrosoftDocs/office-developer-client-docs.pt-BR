---
title: Método Recordset.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: ecc5592893c1caee16f0a00687ce50f68b05e9c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300655"
---
# <a name="recordsetclone-method-dao"></a><span data-ttu-id="d7e50-102">Método Recordset.Clone (DAO)</span><span class="sxs-lookup"><span data-stu-id="d7e50-102">Recordset.Clone method (DAO)</span></span>

<span data-ttu-id="d7e50-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7e50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7e50-104">Cria um objeto do **[Conjunto de Registros](recordset-object-dao.md)** duplicado que se refere ao objeto do **Conjunto de Registros** original.</span><span class="sxs-lookup"><span data-stu-id="d7e50-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7e50-105">Syntax</span></span>

<span data-ttu-id="d7e50-106">*expressão* .Clone</span><span class="sxs-lookup"><span data-stu-id="d7e50-106">expression  . Clone</span></span>

<span data-ttu-id="d7e50-107">*expressão* Uma variável que representa um objeto do **Conjunto de Registros**.</span><span class="sxs-lookup"><span data-stu-id="d7e50-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7e50-108">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d7e50-108">Return value</span></span>

<span data-ttu-id="d7e50-109">Conjunto de Registros</span><span class="sxs-lookup"><span data-stu-id="d7e50-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="d7e50-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7e50-110">Remarks</span></span>

<span data-ttu-id="d7e50-p101">Use o método **Clone** para criar vários objetos **Recordset** duplicados. Cada **Recordset** pode ter seu próprio registro atual. Usar **Clone** sozinho não altera os dados nos objetos ou em suas estruturas subjacentes. Quando você usa o método **Clone**, é possível compartilhar indicadores entre dois ou mais objetos **Recordset** porque seus indicadores são intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="d7e50-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each **Recordset** can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="d7e50-p102">Você pode usar o método **Clone** quando desejar executar uma operação em um **Recordset** que exige vários registros atuais. Isso é mais rápido e mais eficiente do que abrir um segundo **Recordset**. Quando você cria um **Recordset** com o método **Clone**, ele inicialmente não tem um registro atual. Para transformar um registro em atual antes de usar o clone do **Recordset**, você deve definir a propriedade **[Bookmark](recordset-bookmark-property-dao.md)** ou usar um dos métodos **[Move](recordset-movefirst-method-dao.md)**, um dos métodos **[Find](recordset-findfirst-method-dao.md)** ou o método **[Seek](recordset-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d7e50-p102">You can use the **Clone** method when you want to perform an operation on a **Recordset** that requires multiple current records. This is faster and more efficient than opening a second **Recordset**. When you create a **Recordset** with the **Clone** method, it initially lacks a current record. To make a record current before you use the **Recordset** clone, you must set the **[Bookmark](recordset-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset-findfirst-method-dao.md)** methods, or the **[Seek](recordset-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="d7e50-p103">Usar o método **[Close](connection-close-method-dao.md)** no objeto original ou duplicado não afeta o outro objeto. Por exemplo, usar **Close** no **Recordset** original não fecha o clone.</span><span class="sxs-lookup"><span data-stu-id="d7e50-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original **Recordset** doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="d7e50-121">Fechar um conjunto de registros clonado dentro de uma transação pendente provocará uma operação **Rollback** implícita.</span><span class="sxs-lookup"><span data-stu-id="d7e50-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="d7e50-p104">Quando você clona um objeto **Recordset** do tipo tabela em um espaço de trabalho do Microsoft Access, a configuração da propriedade **[Index](recordset2-index-property-dao.md)** não é clonada na nova cópia do conjunto de registros. Você deve copiar a configuração da propriedade **Index** manualmente.</span><span class="sxs-lookup"><span data-stu-id="d7e50-p104">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset. You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="d7e50-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d7e50-124">Example</span></span>

<span data-ttu-id="d7e50-125">Este exemplo usa o método **Clone** para criar cópias de um **Recordset** e, em seguida, permite que o usuário posicione o ponteiro do registro de cada cópia de maneira independente.</span><span class="sxs-lookup"><span data-stu-id="d7e50-125">This example uses the **Clone** method to create copies of a **Recordset** and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
