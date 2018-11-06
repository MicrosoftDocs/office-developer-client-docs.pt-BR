---
title: Método Recordset2.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 598944aadb344ab97d7561e7ef55a67041c4fbf1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998742"
---
# <a name="recordset2clone-method-dao"></a>Método Recordset2.Clone (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Cria um objeto **[Recordset](recordset-object-dao.md)** duplicado que faz referência ao objeto **Recordset2** original.

## <a name="syntax"></a>Sintaxe

*expressão* . Clone

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="return-value"></a>Valor de retorno

Recordset

## <a name="remarks"></a>Comentários

Use o método **Clone** para criar vários objetos **Recordset** duplicados. Cada conjunto de registros pode ter seu próprio registro atual. Usar **Clone** sozinho não altera os dados nos objetos ou em suas estruturas subjacentes. Quando você usa o método **Clone**, é possível compartilhar indicadores entre dois ou mais objetos **Recordset2** porque seus indicadores são intercambiáveis.

Você pode usar o método **Clone** quando desejar executar uma operação em um conjunto de registros que exige vários registros atuais. Isso é mais rápido e mais eficiente do que abrir um segundo conjunto de registros. Quando você cria um conjunto de registros com o método **Clone**, ele inicialmente não tem um registro atual. Para tornar um registro atual antes de usar o clone de conjunto de registros, você deve definir a propriedade **[Bookmark](recordset2-bookmark-property-dao.md)** ou usar um dos métodos **[Move](recordset-movefirst-method-dao.md)**, ou um dos métodos **[Find](recordset2-findfirst-method-dao.md)** ou o método **[Seek](recordset2-seek-method-dao.md)**.

Usar o método **[Close](connection-close-method-dao.md)** no objeto original ou duplicado não afeta o outro objeto. Por exemplo, usar **Close** no conjunto de registros original não fecha o clone.

> [!NOTE]
> - Fechar um conjunto de registros clonado dentro de uma transação pendente provocará uma operação **Rollback** implícita.
> - Quando você clona um objeto **Recordset** do tipo tabela em um espaço de trabalho do Microsoft Access, a configuração da propriedade **[Index](recordset2-index-property-dao.md)** não é clonada na nova cópia do conjunto de registros. Você deve copiar a configuração da propriedade **Index** manualmente.

## <a name="example"></a>Exemplo

Este exemplo usa o método **Clone** para criar cópias de um conjunto de registros e, em seguida, permite que o usuário posicione o ponteiro do registro de cada cópia de maneira independente.

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
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
