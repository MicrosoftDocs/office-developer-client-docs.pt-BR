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
ms.openlocfilehash: c06fbf6bb3424e776e21f32343c8cdb8a795b604
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877104"
---
# <a name="parameterdirection-property-dao"></a><span data-ttu-id="779dc-102">Propriedade Parameter.Direction (DAO)</span><span class="sxs-lookup"><span data-stu-id="779dc-102">Parameter.Direction Property (DAO)</span></span>


<span data-ttu-id="779dc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="779dc-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="779dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="779dc-104">Syntax</span></span>

<span data-ttu-id="779dc-105">*expressão* . Direção</span><span class="sxs-lookup"><span data-stu-id="779dc-105">*expression* .Direction</span></span>

<span data-ttu-id="779dc-106">*expressão* Uma variável que representa um objeto **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="779dc-106">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="779dc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="779dc-107">Remarks</span></span>

<span data-ttu-id="779dc-108">A configuração ou o valor de retorno é um Long que pode ser definido como uma das constantes **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="779dc-108">The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="779dc-p101">Use a propriedade **Direction** para determinar se o parâmetro é de entrada, saída, ambos ou o valor de retorno do procedimento. Alguns drivers ODBC não fornecem informações sobre a direção dos parâmetros para uma instrução SELECT ou chamada de procedimento. Nesses casos, é necessário definir a direção antes de executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="779dc-p101">Use the **Direction** property to determine whether the parameter is an input parameter, output parameter, both, or the return value from the procedure. Some ODBC drivers do not provide information on the direction of parameters to a SELECT statement or procedure call. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

<span data-ttu-id="779dc-112">Por exemplo, o procedimento a seguir retorna um valor de um procedimento armazenado chamado "obter\_funcionários":</span><span class="sxs-lookup"><span data-stu-id="779dc-112">For example, the following procedure returns a value from a stored procedure named "get\_employees":</span></span>

<span data-ttu-id="779dc-113">{?</span><span class="sxs-lookup"><span data-stu-id="779dc-113"></span></span> <span data-ttu-id="779dc-114">= chamada get\_funcionários}</span><span class="sxs-lookup"><span data-stu-id="779dc-114">= call get\_employees}</span></span>

<span data-ttu-id="779dc-p103">Essa chamada gera um parâmetro  o valor de retorno. Você precisa definir a direção desse parâmetro como **dbParamOutput** ou **dbParamReturnValue** antes de executar **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="779dc-p103">This call produces one parameter — the return value. You need to set the direction of this parameter to **dbParamOutput** or **dbParamReturnValue** before executing the **[QueryDef](querydef-object-dao.md)**.</span></span>

<span data-ttu-id="779dc-117">Você precisa definir todas as direções de parâmetro, exceto **dbParamInput**, antes de acessar ou configurar os valores dos parâmetros e antes de executar **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="779dc-117">You need to set all parameter directions except **dbParamInput** before accessing or setting the values of the parameters and before executing the **QueryDef**.</span></span>

<span data-ttu-id="779dc-118">É necessário usar **dbParamReturnValue** para valores de retorno, mas nos casos em que aquela opção não é aceita pelo driver ou pelo servidor, você pode usar **dbParamOutput** no lugar.</span><span class="sxs-lookup"><span data-stu-id="779dc-118">You should use **dbParamReturnValue** for return values, but in cases where that option is not supported by the driver or the server, you can use **dbParamOutput** instead.</span></span>

<span data-ttu-id="779dc-p104">O driver do Microsoft SQL Server define automaticamente a propriedade **Direction** para todos os parâmetros de procedimento. Nem todos os drivers ODBC podem determinar a direção de um parâmetro de consulta. Nesses casos, é necessário definir a direção antes de executar a consulta.</span><span class="sxs-lookup"><span data-stu-id="779dc-p104">The Microsoft SQL Server driver automatically sets the **Direction** property for all procedure parameters. Not all ODBC drivers can determine the direction of a query parameter. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

## <a name="example"></a><span data-ttu-id="779dc-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="779dc-122">Example</span></span>

<span data-ttu-id="779dc-123">Este exemplo usa a propriedade **Direction** para configurar os parâmetros de uma consulta para uma fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="779dc-123">This example uses the **Direction** property to configure the parameters of a query to an ODBC data source.</span></span>

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

