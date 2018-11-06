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
ms.openlocfilehash: aa5a04ec08136dda637aabff15d89f81be6ecde8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998571"
---
# <a name="recordsetclone-method-dao"></a>Método Recordset.Clone (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Cria um objeto **[Recordset](recordset-object-dao.md)** duplicado que faz referência ao objeto **Recordset** original.

## <a name="syntax"></a>Sintaxe

*expressão* . Clone

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="return-value"></a>Valor de retorno

Recordset

## <a name="remarks"></a>Comentários

Use o método **Clone** para criar vários objetos **Recordset** duplicados. Cada **Recordset** pode ter seu próprio registro atual. Usar **Clone** sozinho não altera os dados nos objetos ou em suas estruturas subjacentes. Quando você usa o método **Clone**, é possível compartilhar indicadores entre dois ou mais objetos **Recordset** porque seus indicadores são intercambiáveis.

Você pode usar o método **Clone** quando desejar executar uma operação em um **Recordset** que exige vários registros atuais. Isso é mais rápido e mais eficiente do que abrir um segundo **Recordset**. Quando você cria um **Recordset** com o método **Clone**, ele inicialmente não tem um registro atual. Para transformar um registro em atual antes de usar o clone do **Recordset**, você deve definir a propriedade **[Bookmark](recordset-bookmark-property-dao.md)** ou usar um dos métodos **[Move](recordset-movefirst-method-dao.md)**, um dos métodos **[Find](recordset-findfirst-method-dao.md)** ou o método **[Seek](recordset-seek-method-dao.md)**.

Usar o método **[Close](connection-close-method-dao.md)** no objeto original ou duplicado não afeta o outro objeto. Por exemplo, usar **Close** no **Recordset** original não fecha o clone.

> [!NOTE]
> - Fechar um conjunto de registros clonado dentro de uma transação pendente provocará uma operação **Rollback** implícita.
> - Quando você clona um objeto **Recordset** do tipo tabela em um espaço de trabalho do Microsoft Access, a configuração da propriedade **[Index](recordset2-index-property-dao.md)** não é clonada na nova cópia do conjunto de registros. Você deve copiar a configuração da propriedade **Index** manualmente.

## <a name="example"></a>Exemplo

Este exemplo usa o método **Clone** para criar cópias de um **Recordset** e, em seguida, permite que o usuário posicione o ponteiro do registro de cada cópia de maneira independente.

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
