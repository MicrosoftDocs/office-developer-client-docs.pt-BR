---
title: Método DBEngine.Idle (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bb92d21020d918d03195cbe0353e78b173257809
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863875"
---
# <a name="dbengineidle-method-dao"></a>Método DBEngine.Idle (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Suspende o processamento de dados, habilitando o mecanismo de banco de dados do Microsoft Access a concluir tarefas pendentes, como otimização de memória ou tempo limite da página (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Ocioso (***ação***)

*expressão* Uma variável que representa um objeto **DBEngine** .

### <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Ação</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica a ação a ser tomada. Pode ser uma das constantes <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O método **Idle** permite que o mecanismo de banco de dados do Microsoft Access execute tarefas em segundo plano que podem não estar atualizadas por causa de intenso processamento de dados. Isso geralmente ocorre em ambientes multiusuários e multitarefas que não têm tempo suficiente de planejamento em segundo plano para manter todos os registros em um **[Recordset](recordset-object-dao.md)** atual.

Em geral, bloqueios de leitura são removidos e os dados em objetos **Recordset** do tipo dynaset locais são atualizados apenas quando nenhuma outra ação ocorrer (inclusive movimentos de mouse). Se você usa periodicamente o método **Idle**, o mecanismo de banco de dados do Microsoft Access pode realizar o processamento de tarefas em segundo plano, liberando bloqueios de leitura desnecessários.

Especificar o argumento **dbRefreshCache** opcional atualiza a memória apenas com os dados mais recentes do banco de dados.

Você não precisa usar esse método em ambientes de um único usuário a menos que várias instâncias de um aplicativo estejam em execução. O método **Idle** pode aumentar o desempenho em um ambiente multiusuário porque força o mecanismo de banco de dados a gravar dados em disco, liberando bloqueios na memória.


> [!NOTE]
> [!OBSERVAçãO] Você também pode liberar bloqueios de leitura tornando as operações parte de uma transação.

## <a name="example"></a>Exemplo

Este exemplo usa o método **Idle** para assegurar que um procedimento de saída está acessando os dados mais atuais disponíveis no banco de dados. O procedimento IdleOutput é exigido para a execução do procedimento.

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

