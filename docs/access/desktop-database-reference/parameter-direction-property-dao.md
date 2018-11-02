---
title: Propriedade Parameter.Direction (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f7d468d703989fdc26538d18cbc00eb950fe0e8e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930214"
---
# <a name="parameterdirection-property-dao"></a>Propriedade Parameter.Direction (DAO)


**Aplica-se a**: Access 2013, o Office 2013


## <a name="syntax"></a>Sintaxe

*expressão* . Direção

*expressão* Uma variável que representa um objeto **Parameter** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno é um Long que pode ser definido como uma das constantes **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)**.

Use a propriedade **Direction** para determinar se o parâmetro é de entrada, saída, ambos ou o valor de retorno do procedimento. Alguns drivers ODBC não fornecem informações sobre a direção dos parâmetros para uma instrução SELECT ou chamada de procedimento. Nesses casos, é necessário definir a direção antes de executar a consulta.

Por exemplo, o procedimento a seguir retorna um valor de um procedimento armazenado chamado "obter\_funcionários":

{? = chamada get\_funcionários}

Essa chamada gera um parâmetro  o valor de retorno. Você precisa definir a direção desse parâmetro como **dbParamOutput** ou **dbParamReturnValue** antes de executar **[QueryDef](querydef-object-dao.md)**.

Você precisa definir todas as direções de parâmetro, exceto **dbParamInput**, antes de acessar ou configurar os valores dos parâmetros e antes de executar **QueryDef**.

É necessário usar **dbParamReturnValue** para valores de retorno, mas nos casos em que aquela opção não é aceita pelo driver ou pelo servidor, você pode usar **dbParamOutput** no lugar.

O driver do Microsoft SQL Server define automaticamente a propriedade **Direction** para todos os parâmetros de procedimento. Nem todos os drivers ODBC podem determinar a direção de um parâmetro de consulta. Nesses casos, é necessário definir a direção antes de executar a consulta.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **Direction** para configurar os parâmetros de uma consulta para uma fonte de dados ODBC.

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

