---
title: Propriedade Recorset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb3d73cc236821d56e2151d80cf0e0aba241b8c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463065"
---
# <a name="recordsetrecordcount-property-dao"></a>Propriedade Recorset.RecordCount (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Retorna o número de registros acessados em um objeto **[Recordset](recordset-object-dao.md)** ou o número total de registros em um objeto **Recordset** do tipo tabela ou em um objeto **[TableDef](tabledef-object-dao.md)**. **Long** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . RecordCount

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Use a propriedade **RecordCount** para descobrir quantos registros de um objeto **Recordset** ou **TableDef** foram acessados. A propriedade **RecordCount** não indica quantos registros estão contido em um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento, até que todos os registros foram acessados. Assim que o último registro tiver sido acessado, a propriedade **RecordCount** indicará o número total de registros não excluídos no objeto **Recordset** ou **TableDef**. Para impor que o último registro seja acessado, use o método **[MoveLast](recordset-movelast-method-dao.md)** no objeto **Recordset**. Você também pode usar uma função **Count** SQL para determinar o número aproximado de registros que a sua consulta retornará.


> [!NOTE]
> <P>[!OBSERVAçãO] Usar o método <STRONG>MoveLast</STRONG> para preencher um <STRONG>Recordset</STRONG> recém-aberto afeta negativamente o desempenho. A menos que seja necessário ter uma <STRONG>RecordCount</STRONG> precisa assim que você abrir um <STRONG>Recordset</STRONG>, será melhor aguardar até o preenchimento do <STRONG>Recordset</STRONG> com outras partes de código antes da verificação da propriedade <STRONG>RecordCount</STRONG>.</P>



À medida que seu aplicativo exclui registros em um objeto **Recordset** do tipo dynaset, o valor da propriedade **RecordCount** será reduzido. Entretanto, os registros excluídos por outros usuários não serão refletidos pela propriedade **RecordCount** até o registro atual ser posicionado em um registro excluído. Se você executar uma transação que afete a configuração da propriedade **RecordCount** e se depois a transação for revertida, a propriedade **RecordCount** não afetará o número real de registros restantes.

A propriedade **RecordCount** de um objeto **Recordset** de instantâneo – ou – tipo forward only não é afetada pelas alterações nas tabelas base.

Um objeto **Recordset** ou **TableDef** sem registros tem a propriedade **RecordCount** configurada como 0.

O uso do método **[Requery](recordset-requery-method-dao.md)** em um objeto **Recordset** redefine a propriedade **RecordCount** como se a consulta tivesse sido executada novamente.

## <a name="example"></a>Exemplo

Este exemplo demonstra a propriedade **RecordCount** com tipos diferentes de **Recordsets** antes e depois de preenchidos.

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```